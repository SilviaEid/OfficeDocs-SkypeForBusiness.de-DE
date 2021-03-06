---
title: Apps, Bots und Connectors in Microsoft Teams
ms.reviewer: ''
description: Erfahren Sie mehr über Apps, Bots und Connectors und darüber, wie Sie entscheiden können, welche dieser Komponenten basierend auf den Profil- und Geschäftsanforderungen Ihrer Organisation in Microsoft Teams bereitgestellt werden.
ms.topic: article
author: SerdarSoysal
ms.author: serdars
manager: serdars
audience: admin
ms.date: 01/28/2019
ms.service: msteams
ms.collection:
- M365-collaboration
f1.keywords:
- NOCSH
localization_priority: Priority
search.appverid: MET150
appliesto:
- Microsoft Teams
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c7ad1c83a09a17fb45adae149272177c8d42d17e
ms.sourcegitcommit: fb4edc26c566228d74c10cb51a063b5fdc7e11a1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "48177335"
---
# <a name="apps-bots--connectors-in-microsoft-teams"></a>Apps, Bots und Connectors in Microsoft Teams

Mithilfe von Apps finden Sie Inhalte aus Ihren bevorzugten Diensten und teilen sie direkt in Teams. Sie helfen Ihnen beim Anheften von Diensten oben in einem Kanal, beim Chat mit Bots, beim Teilen und Zuweisen von Aufgaben und ähnlichen Tätigkeiten. Weitere Informationen finden Sie unter [Übersicht über Apps in Teams](https://support.office.com/article/overview-of-apps-in-teams-747492ee-7cdd-4115-a993-8c7e7f98a3d0).

Es ist empfehlenswert, die von uns vorgeschlagenen Apps – wie etwa Planner – in Ihre erstmalige Teams-Bereitstellung mit aufzunehmen. Fügen Sie mit fortschreitender Einführung von Teams weitere Apps, Bots und Connectors hinzu.

Sie haben auch die Möglichkeit, Ihre eigenen benutzerdefinierten Apps zu erstellen. Weitere Informationen finden Sie in der [Dokumentation für Entwickler](/microsoftteams/platform/overview).

## <a name="apps-deployment-decisions"></a>Entscheidungen bei der Bereitstellung von Apps

Teams bietet ohne weitere Konfiguration eine hervorragende Zusammenarbeitserfahrung, und die meisten Organisationen stellen fest, dass die Standardeinstellungen für sie sinnvoll sind. Dieser Artikel hilft Ihnen bei der Entscheidung, ob einige der Standardeinstellungen geändert werden sollen, berücksichtigt dazu das Profil und die geschäftlichen Anforderungen Ihrer Organisation und führt Sie dann schrittweise durch die einzelnen Änderungen. Wir haben die Einstellungen in zwei Gruppen aufgeteilt und beginnen mit der Kernmenge der [Änderungen, die Sie mit größerer Wahrscheinlichkeit vornehmen](#core-deployment-decisions) werden. Die zweite Gruppe umfasst die [zusätzlichen Einstellungen](#additional-deployment-decisions), deren Konfiguration, abhängig von den Bedürfnissen Ihrer Organisation, sinnvoll sein kann.

## <a name="core-deployment-decisions"></a>Zentrale Entscheidungen bei der Bereitstellung

Dies sind die Einstellungen für Apps, deren Änderung in den meisten Organisationen sinnvoll ist (wenn die Standardeinstellungen von Teams sich für sie nicht eignen).

### <a name="app-availability-settings"></a>Verfügbarkeitseinstellungen für Apps 

Teams bietet eine Reihe von von Microsoft veröffentlichte und von Drittanbietern stammende Apps, um Benutzer zu binden, die Produktivität zu steigern und häufig verwendete Businessdienste in Teams zu integrieren. Laden Sie Apps aus dem Teams Store herunter. Standardmäßig sind alle Apps, einschließlich benutzerdefinierter Apps, die Sie mithilfe des [Teams Store-Genehmigungsverfahrens](https://docs.microsoft.com/microsoftteams/platform/publishing/apps-publish#microsoft-teams-app-approval-process) eingereicht haben, für alle Benutzer aktiviert. Beispielsweise können Benutzer die Planner-App verwenden, um Teamaufgaben in Teams zu erstellen und verwalten.

Standardmäßig sind alle von Microsoft bereitgestellten, Drittanbieter- und benutzerdefinierten Apps verfügbar. Sie können einzelne Apps ein- oder ausschalten. Es gibt organisationsweite Einstellungen, mit denen Sie alle Apps von Drittanbietern und/oder benutzerdefinierte Apps für Ihre gesamte Organisation ein- oder ausschalten können.

| Frage | Aktion |
|--------------|--------|
|Müssen Sie die Teams-Standardeinstellungen für Apps ändern? | Weitere Informationen zu Richtlinien und Einstellungen, die Sie zum Verwalten von Apps in Ihrer Organisation verwenden können, finden Sie unter [Administratoreinstellungen für Apps in Microsoft Teams](admin-settings.md).|
|||

### <a name="app-permissions-and-other-considerations"></a>App-Berechtigungen und andere Überlegungen

Apps erhalten ein Einverständnis von den Benutzern und werden vom Administrator oder IT-Experten mithilfe von Richtlinien verwaltet. Großenteils sind allerdings die Berechtigungen und Risikoprofile einer App in der App selbst definiert. 

| Frage | Aktion |
|--------------|--------|
|<br>Auf welche Apps möchte ich den Zugriff erlauben? Auf welche möchte ich keinen Zugriff erlauben?  | <ul><li>Eine Liste der Gesichtspunkte, die Sie beim Zulassen des Zugriffs auf eine App, einen Bot, eine Registerkarte oder einen Connector berücksichtigen sollten, finden Sie unter [Berechtigungen für Microsoft Teams-Apps und Überlegungen dazu](app-permissions.md).</li><li>Unter [Verwalten Ihrer Apps im Microsoft Teams Admin Center](manage-apps.md) finden Sie Informationen zur Bereitstellung einer App für Benutzer in Ihrer Organisation.</li></ul>|
|||

### <a name="bots-for-private-chats-and-channels"></a>Bots für private Chats und Kanäle

Bots sind automatisierte Programme, die auf Abfragen antworten oder Updates und Benachrichtigungen zu Details herausgeben, die Benutzer interessant finden oder über die sie auf dem Laufenden bleiben möchten. Mithilfe von Bots können Benutzer mit Clouddiensten wie Aufgabenverwaltung, Planung und Abstimmung in einem Teams-Chat interagieren. Teams unterstützt Bots in privaten Chats und Kanälen. Administratoren können steuern, ob die Verwendung von Bots in einer Microsoft 365- oder Office 365-Organisation zulässig ist.

| Frage | Aktion |
|--------------|--------|
|Möchte ich benutzerdefinierte Bots in meiner Organisation zulassen?|Weitere Informationen zum Hinzufügen von Bots finden Sie unter [Hinzufügen von Bots für private Chats und Kanäle in Microsoft Teams](add-bots.md). Informationen zum Aktivieren oder Deaktivieren von benutzerdefinierten Bots finden Sie unter [Administratoreinstellungen für Apps in Microsoft Teams](admin-settings.md).|
|||

### <a name="built-in-and-custom-tabs"></a>Integrierte und benutzerdefinierte Registerkarten

Besitzer und Teammitglieder können einem Kanal, einem privaten Chat oder einem Gruppenchat Registerkarten hinzufügen, um ihre Clouddienste besser integrieren zu können. Fügen Sie Registerkarten hinzu, um Benutzer bei Zugriff und Verwaltung der am häufigsten benötigten Daten zu unterstützen. In Kanälen werden standardmäßig die Registerkarten “Unterhaltungen” und “Dateien” erstellt. In jedem privaten Chat werden standardmäßig die Registerkarten “Unterhaltungen”, “Dateien”, “Organisation” und “Aktivität” erstellt. Über diese integrierten Registerkarten hinaus können Sie benutzerdefinierte Registerkarten entwerfen und hinzufügen. Informationen zum Aktivieren oder Deaktivieren von Registerkarten für Ihre Organisation finden Sie unter [Administratoreinstellungen für Apps in Microsoft Teams](admin-settings.md).

| Frage | Aktion |
|--------------|--------|
|Möchte ich benutzerdefinierte Registerkarten in meiner Organisation zulassen?|Weitere Informationen finden Sie unter [Verwenden integrierter und benutzerdefinierter Registerkarten in Teams](built-in-custom-tabs.md).|
|||

### <a name="custom-connectors"></a>Benutzerdefinierte Connectors

Mithilfe von Connectors bleiben Ihre Teams auf dem Laufenden, indem Inhalte und Updates von Diensten, die Sie häufig verwenden, direkt in einen Kanal übermittelt werden. Mithilfe von Connectors können Ihre Teams-Benutzer Updates von beliebten Diensten wie Twitter, Trello, Wunderlist, GitHub und Azure DevOps Services in ihren Teams-Chats empfangen.

| Frage | Aktion |
|--------------|--------|
|Möchte ich Benutzern das Erstellen benutzerdefinierter Connectors erlauben?|Weitere Informationen finden Sie unter [Verwenden von benutzerdefinierten Connectors in Teams](office-365-custom-connectors.md).|
|||

## <a name="additional-deployment-decisions"></a>Zusätzliche Bereitstellungsentscheidungen

Je nach den Bedürfnissen und der Konfiguration Ihrer Organisation kann es sinnvoll sein, diese Einstellungen zu ändern.

### <a name="activity-reports"></a>Aktivitätsberichte

Mithilfe von Aktivitätsberichten können Sie erfahren, wie Benutzer in Ihrer Organisation Teams verwenden. Wenn einige beispielsweise Teams noch nicht verwenden, wissen sie vielleicht nicht, wie sie den Einstieg finden sollen oder verstehen nicht, wie sie Teams zur Steigerung ihrer Produktivität und Verbesserung der Zusammenarbeit nutzen können. Ihre Organisation kann mithilfe der Aktivitätsberichte entscheiden, wo Schulungs- und Kommunikationsinitiativen priorisiert ansetzen sollen. Um Aktivitätsberichte anzuzeigen, müssen Sie ein globaler Administrator in Microsoft 365 oder Office 365, ein Teams-Dienstadministrator oder ein Skype for Business-Administrator sein.

| Frage | Aktion |
|--------------|--------|
| <br>Wer muss in der Lage sein, die Aktivitätsberichte zu sehen, und verfügen die betreffenden Benutzer über die richtigen Berechtigungen, um sie anzuzeigen? |<ul><li>Wenn Sie einem Benutzer keine Administratorrolle zuweisen möchten, können Sie die [Leseberechtigung für Berichte zuweisen](teams-activity-reports.md#reports-reader-role).</li><li>Informationen zum Zuweisen von Administratorrollen in Azure Active Directory finden Sie unter [Rollen und Berechtigungen](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles) und [Anzeigen und Zuweisen von Rollen](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-manage-roles-portal).</li></ul> |
|||

### <a name="app-templates"></a>App-Vorlagen

App-Vorlagen sind in GitHub verfügbare communitygesteuerte, produktionsbereite Quell-Apps für Microsoft Teams.  Jede enthält detaillierte Anweisungen dazu, wie Sie diese App für Ihre Organisation bereitstellen und installieren, indem sie eine anwendungsbereite App zur Verfügung stellt, die Sie umgehend installieren und verwenden können. Der gesamte Quellcode steht ebenfalls zur Verfügung. Sie können ihn im Detail durchsuchen oder abzweigen, um ihn Ihren Anforderungen entsprechend zu ändern.

| Frage | Aktion |
|--------------|--------|
| Möchte ich irgendwelche Teams-App-Vorlagen wie Icebreaker installieren? |Weitere Informationen finden Sie unter [App-Vorlagen für Teams](https://docs.microsoft.com/microsoftteams/platform/samples/app-templates?toc=MicrosoftTeams/toc.json&bc=/microsoftteams/breadcrumb/toc.json).|
|||


## <a name="next-steps"></a>Nächste Schritte
- [Fördern der Einführung](adopt-microsoft-teams-landing-page.md) empfohlener Apps, wie beispielsweise Planner.
- [Bereitstellung von Besprechungen und Konferenzen](deploy-meetings-microsoft-teams-landing-page.md)
- [Bereitstellen von Cloud Voice](cloud-voice-landing-page.md)


