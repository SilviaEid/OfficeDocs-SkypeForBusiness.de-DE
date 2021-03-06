---
title: Übersicht über dynamische Mitgliedschaft für Teams
author: SerdarSoysal
ms.author: serdars
manager: serdars
ms.reviewer: kblevens, phlouie
ms.topic: conceptual
ms.service: msteams
audience: admin
search.appverid: MET150
description: Erfahren Sie, wie Microsoft Teams mithilfe der dynamischen Mitgliedschaft Teams unterstützt, die Microsoft 365-Gruppen zugeordnet sind.
f1.keywords:
- NOCSH
localization_priority: Normal
ms.custom: seo-marvel-apr2020
ms.collection:
- M365-collaboration
appliesto:
- Microsoft Teams
ms.openlocfilehash: 75bd058d79b1f54a40ad0e42207178c9c29d08cd
ms.sourcegitcommit: 43d66693f6f08d4dcade0095bf613240031fec56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "46583924"
---
# <a name="overview-of-dynamic-membership-for-teams"></a>Übersicht über dynamische Mitgliedschaft für Teams

Microsoft Teams unterstützt Teams, die Microsoft 365-Gruppen zugeordnet sind, mithilfe der *dynamischen Mitgliedschaft*. Mit der dynamischen Mitgliedschaft kann die Mitgliedschaft in einem Team durch eine oder mehrere Regeln definiert werden, die in Azure Active Directory (Azure AD) nach bestimmten Benutzerattributen suchen. Benutzer werden automatisch zu den richtigen Teams hinzugefügt oder entfernt, wenn sich Benutzerattribute ändern oder Benutzer dem Mandanten beitreten und ihn belassen.

Mit der dynamischen Mitgliedschaft können Sie Teams für bestimmte Kohorten von Benutzern in Ihrer Organisation einrichten. Mögliche Szenarien sind:
- In einem Krankenhaus können unterschiedliche Teams für Krankenschwestern, Ärzte und Chirurgen zur Übertragung von Kommunikationen erstellt werden. Dies ist besonders wichtig, wenn das Krankenhaus auf temporäre Mitarbeiter angewiesen ist.
- Eine Universität kann ein Team für alle Dozenten innerhalb eines bestimmten Kollegiums erstellen, einschließlich einer Dozenten Gruppe, die sich häufig ändert.
- Eine Fluglinie möchte für jeden Flug ein Team erstellen (wie einen Dienstag Nachmittag nonstop von Chicago nach Atlanta) und eine häufig wechselnde Flight Crew automatisch zugewiesen oder entfernt werden.

Mithilfe dieser Funktion werden die Mitglieder eines bestimmten Teams automatisch basierend auf einem bestimmten Satz von Kriterien aktualisiert, anstatt die Mitgliedschaft manuell zu verwalten. Hierfür sind Azure AD Premium P1-Lizenzen erforderlich, und die Teammitgliedschaft kann [von einem mandantenadministrator](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership) für die Azure AD-Eigenschaften jedes Benutzers zugewiesen werden, vorausgesetzt, Sie verfügen über einen Mandanten und ein Administratorkonto.

Microsoft Teams kann zwischen ein paar Minuten und bis zu zwei Stunden dauern, um dynamische Mitgliedschaftsänderungen wiederzugeben, sobald Sie in der Microsoft 365-Gruppe für ein Team wirksam werden.

> [!NOTE]
> - Regeln können definieren, wer ein Teammitglied ist, aber nicht, wer ein Teambesitzer ist.
> - Aktuelle Grenzwerte für Team-und Kanal Größen finden Sie unter [Grenzwerte und Spezifikationen für Microsoft Teams](limits-specifications-teams.md) .
> - Besitzer können Benutzer nicht als Mitglieder des Teams hinzufügen oder entfernen, da Mitglieder durch dynamische Gruppenregeln definiert werden.
> -    Mitglieder können Teams nicht von dynamischen Gruppen zurücklassen.

## <a name="creating-and-managing-a-microsoft-365-group-with-dynamic-membership"></a>Erstellen und Verwalten einer Microsoft 365-Gruppe mit dynamischer Mitgliedschaft

Wenn Sie als mandantenadministrator angemeldet sind, folgen Sie den Anweisungen unter [Erstellen einer dynamischen Gruppe und Überprüfen des Status](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-create-rule). Beziehen Sie sich bei Bedarf auf [Dynamische Mitgliedschaftsregeln für Gruppen in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership).

## <a name="create-a-new-team-with-your-microsoft-365-group"></a>Erstellen eines neuen Teams mit Ihrer Microsoft 365-Gruppe

Lassen Sie jetzt Zeit, bis die Mitgliedschaftsänderungen wirksam werden, und erstellen Sie ein neues Team, wie unter [Erstellen eines Teams aus einer vorhandenen Gruppe](https://support.microsoft.com/en-us/office/create-a-team-from-an-existing-group-24ec428e-40d7-4a1a-ab87-29be7d145865)beschrieben.

## <a name="apply-dynamic-membership-to-an-existing-team"></a>Anwenden einer dynamischen Mitgliedschaft auf ein vorhandenes Team

Sie können auch ein vorhandenes Team übernehmen und es so ändern, dass es eine dynamische Mitgliedschaft aufweist, wie unter [Ändern der statischen Gruppenmitgliedschaft in Dynamic in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-change-type)beschrieben.

## <a name="changes-in-client-behavior"></a>Änderungen des Clientverhaltens

Sobald die dynamische Mitgliedschaft für ein Team aktiviert ist, können die Teams-Clients die Mitgliederverwaltung für das Team nicht mehr zulassen. Optionen zum Hinzufügen von Mitgliedern, Bearbeiten von Mitgliederrollen, senden und Genehmigen von Join-Anfragen und belassen des Teams sind alle verborgen.
