---
title: Verwalten der explorativen Microsoft Teams-Umgebung
author: SerdarSoysal
ms.author: serdars
manager: serdars
ms.topic: reference
audience: Admin
ms.reviewer: baluc
ms.service: msteams
search.appverid: MET150
localization_priority: Priority
description: Microsoft 365- oder Office 365-Benutzer, die nicht für Microsoft Teams lizenziert sind, können eine explorative Lizenz von Microsoft Teams starten.
f1.keywords:
- NOCSH
ms.collection:
- M365-collaboration
- Teams_ITAdmin_RemoteWorkers
- m365initiative-deployteams
appliesto:
- Microsoft Teams
ms.openlocfilehash: df06c03ab37a98c5ea4404d8dbd12703b07ad3ee
ms.sourcegitcommit: 4386f4b89331112e0d54943dc3133791d5dca3fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "49611809"
---
# <a name="manage-the-microsoft-teams-exploratory-license"></a>Verwalten der explorativen Lizenz von Microsoft Teams

Die Microsoft Teams Exploratory-Umgebung ermöglicht Benutzern in Ihrer Organisation, die über Azure Active Directory (Azure AD) verfügen und nicht für Microsoft Teams lizenziert sind, eine explorative Microsoft Teams-Umgebung zu starten. Administratoren können dieses Feature für Benutzer in ihrer Organisation aktivieren oder deaktivieren. Die frühere [Microsoft Commercial Cloud-Testversion](iw-trial-teams.md) wurde durch die explorative Microsoft Teams-Umgebung ersetzt.

## <a name="whats-in-the-teams-exploratory-experience"></a>Was steckt in der Microsoft Teams Exploratory-Umgebung?

Folgende Dienstpläne werden einem Administrator als Teil der Microsoft Teams Exploratory-Umgebung angezeigt:

- Exchange Online (Plan 1)
- Flow für Microsoft 365 oder Office 365
- MyAnalytics Insights
- Microsoft Forms (Plan E1)
- Microsoft Planner
- Microsoft Search
- Microsoft StaffHub
- Microsoft Stream für Microsoft 365 und Office 365 E1 SKUs <sup>1</1>
- Microsoft Teams
- Verwaltung mobiler Geräte für Microsoft 365 oder Office 365
- Office Mobile-Apps für Office 365
- Office Online
- PowerApps für Microsoft 365 oder Office 365
- SharePoint Online (Plan 1)
- Sway
- To-Do (Plan 1)
- Whiteboard (Plan 1)
- Yammer Enterprise

  <sup>1</sup> Der Wechsel von Microsoft Stream zu [OneDrive for Business und SharePoint für Besprechungsaufzeichnungen](tmr-meeting-recording-change.md) erfolgt schrittweise. Beim Start können Sie sich für diese Umgebung entscheiden. Sie müssen sich im November abmelden, wenn Sie Stream weiterhin verwenden möchten. Anfang 2021 müssen alle Kunden OneDrive for Business und SharePoint für neue Besprechungsaufzeichungen verwenden.

## <a name="whos-eligible"></a>Wer ist anspruchsberechtigt?

Benutzer erfüllen die Kriterien für eine Microsoft Teams Exploratory-Umgebung wenn sie:

- Über eine verwaltete Azure AD-Domain-E-Mail-Adresse verfügen.
- Zu einem Mandanten mit einem kostenpflichtigen Abonnement gehören.

