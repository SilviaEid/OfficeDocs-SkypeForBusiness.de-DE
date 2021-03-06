---
title: Upgrade von Skype for Business-hybridbereitstellung in Teams
author: lanachin
ms.author: v-lanac
manager: serdars
ms.topic: article
ms.service: msteams
audience: admin
ms.reviewer: landerl
description: Erfahren Sie, wie Sie Ihre Organisation von einer Skype for Business-hybridbereitstellung auf Microsoft Teams aktualisieren.
localization_priority: Normal
search.appverid: MET150
f1.keywords:
- CSH
ms.custom:
- Teams-upgrade-guidance
- seo-marvel-mar2020
ms.collection:
- Teams_ITAdmin_JourneyFromSfB
- M365-collaboration
appliesto:
- Microsoft Teams
ms.openlocfilehash: 72786dc2ef5cefe7c3c87c5a376cc01d93a2c22c
ms.sourcegitcommit: b07938c0b6edafacaeaaef205a1be00c4c1693ba
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "47940515"
---
# <a name="upgrade-from-a-skype-for-business-hybrid-deployment-to-teams"></a>Upgrade von einer Skype for Business-hybridbereitstellung in Teams

![Phasen der Upgrade-Reise, wobei der Schwerpunkt auf der Bereitstellungs-und Implementierungsphase liegt](media/upgrade-banner-deployment.png "Phasen der Upgrade-Reise, wobei der Schwerpunkt auf der Bereitstellungs-und Implementierungsphase liegt")

Dieser Artikel ist Teil der Bereitstellungs-und Implementierungsphase Ihrer Upgrade-Reise. Bevor Sie fortfahren, bestätigen Sie, dass Sie die folgenden Aktivitäten abgeschlossen haben:

- [Ernennen der Projektbeteiligten](upgrade-enlist-stakeholders.md)
- [Definieren des Projektumfangs](https://aka.ms/SkypetoTeams-Scope)
- [Vertrautmachen mit der Koexistenz und Interoperabilität von Skype for Business und Microsoft Teams](https://aka.ms/SkypeToTeams-Coexist)
- [Auswählen der Upgrade-Strategie](upgrade-and-coexistence-of-skypeforbusiness-and-teams.md)
- [Ihre Umgebung vorbereitet](https://aka.ms/SkypeToTeams-TechnicalReadiness)
- [Vorbereiten Ihrer Organisation](https://aka.ms/SkypeToTeams-UserReadiness)
- [Durchgeführt eines Pilotprojekts](https://aka.ms/SkypeToTeams-Pilot)

Befolgen Sie die Anleitungen in diesem Artikel, wenn Sie Skype for Business oder Microsoft lync lokal bereitgestellt und in einer hybridbereitstellung mit Ihrer Microsoft 365-oder Office 365-Organisation konfiguriert haben und Ihre Organisation ein Upgrade auf Teams entweder selektiv durchführen möchte, indem Sie mehrere Koexistenzmodus verwenden – oder All-in. Wenn Sie eine Upgrade-Reise durchführen möchten, müssen Sie Ihre Benutzer in Skype for Business Online verschieben (sofern Sie nicht bereits online sind) und Ihnen dann den entsprechenden Koexistenz-und Aktualisierungsmodus zuweisen.

> [!IMPORTANT]
> [!INCLUDE [upgrade-disclaimer](includes/upgrade-disclaimer.md)]

## <a name="step-1-move-users-to-skype-for-business-online"></a>Schritt 1: Verschieben von Benutzern in Skype for Business Online

Dieser Schritt bezieht sich auf Benutzer, die derzeit lokal verwaltet werden. Weitere Informationen zum Verschieben dieser Benutzer in Skype for Business Online finden Sie unter [Verschieben von Benutzern von lokal in Skype for Business Online](/skypeforbusiness/skype-for-business-hybrid-solutions/deploy-hybrid-connectivity/move-users-from-on-premises-to-skype-for-business-online).

## <a name="step-2-assign-a-coexistence-and-upgrade-mode"></a>Schritt 2: Zuweisen einer Koexistenz und eines Aktualisierungsmodus

Nachdem Sie Ihre Benutzer in Skype for Business Online verschoben haben, können Sie Ihnen den passenden Koexistenzmodus zuweisen, der auf der von Ihrer Organisation ausgewählten Upgrade-Reise basiert. Weitere Informationen finden Sie unter [Festlegen von Koexistenz-und Upgradeeinstellungen](https://aka.ms/SkypeToTeams-SetCoexistence) und [TeamsUpgradePolicy: Verwalten von Migration und Koexistenz](upgrade-to-teams-on-prem-tools.md).

> [!NOTE]
> Mit Skype for Business Server 2019 und einem zukünftigen kumulativen Update von Skype for Business Server 2015 können Sie Schritt 1 (Verschieben von Benutzern in Skype for Business Online) und Schritt 2 (Benutzer auf Teams aktualisieren) in einem einzigen Schritt ausführen. Weitere Informationen werden nach der Veröffentlichung von Skype for Business Server 2019 bereitgestellt.

## <a name="phone-system-and-teams-upgrade"></a>Upgrade für Telefonsysteme und Teams

Wenn Sie Ihre Skype for Business-hybridbereitstellung in das Telefon System mit Anrufplänen umstellen und Microsoft Ihr öffentlich geschaltetes Telefonnetz (PSTN)-Anbieter ist – und vorausgesetzt, dass Sie die Portierung von Telefonnummern abgeschlossen haben – werden durch das Upgrade Ihrer Benutzer auf Teams automatisch eingehende PSTN-Anrufe an Teams übertragen.

Wenn keine Anrufpläne verfügbar sind oder Sie beabsichtigen, Ihren vorhandenen PSTN-Verbindungsanbieter zu verwenden, müssen Sie Ihre Enterprise-VoIP-Bereitstellung – oder die Hybrid-sprach Bereitstellung, die Ihre vorhandene lokale Bereitstellung oder Cloud Connector Edition verwendet – auf das direkte Routing von Microsoft Phone System umstellen. Wenn Sie Ihre Benutzer auf Teams aktualisieren möchten, lesen Sie die [zusätzlichen Überlegungen für das direkte Routing von Telefonsystemen](2-envision-make-my-service-decisions-direct-routing.md).
