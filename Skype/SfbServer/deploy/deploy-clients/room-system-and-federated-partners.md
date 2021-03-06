---
title: Skype Room System- und Skype for Business-Verbundpartner
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.reviewer: sohailta
ms.topic: quickstart
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: 1cc20323-ecba-4e87-a861-e54193e64cf0
description: Lesen Sie dieses Thema, um zu erfahren, wie Sie Skype Room System für Skype for Business-Verbundpartner einrichten.
ms.openlocfilehash: d5ee83857aa439791e2a31ef201e0f365dbb8408
ms.sourcegitcommit: dd3a3ab4ddbdcfe772f30fb01ba3b97c45c43dd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "41768718"
---
# <a name="skype-room-system-and-skype-for-business-federated-partners"></a>Skype Room System- und Skype for Business-Verbundpartner
 
Lesen Sie dieses Thema, um zu erfahren, wie Sie Skype Room System für Skype for Business-Verbundpartner einrichten.
  
## <a name="skype-room-system-and-skype-for-business-federated-partners"></a>Skype Room System- und Skype for Business-Verbundpartner

Das Skype Room-System basiert auf dem Link "an Skype for Business-Besprechung teilnehmen" in der Besprechungsanfrage des Kalenders. Der Link für die Teilnahme ist normalerweise im Textkörper der Besprechungsanfrage zu finden. Das Skype Room-System hängt jedoch davon ab, dass dieser Link in den MAPI-Eigenschaften der Nachricht vorhanden ist. Wenn diese Besprechungsanfrage an Remote Organisationen (Skype for Business-Verbundpartner) gesendet wird, wird standardmäßig im Skype Room-System der Remoteorganisation der Link "Besprechungsteilnahme" im Kalender nicht angezeigt. In der Tat können Outlook-Benutzer in der Remoteorganisation mit einem Rechtsklick auf das Kalenderelement oder innerhalb der Besprechungserinnerung nicht an der Skype for Business-Besprechung teilnehmen. Sie müssen die Besprechungseinladung öffnen und im Textkörper der Nachricht auf an Skype for Business-Besprechung teilnehmen klicken. 
  
Der Grund für dieses Einschränkung ist, dass Outlook und Microsoft Exchange keine spezielle Methode dafür kennen, Informationen für den Versand von Nachrichten über das Internet mit einzuschließen. Diese Methode, die als „Transport Neutral Encapsulation Format“ (TNEF) bezeichnet wird, ist für Nachrichten, die aus einem Exchange-Unternehmen extern versendet werden, standardmäßig deaktiviert. Damit ein Link zur Besprechungsteilnahme in einem Remote-Skype-Raum System angezeigt wird, muss die sendende Organisation TNEF mithilfe des folgenden Befehls aktivieren:
  
```powershell
New-RemoteDomain -DomainName Contoso.com -Name Contoso
Set-RemoteDomain -Identity Contoso -TNEFEnabled $true
```

Nachdem TNEF für das Remote-Unternehmen aktiviert worden ist, wird jede über das Internet an das Unternehmen gesendete Nachricht als Anlage im TNEF-Format geschickt. Wenn die TNEF-Funktion aktiviert ist und eine Skype for Business-Besprechungsanfrage an den Skype for Business-Verbundpartner gesendet wird, kann Skype Room System die Teilnahme an Skype for Business-Besprechungen wiedergeben, und Remotebenutzer können an Skype for Business-Besprechungen teilnehmen. 