Benutzern muss (im Microsoft 365 Admin Center) die Möglichkeit bereitgestellt werden, sich für Apps und Testversionen zu registrieren. Weitere Informationen finden Sie weiter unten in diesem Artikel unter [Verwalten der explorativen Microsoft Teams-Umgebung](#manage-the-teams-exploratory-experience).

## <a name="who-isnt-eligible"></a>Wer ist nicht berechtigt?

Benutzer erfüllen nicht die Kriterien, wenn sie:

- Teams zurzeit oder früher als kostenpflichtige oder unbezahlte Lizenz oder aber als Testlizenz verwenden bzw. verwendet haben
- Zu einem Mandanten gehören, der mindestens ein spezielles COVID-Angebot nutzte/empfing.

Ihre Organisation ist nicht für dieses Angebot berechtigt, wenn Sie ein Syndication-Partnerkunde oder ein GCC-, GCC High-, DoD- oder EDU-Kunde sind.

## <a name="how-users-sign-up-for-the-teams-exploratory-experience"></a>So können Benutzer sich für die explorative Microsoft Teams-Umgebung registrieren

Berechtigte Benutzer können sich für die explorative Microsoft Teams-Umgebung (Microsoft Teams Exploratory) registrieren, indem sie sich bei Microsoft Teams ([teams.microsoft.com](https://teams.microsoft.com)) anmelden. Zurzeit wird das Aktivieren von Exploratory über ein mobiles Gerät nicht unterstützt. Bei ihrer Anmeldung wird berechtigten Benutzern diese Lizenz automatisch zugewiesen. Der Mandantenadministrator erhält eine E-Mail-Benachrichtigung, wenn eine Person in seiner Organisation die Microsoft Teams Exploratory-Umgebung zum ersten Mal startet.

## <a name="manage-the-teams-exploratory-experience"></a>Verwalten der Microsoft Teams Exploratory-Umgebung

Die Microsoft Teams Exploratory-Umgebung ist für die Initialisierung durch einzelne Endbenutzer bestimmt, und Sie sind nicht berechtigt, dieses Angebot im Namen von Endbenutzern oder Angestellten zu initiieren.

Die Microsoft Teams Exploratory-Umgebung wird mit einer Exchange Online-Lizenz geliefert, die dem Benutzer jedoch erst vom Administrator zugewiesen werden muss. Verfügt der Benutzer noch über keine Exchange-Lizenz, kann er keine Besprechungen in Microsoft Teams planen und andere Microsoft Teams-Funktionen möglicherweise nicht verwenden, solange der Administrator die Exchange Online-Lizenz noch nicht zugewiesen hat.

Administratoren können die Option zur Ausführung der explorativen Microsoft Teams-Umgebung für Benutzer in ihrer Organisation über den Switch **Test-Apps und -Dienste** deaktivieren.

### <a name="prevent-users-from-installing-trial-apps-and-services"></a>Verhindern, dass Benutzer Test-Apps und -dienste installieren

Sie können die Möglichkeit eines Benutzers zum Installieren von Test-Apps und -Diensten deaktivieren. Auf diese Weise hindern Sie ihn daran, die explorative Microsoft Teams-Umgebung auszuführen.

1. Navigieren Sie im Microsoft 365 Admin Center zu **Einstellungen** > **Organisationseinstellungen**, wählen Sie **Dienste** und dann **Apps und Dienste im Besitz des Benutzers** aus.

    ![die Seite „Dienste“ im Admin Center](media/iw-trial-services.png)

2. Deaktivieren Sie das Kontrollkästchen **Benutzer Test-Apps und -dienste installieren lassen**.

    ![die Seite „Apps und Dienste im Besitz des Benutzers" im Admin Center](media/iw-trial-user-owned-apps-services.png)

    > [!NOTE]
    > Wenn Ihre Organisation nicht berechtigt ist, die explorative Microsoft Teams-Umgebung in Anspruch zu nehmen, wird die Option **Benutzer Test-Apps und -dienste installieren lassen** nicht angezeigt.

### <a name="manage-availability-for-a-user-with-a-license-that-includes-teams"></a>Verwalten der Verfügbarkeit für einen Benutzer mit einer Lizenz, die Microsoft Teams umfasst

Ein Benutzer, dem eine Lizenz zugewiesen wurde, die Microsoft Teams bereits umfasst, ist nicht berechtigt, die explorative Microsoft Teams-Umgebung in Anspruch zu nehmen. Wenn der Microsoft Teams-Serviceplan aktiviert ist, kann sich der Benutzer anmelden und Microsoft Teams verwenden. Wenn der Dienstplan deaktiviert ist, kann sich der Benutzer nicht anmelden, und die explorative Microsoft Teams-Umgebung ist nicht verfügbar. Sie benötigen Administratorberechtigungen.

So deaktivieren Sie den Zugriff auf Teams:

1. Wählen Sie im Microsoft 365 Admin Center, **Benutzer** > **Aktive Benutzer** aus.

2. Aktivieren Sie das Kontrollkästchen neben dem Namen des Benutzers.

3. Wählen Sie in der Zeile **Produktlizenzen** die Option **Bearbeiten** aus.

4. Setzen Sie im Bereich **Produktlizenzen** die Umschaltfläche auf **Aus**.

    ![die Seite „Produktlizenzen“ im Admin Center](media/iw-trial-enable-3.png)

### <a name="manage-teams-availability-for-users-who-are-already-using-the-teams-exploratory-experience"></a>Verwalten der Verfügbarkeit von Microsoft Teams für Benutzer, die bereits die explorative Microsoft Teams-Umgebung verwenden

Wenn ein Benutzer die explorative Microsoft Teams-Umgebung ausführt, können Sie diese deaktivieren, indem Sie die Lizenz oder den Dienstplan entfernen. Sie benötigen Administratorberechtigungen.

So deaktivieren Sie die Lizenz für die Microsoft Teams Exploratory-Umgebung:

1. Wählen Sie im Microsoft 365 Admin Center, **Benutzer** > **Aktive Benutzer** aus.

2. Aktivieren Sie das Kontrollkästchen neben dem Namen des Benutzers.

3. Wählen Sie in der Zeile **Produktlizenzen** die Option **Bearbeiten** aus.

4. Wechseln Sie im Bereich **Produktlizenzen** die Umschaltfläche für die explorative Lizenz auf **Aus**.

    >[!Note]
    >Die Umschaltfläche für die explorative Microsoft Teams-Umgebung wird angezeigt, sobald der erste Benutzer in der Organisation die explorative Microsoft Teams-Umgebung startet.

### <a name="manage-teams-for-users-who-have-the-teams-exploratory-license"></a>Verwalten von Microsoft Teams für Benutzer, die über die explorative Microsoft Teams-Lizenz verfügen

Sie können Benutzer mit einer explorativen Microsoft Teams-Lizenz genauso verwalten wie Benutzer mit einer regulären kostenpflichtigen Lizenz. Weitere Informationen finden Sie unter [Verwalten von Microsoft Teams-Einstellungen in Ihrer Organisation](enable-features-office-365.md).

### <a name="upgrade-users-from-the-teams-exploratory-license"></a>Upgraden von Benutzern mit der explorativen Microsoft Teams-Lizenz

Um Benutzer mit der Microsoft Teams Exploratory-Lizenz zu upgraden (Sie benötigen Administratorberechtigungen), gehen Sie wie folgt vor:

1. Kaufen Sie ein Abonnement, das Microsoft Teams enthält.

2. Entfernen Sie das Abonnement der explorativen Microsoft Teams-Umgebung des Benutzers.

3. Weisen Sie die neu erworbene Lizenz zu.

Weitere Informationen finden Sie unter [Microsoft Teams-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/teams-service-description).

> [!NOTE]
> Wenn die Microsoft Teams Exploratory-Lizenz endet und für einen Benutzer nicht sofort ein Upgrade auf ein Abonnement vorgenommen wird, das Microsoft Teams umfasst, hat er eine Nachfrist von 30 Tagen und dann weitere 30 Tage, nach deren Ablauf die Daten gelöscht werden. Der Benutzer ist weiterhin in Azure Active Directory vorhanden. Sobald dem Benutzer eine neue Lizenz zugewiesen wurde, um Microsoft Teams-Funktionen wieder zu aktivieren, sind die Inhalte weiterhin vorhanden, sofern der Benutzer innerhalb der Nachfrist hinzugefügt wird.

## <a name="what-happens-to-legacy-microsoft-teams-commercial-cloud-trial-licenses"></a>Was geschieht mit älteren Lizenzen für Microsoft Teams Commercial Cloud-Testversionen?

Seit Februar 2020 können anspruchsberechtigte Benutzer mit der Nutzung der neuesten Microsoft Teams Exploratory-Umgebung beginnen. Alle Legacylizenzen für den Test der kommerziellen Cloud von Microsoft Teams werden automatisch in das neue Angebot konvertiert, bevor die Testversion abläuft.

Wenn sich ein Benutzer zum ersten Mal bei seiner abgelaufenen Microsoft Teams Commercial Cloud-Testversionen anmeldet, wird ihm automatisch eine Lizenz für die Microsoft Teams Exploratory-Umgebung zugewiesen. Benutzer werden erst konvertiert, wenn sie sich anmelden.

### <a name="remove-a-teams-exploratory-license"></a>Entfernen einer explorativen Microsoft Teams-Lizenz

- Wenn Sie diese Lizenz über PowerShell entfernen möchten, ziehen Sie [Entfernen von Lizenzen von Benutzerkonten mit Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/remove-licenses-from-user-accounts-with-office-365-powershell) zurate.

- Wenn Sie diese Lizenz über das Verwaltungsportal entfernen möchten, lesen Sie [Löschen eines Benutzers aus Ihrer Organisation](https://docs.microsoft.com/microsoft-365/admin/add-users/delete-a-user).

## <a name="what-is-the-data-retention-policy"></a>Was sieht die Datenaufbewahrungsrichtlinie vor

Informationen hierzu finden Sie unter [Informationen zum Microsoft 365-Abonnement](https://docs.microsoft.com/microsoft-365/commerce/subscriptions/what-if-my-subscription-expires?view=o365-worldwide).

## <a name="how-long-does-the-teams-exploratory-experience-last"></a>Wie lange die Teams Exploratory-Umgebung verfügbar ist

Die Microsoft Teams Exploratory-Umgebung wird ohne Zusatzkosten für 12 Monate (ab der ersten Benutzerregistrierung) plus einer zusätzlichen Nachfrist von 30 Tagen bereitgestellt. Zu diesem Zeitpunkt müssen Endbenutzer mit einer Lizenz für die Microsoft Exploratory-Umgebung zu einer kostenpflichtigen Lizenz wechseln, die Microsoft Teams enthält. Dasselbe Enddatum gilt für alle Benutzer in demselben Mandanten, wobei die 12-Monats-Frist ab dem Anmeldedatum des ersten Benutzers beginnt.

### <a name="what-happens-if-an-end-user-initiates-the-microsoft-teams-exploratory-experience-just-before-the-anniversary-or-renewal-date"></a>Was geschieht, wenn ein Endbenutzer kurz vor dem Fälligkeits- oder Verlängerungsdatum mit der Nutzung der Microsoft Teams Exploratory-Umgebung beginnt?

Lizenzen für die Microsoft Teams Exploratory-Umgebung, die innerhalb von 90 Tagen nach dem **Fälligkeitstag** oder der **Verlängerung des Vertrags** begonnen wurden, sind bis zum anschließenden Fälligkeitstag oder Verlängerungszyklus nicht zum Wechsel zu einer kostenpflichtigen Lizenz verpflichtet.

### <a name="what-if-my-agreement-doesnt-have-an-anniversary-or-yearly-renewal-date-for-example-month-to-month-agreements"></a>Was ist zu tun, wenn mein Vertrag keinen Fälligkeits- oder jährliches Verlängerungsdatum aufweist (z. B. Monatsverträge)?

Bei Verträgen ohne Fälligkeits- oder jährliches Verlängerungsdatum wird das Folgejahr, nachdem der erste Endbenutzer die Microsoft Teams Exploratory-Lizenz aktiviert hat, als Fälligkeits- oder Verlängerungsdatum behandelt. Benutzer mit der Lizenz für die Microsoft Teams Exploratory-Umgebung müssen bis zu diesem Datum jedes Jahr entsprechend den in diesem Artikel genannten Richtlinien zu einer kostenpflichtigen Lizenz wechseln.

Wenn der erste Endbenutzer Microsoft Teams Exploratory zum Beispiel am 19. Juni 2020 aktiviert, müssen er und alle anderen berechtigten Benutzer im Kundenmandanten bis zum 19. Juni 2021 auf eine kostenpflichtige Lizenz mit Teams umsteigen.

> [!Note]
> Nach Ablauf der vorherigen Exploratory-Testlizenz werden Kunden deaktiviert und drei Monate lang daran gehindert, eine neue Testversion zu starten.
