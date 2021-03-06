---
title: Trunkfailover bei ausgehenden Anrufen
ms.author: crowe
author: CarolynRowe
manager: serdars
audience: ITPro
ms.reviewer: NMuravlyannikov
ms.topic: article
ms.service: msteams
localization_priority: Normal
search.appverid: MET150
ms.collection:
- M365-voice
appliesto:
- Microsoft Teams
f1.keywords:
- NOCSH
description: In diesem Thema erfahren Sie, wie Sie trunk-Failovers bei ausgehenden Anrufen von Teams an den Session Border Controller (SBC) behandeln.
ms.openlocfilehash: c88394cba0a98316ac272901a6ab2972e9eaf3c8
ms.sourcegitcommit: ed3d7ebb193229cab9e0e5be3dc1c28c3f622c1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41836177"
---
# <a name="trunk-failover-on-outbound-calls"></a>Trunkfailover bei ausgehenden Anrufen

In diesem Thema wird beschrieben, wie Sie trunk-Failovers bei ausgehenden Anrufen vermeiden – von Teams bis zum Session Border Controller (SBC).

## <a name="failover-on-network-errors"></a>Failover bei Netzwerkfehlern

Wenn ein trunk aus irgendeinem Grund nicht verbunden werden kann, wird die Verbindung mit dem gleichen Stamm aus einem anderen Microsoft-Rechenzentrum getestet. Ein trunk ist möglicherweise nicht verbunden, beispielsweise, wenn eine Verbindung verweigert wird, wenn ein TLS-Timeout vorliegt oder wenn es andere Probleme auf Netzwerkebene gibt.
So kann beispielsweise eine Verbindung fehlschlagen, wenn ein Administrator den Zugriff auf den SBC nur von bekannten IP-Adressen einschränkt, aber vergisst, die IP-Adressen aller Microsoft Direct-Routing-Rechenzentren in der Zugriffssteuerungsliste (ACL) des SBC abzulegen. 

## <a name="failover-of-specific-sip-codes-received-from-the-session-border-controller-sbc"></a>Failover spezifischer SIP-Codes, die vom Session Border Controller (SBC) empfangen wurden

Wenn Direktes Routing als Antwort auf eine ausgehende Einladung 4xx-oder 6xx-SIP-Fehlercodes erhält, gilt der Anruf standardmäßig als abgeschlossen. Outgoing bedeutet einen Anruf von einem Teams-Client an das öffentlich geschaltete Telefonnetz (PSTN) mit folgendem Verkehrsfluss: Teams Client-#a0 Direct Routing-#a1 SBC-#a2-Telefonie-Netzwerk.

Die Liste der SIP-Codes befindet sich im [SIP-RFC (Session Initiation Protocol)](https://tools.ietf.org/html/rfc3261).

Nehmen Sie eine Situation an, in der ein SBC auf eine eingehende Einladung mit dem Code "408-Anforderungs Timeout: der Server konnte keine Antwort innerhalb einer angemessenen Zeitspanne erstellen, beispielsweise antwortete, wenn er den Standort des Benutzers nicht rechtzeitig ermitteln konnte. Der Client kann die Anfrage zu einem späteren Zeitpunkt ohne Änderungen wiederholen. "

Dieser besondere SBC hat möglicherweise Probleme beim Herstellen einer Verbindung mit dem aufgerufenen--möglicherweise aufgrund einer fehlerhafte Netzwerkkonfiguration oder eines anderen Fehlers. Es gibt jedoch noch einen SBC auf der Route, der möglicherweise in der Lage ist, den aufgerufenen zu erreichen.

Wenn ein Benutzer einen Anruf an eine Telefonnummer tätigt, gibt es im folgenden Diagramm zwei SBCS in der Route, die diesen Anruf potenziell übermitteln können. Anfangs ist SBC1.contoso.com für den Anruf ausgewählt, aber SBC1.contoso.com kann aufgrund eines Netzwerkproblems kein PTSN-Netzwerk erreichen.
Standardmäßig wird der Anruf zurzeit abgeschlossen. 
 
![Diagramm mit SBC, das PSTN aufgrund eines Netzwerkproblems nicht erreichen kann](media/direct-routing-failover-response-codes1.png)

Es gibt jedoch noch einen SBC auf der Route, der den Anruf potenziell abliefern kann.
Wenn Sie den Parameter `Set-CSOnlinePSTNGateway -Identity sbc1.contoso.com -FailoverResponseCodes "408"`konfigurieren, wird der zweite SBC ausprobiert--SBC2.contoso.com im folgenden Diagramm:

![Diagramm mit Routing an zweiten SBC](media/direct-routing-failover-response-codes2.png)

Durch das Festlegen der Parameter-FailoverResponseCodes und die Angabe der Codes können Sie Ihr Routing optimieren und potenzielle Probleme vermeiden, wenn ein SBC aufgrund von Netzwerk-oder anderen Problemen keinen Anruf führen kann.

Standardwerte: 408, 503, 504

