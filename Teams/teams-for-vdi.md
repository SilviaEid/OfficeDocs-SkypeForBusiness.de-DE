---
title: Microsoft Teams für Virtualized Desktop Infrastructure
author: LanaChin
ms.author: v-lanac
manager: serdars
ms.topic: article
ms.service: msteams
ms.reviewer: rafarhi, jmorrow
audience: admin
description: Erfahren Sie, wie Sie Microsoft Teams in einer VDI-Umgebung (virtualisierte Desktop Infrastruktur) ausführen.
localization_priority: Normal
search.appverid: MET150
f1.keywords:
- NOCSH
ms.collection:
- M365-collaboration
- m365initiative-deployteams
appliesto:
- Microsoft Teams
ms.openlocfilehash: 53a4fca44e63f76875205726b4d145b815b9ee9c
ms.sourcegitcommit: ef58f429658333b53d72d5fa7265701d2a18326b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "49350637"
---
# <a name="teams-for-virtualized-desktop-infrastructure"></a>Microsoft Teams für Virtualized Desktop Infrastructure

In diesem Artikel werden die Anforderungen und Einschränkungen für die Verwendung von Microsoft Teams in einer virtualisierten Umgebung beschrieben.

## <a name="what-is-vdi"></a>Was ist VDI?

Virtual Desktop Infrastructure (VDI) ist eine Virtualisierungstechnologie, die ein Desktop Betriebssystem und Anwendungen auf einem zentralen Server in einem Rechenzentrum hostet. Dies ermöglicht Benutzern mit einer vollständig gesicherten und kompatiblen zentralisierten Quelle eine vollständig personalisierte Desktopoberfläche.

Microsoft Teams in einer virtualisierten Umgebung unterstützen Chats und Zusammenarbeit. Und mit den Windows Virtual Desktop-, Citrix-und VMware-Plattformen werden auch Anruf-und Besprechungsfunktionen unterstützt.

Teams in einer virtualisierten Umgebung unterstützen mehrere Konfigurationen. Dazu gehören VDI-, dedizierte, freigegebene, persistente und nicht persistente Modi. Die Features werden kontinuierlich weiterentwickelt und regelmäßig hinzugefügt, und die Funktionalität wird in den nächsten Monaten und Jahren erweitert.

Die Verwendung von Teams in einer virtualisierten Umgebung unterscheidet sich möglicherweise von der Verwendung von Teams in einer nicht virtualisierten Umgebung. Einige erweiterte Funktionen sind in einer virtualisierten Umgebung möglicherweise nicht verfügbar, und die Videoauflösung kann sich unterscheiden.

Befolgen Sie die Anleitungen in diesem Artikel, um eine optimale Benutzererfahrung zu gewährleisten.

> [!Note]
> Details zu den VDI-Teams auf unterschiedlichen Plattformen finden Sie unter [Teams-Features nach Plattform](https://support.microsoft.com/office/teams-features-by-platform-debe7ff4-7db4-4138-b7d0-fcc276f392d3).

## <a name="teams-on-vdi-components"></a>Teams für VDI-Komponenten

Für die Verwendung von Teams in einer virtualisierten Umgebung sind die folgenden Komponenten erforderlich:

- **Virtualization Broker**: die Ressource und der Verbindungs-Manager für den Virtualisierungssoftware-Anbieter, wie Azure
- **Virtueller Desktop**: der VM-Stapel (Virtual Machine), der Microsoft Teams ausführt
- **Thin Client**: der Endpunkt, mit dem der Benutzer physikalisch eine Schnittstelle verwendet
- **Teams-Desktop-App**: die Desktop-Client-App für Teams

## <a name="teams-on-vdi-requirements"></a>Teams für VDI-Anforderungen

### <a name="virtualization-provider-requirements"></a>Anforderungen des Virtualisierungs-Anbieters

Die Desktop-App für Teams wurde mit führenden Anbietern von Virtualisierungslösungen validiert. Bei mehreren Marktanbietern empfehlen wir, dass Sie sich an Ihren Anbieter von Virtualisierungslösungen wenden, um sicherzustellen, dass Sie die Mindestanforderungen erfüllen.
  
Derzeit sind Teams auf VDI mit Audio/Video (AV)-Optimierung mit Windows Virtual Desktop, Citrix und VMware zertifiziert. Überprüfen Sie die Informationen in diesem Abschnitt, um sicherzustellen, dass Sie alle Anforderungen für die ordnungsgemäße Funktionalität erfüllen.

### <a name="platforms-certified-for-teams"></a>Für Teams zertifizierte Plattformen

Die folgenden Plattformen verfügen über virtuelle Desktopinfrastruktur Lösungen für Teams.

|Plattform|Lösung|
|----|---|
|![Das Logo, das Microsoft darstellt](media/microsoft-logo.png)| <a href="https://docs.microsoft.com/azure/virtual-desktop/teams-on-wvd" target="_blank">Virtueller Windows-Desktop</a> |
|![Das Logo, das Citrix darstellt](media/citrix-logo.png)| <a href="https://www.citrix.com/products/citrix-virtual-apps-and-desktops/" target="_blank">Virtuelle Citrix-apps und-Desktops</a> |
|![Das Logo, das VMware darstellt](media/vmware-logo.png)| <a href="https://www.vmware.com/products/horizon.html" target="_blank">VMware Horizon</a> |

### <a name="windows-virtual-desktop"></a>Virtueller Windows-Desktop

Der virtuelle Windows-Desktop bietet AV-Optimierung für Teams auf VDI. Weitere Informationen zu den Anforderungen und zur Installation finden Sie unter [Verwenden von Teams auf dem virtuellen Windows-Desktop](https://docs.microsoft.com/azure/virtual-desktop/teams-on-wvd).

### <a name="citrix-virtual-apps-and-desktops-requirements"></a>Voraussetzungen für virtuelle Citrix-apps und-Desktops

Citrix-Virtual-apps und-Desktops (ehemals XenApp und XenDesktop) bieten AV-Optimierung für Teams auf VDI. Mit virtuellen Citrix-apps und-Desktops unterstützt Teams auf VDI neben Chat und Zusammenarbeit auch Anruf-und Besprechungsfunktionen.

Sie können die aktuelle Version der virtuellen Citrix-apps und-Desktops auf [der Citrix](https://www.citrix.com/downloads/citrix-virtual-apps-and-desktops/)-Download Website herunterladen. (Sie müssen sich zuerst anmelden.) Die erforderlichen Komponenten werden standardmäßig in die [Citrix Workspace-app (GAV)](https://www.citrix.com/downloads/workspace-app/) und den Virtual Delivery Agent (VDA) gebündelt. Sie müssen keine weiteren Komponenten oder Plugins auf der Gewerkschafts-oder VDA-Karte installieren.

Die neuesten Server-und Clientanforderungen finden Sie auf [dieser Citrix-Website](https://docs.citrix.com/en-us/citrix-virtual-apps-desktops/multimedia/opt-ms-teams.html).

### <a name="vmware-horizon-workspace-and-desktop-requirements"></a>VMware Horizon-Arbeitsbereichs-und Desktop Anforderungen

VMware Horizon ist eine moderne Plattform für die sichere Bereitstellung virtueller Desktops und apps in der Hybrid-Cloud. Um eine großartige Benutzererfahrung zu bieten, bietet VMware Horizon Medienoptimierung für Teams. Diese Optimierung verbessert die Gesamtproduktivität für virtuelle Desktops und apps und verbessert die Benutzerfreundlichkeit beim anrufen und Besprechungen mithilfe von Teams.

Sie können die aktuelle Version von VMware Horizon über die Seite [VMware Downloads](https://my.vmware.com/web/vmware/downloads/#all_products) herunterladen. Die erforderlichen Medien Optimierungs Komponenten sind standardmäßig Teil des Horizon-Agents und des Horizon-Clients, und es ist nicht erforderlich, zusätzliches Plug-in zu installieren, um die Optimierungsfunktion für Teams zu verwenden.

Wenn Sie die neuesten Anforderungen und Anleitungen zum Konfigurieren der Medienoptimierung für Teams erhalten möchten, lesen Sie [Diese VMware-Website](https://docs.vmware.com/en/VMware-Horizon/2006/horizon-remote-desktop-features/GUID-F68FA7BB-B08F-4EFF-9BB1-1F9FC71F8214.html).

## <a name="install-or-update-the-teams-desktop-app-on-vdi"></a>Installieren oder Aktualisieren der Desktop-App "Teams" auf VDI

Sie können die Desktop-App "Teams" für VDI mithilfe einer pro-Computer-Installation oder einer Einzelbenutzerinstallation mithilfe des MSI-Pakets bereitstellen. Die Entscheidung, welcher Ansatz zu verwenden ist, hängt davon ab, ob Sie eine dauerhafte oder nicht beständige Einrichtung und die zugehörigen Funktionsanforderungen Ihrer Organisation verwenden.

Für eine dedizierte, dauerhafte Einrichtung würde jeder Ansatz funktionieren. Für eine nicht persistente Einrichtung erfordert Teams jedoch eine Installation pro Computer, um effizient arbeiten zu können. Weitere Informationen finden Sie im Abschnitt " [nicht persistente Einrichtung](#non-persistent-setup) ".

Bei der Installation pro Computer sind die automatischen Updates deaktiviert. Dies bedeutet, dass Sie zum Aktualisieren der Teams-APP die aktuelle Version deinstallieren müssen, um Sie auf eine neuere Version zu aktualisieren. Bei der Installation pro Benutzer sind die automatischen Updates aktiviert. Für die meisten VDI-Bereitstellungen empfehlen wir die Bereitstellung von Teams mithilfe der Installation pro Computer.

Wenn Sie auf die neueste Version von Teams aktualisieren möchten, beginnen Sie mit dem Deinstallationsverfahren, gefolgt von der neuesten Version der Teams-Bereitstellung.

Damit die AV-Optimierung von Teams in VDI-Umgebungen ordnungsgemäß funktioniert, muss der Thin Client-Endpunkt Zugriff auf das Internet haben. Wenn Internetzugriff am Thin Client-Endpunkt nicht zur Verfügung steht, ist der Optimierungs Start nicht erfolgreich. Dies bedeutet, dass sich der Benutzer in einem nicht optimierten Medien Zustand befindet.

#### <a name="dedicated-persistent-setup"></a>Dedizierte permanente Einrichtung

Bei einer dedizierten permanenten Einrichtung werden die Änderungen des lokalen Betriebssystems des Benutzers beibehalten, nachdem sich die Benutzer abgemeldet haben. Für das dauerhafte Setup unterstützt Teams die Installation pro Benutzer und pro Computer.

Es folgt die empfohlene minimale VM-Konfiguration.

|Parameter  |Workstation-Betriebssystem  |Server-Betriebssystem  |
|---------|---------|---------|
|vCPU   |    2 Kerne     |  4, 6 oder 8<br>Es ist wichtig, die zugrunde liegende NUMA-Konfiguration (Non-Uniform Memory Access) zu verstehen und ihre VMs entsprechend zu konfigurieren.     |
|RAM     |   4 GB      | 512 bis 1024 MB pro Benutzer        |
|Speicher    | 8 GB        | 40 bis 60 GB        |

#### <a name="non-persistent-setup"></a>Nicht beständiges Setup

Bei einem nicht persistenten Setup werden die Änderungen des lokalen Betriebssystems des Benutzers nicht beibehalten, nachdem sich die Benutzer abgemeldet haben. Bei solchen Setups handelt es sich um häufig freigegebene mehr Benutzersitzungen. Die VM-Konfiguration variiert je nach der Anzahl der Benutzer und den verfügbaren physikalischen Feld Ressourcen.

Bei einem nicht persistenten Setup muss die Team-Desktop-App pro Computer auf das goldene Bild installiert werden. (Weitere Informationen finden Sie unter [installieren oder Aktualisieren der Desktop-App "Teams" im](#install-or-update-the-teams-desktop-app-on-vdi) Abschnitt "VDI".) Dadurch wird sichergestellt, dass die Teams-APP während einer Benutzersitzung effizient gestartet wird.

Für die Verwendung von Teams mit einem nicht beständigen Setup ist auch ein Profilcache-Manager für eine effiziente Team Laufzeit-Datensynchronisierung erforderlich. Dadurch wird sichergestellt, dass die entsprechenden benutzerspezifischen Informationen (beispielsweise Benutzerdaten, Profil und Einstellungen) während der Benutzersitzung zwischengespeichert werden. Stellen Sie sicher, dass die Daten in diesen beiden Ordnern synchronisiert sind.  

- C:\Users\username\AppData\Local\Microsoft\IdentityCache (%localAppdata%\Microsoft\IdentityCache)
- C:\Users\username\AppData\Roaming\Microsoft\Teams (%appdata%\Microsoft\Teams)

Es stehen verschiedene Caching Manager-Lösungen zur Verfügung. Beispiel: [FSLogix](https://docs.microsoft.com/fslogix/overview). Wenden Sie sich an Ihren Caching Manager-Anbieter, um bestimmte Konfigurationsanweisungen anzuzeigen.

##### <a name="teams-cached-content-exclusion-list-for-non-persistent-setup"></a>Ausschlussliste für in Teams zwischengespeicherte Inhalte für nicht persistente Einrichtung

Schließen Sie im Ordner "Teams-Zwischenspeicherung" Folgendes aus:% APPDATA%/Microsoft/Teams. Wenn Sie diese Elemente ausschließen, können Sie die Größe der Benutzer Zwischenspeicherung reduzieren, um Ihre nicht persistente Einrichtung weiter zu optimieren.

- txt-Dateien
- Ordner "Medien Stapel"
- meeting-addin\Cache (%appdata%\Microsoft\Teams\meeting-addin\Cache)

### <a name="microsoft-365-apps-for-enterprise-considerations"></a>Überlegungen zu Microsoft 365-Apps für Unternehmen

Bedenken Sie beim Bereitstellen von Teams mit Microsoft 365-Apps für Enterprise auf VDI Folgendes:

#### <a name="new-deployments-of-teams-through-microsoft-365-apps-for-enterprise"></a>Neue Bereitstellungen von Teams über Microsoft 365-Apps für Unternehmen

Bevor Sie Teams über Microsoft 365-Apps für Unternehmen bereitstellen, müssen Sie zuerst alle bereits vorhandenen Teams-apps deinstallieren, wenn Sie mithilfe der Installation pro Computer bereitgestellt wurden.

Teams über Microsoft 365-Apps für Unternehmen werden pro Benutzer installiert. Weitere Informationen finden Sie im Abschnitt [installieren oder Aktualisieren der Desktop-App für Teams im VDI](#install-or-update-the-teams-desktop-app-on-vdi) .

#### <a name="teams-deployments-through-microsoft-365-apps-for-enterprise-updates"></a>Teams-Bereitstellungen über Microsoft 365-Apps für Enterprise-Updates

Teams werden auch vorhandenen Installationen von Microsoft 365-Apps für Unternehmen hinzugefügt. Da Microsoft 365-Apps für Enterprise nur Teams pro Benutzer installiert, lesen Sie [installieren oder Aktualisieren der Desktop-App für Teams im VDI](#install-or-update-the-teams-desktop-app-on-vdi) -Abschnitt.

#### <a name="using-teams-with-per-machine-installation-and-microsoft-365-apps-for-enterprise"></a>Verwenden von Teams mit pro-Computer-Installation und Microsoft 365-Apps für Unternehmen

Microsoft 365-Apps für Unternehmen unterstützen keine pro-Computer-Installationen von Teams. Wenn Sie die Installation pro Computer verwenden möchten, müssen Sie Teams aus Microsoft 365-Apps für Unternehmen ausschließen. Weitere Informationen finden Sie unter [Bereitstellen der Desktop-App "Teams" auf dem virtuellen Computer](#deploy-the-teams-desktop-app-to-the-vm) und [ausschließen der Bereitstellung von Teams über Microsoft 365-Apps für Enterprise](#how-to-exclude-teams-deployment-through-microsoft-365-apps-for-enterprise) -Abschnitte.

#### <a name="how-to-exclude-teams-deployment-through-microsoft-365-apps-for-enterprise"></a>Ausschließen der Bereitstellung von Teams über Microsoft 365-Apps für Unternehmen

Weitere Informationen zu Teams und Microsoft 365-Apps für Unternehmen finden Sie unter [Ausschließen von Teams aus neuen Installationen von Microsoft 365-Apps für Unternehmen](https://docs.microsoft.com/DeployOffice/teams-install#how-to-exclude-microsoft-teams-from-new-installations-of-office-365-proplus) und [Verwenden von Gruppenrichtlinien zum Steuern der Installation von Teams](https://docs.microsoft.com/DeployOffice/teams-install#use-group-policy-to-control-the-installation-of-microsoft-teams).

### <a name="deploy-the-teams-desktop-app-to-the-vm"></a>Bereitstellen der Desktop-App "Teams" auf dem virtuellen Computer

1. Laden Sie das MSI-Paket für Teams, das Ihrem VDI-VM-Betriebssystem entspricht, mit einem der folgenden Links herunter:

    - [32-Bit-Version](https://teams.microsoft.com/downloads/desktopurl?env=production&plat=windows&managedInstaller=true&download=true)
    - [64-Bit-Version](https://teams.microsoft.com/downloads/desktopurl?env=production&plat=windows&arch=x64&managedInstaller=true&download=true)

    > [!NOTE]
    > Informationen zu öffentlichen Clouds finden Sie unter [Installieren von Microsoft Teams mit Microsoft Endpoint Configuration Manager](msi-deployment.md) für die Download Links zu den MSI-Dateien.

    Die Mindestversion der Desktop-App für Teams, die erforderlich ist, ist Version 1.3.00.4461. (PSTN-Haltebereich wird in früheren Versionen nicht unterstützt.)

2. Installieren Sie die MSI-Karte auf der VDI-VM, indem Sie einen der folgenden Befehle ausführen:

    - Benutzerspezifische Installation (Standard)
  
        ```console
        msiexec /i <path_to_msi> /l*v <install_logfile_name> ALLUSERS=1
        ```

        Bei diesem Prozess handelt es sich um die Standardinstallation, mit der Teams im Benutzerordner% APPDATA% installiert werden. An diesem Punkt ist die Einrichtung des „Golden Image“ abgeschlossen. Teams funktionieren nicht ordnungsgemäß mit der Installation pro Benutzer bei einem nicht persistenten Setup.

    - Installation pro Computer

        ```console
        msiexec /i <path_to_msi> /l*v <install_logfile_name> ALLUSER=1 ALLUSERS=1
        ```

        Durch diesen Vorgang werden Teams im Programmdateien (x86)-Ordner auf einem 64-Bit-Betriebssystem und im Ordner "Programme" auf einem 32-Bit-Betriebssystem installiert. An diesem Punkt ist die Einrichtung des „Golden Image“ abgeschlossen. Für nicht persistente Setups ist die Installation von Teams pro Computer erforderlich.

        Bei der nächsten interaktiven Anmeldesitzung startet Teams und fordert Anmeldeinformationen an.

        > [!NOTE]
        > In diesen Beispielen wird auch der **ALLUSERS = 1** -Parameter verwendet. Wenn Sie diesen Parameter festlegen, wird das Installationsprogramm für die computerweite Installation von Teams unter "Programme und Features" in der Systemsteuerung sowie unter "Apps und Features" in den Windows-Einstellungen für alle Benutzer des Computers angezeigt. Alle Benutzer können dann Teams deinstallieren, wenn Sie über Administratoranmeldeinformationen verfügen.
        Es ist wichtig, den Unterschied zwischen **ALLUSERS = 1** und **alluser = 1** zu verstehen. Der **ALLUSERS = 1** -Parameter kann in nicht-VDI-und VDI-Umgebungen verwendet werden, während der **alluser = 1** -Parameter nur in VDI-Umgebungen verwendet wird, um eine pro-Computer-Installation festzulegen.

3. Deinstallieren Sie die MSI-Karte aus der VDI-VM. Es gibt zwei Möglichkeiten, Teams zu deinstallieren.

    - PowerShell-Skript: Sie können [dieses PowerShell-Skript](scripts/powershell-script-deployment-cleanup.md) verwenden, um Teams zu deinstallieren und den Ordner "Teams" für einen Benutzer zu entfernen. Führen Sie das Skript für jedes Benutzerprofil aus, auf dem Teams auf dem Computer installiert wurden.
    - Befehlszeile: führen Sie den folgenden Befehl aus.
  
      ```console
      msiexec /passive /x <path_to_msi> /l*v <uninstall_logfile_name>
      ```

      Dieser Prozess deinstalliert Teams aus dem Ordner "Programmdateien (x86)" oder "Programmdateien", je nach Betriebssystemumgebung.

## <a name="teams-on-vdi-performance-considerations"></a>Teams zu VDI-Leistungsüberlegungen

Es gibt eine Reihe von virtualisierten Setup Konfigurationen, die jeweils einen anderen Fokus für die Optimierung aufweisen. Eine Konfiguration kann sich beispielsweise auf die Benutzerdichte konzentrieren. Bei der Planung sollten Sie die folgenden Schritte Unternehmen, um Ihre Einrichtung auf der Grundlage der Arbeits Auslastungsanforderungen Ihrer Organisation zu optimieren.

- Mindestanforderung: einige Arbeitsauslastungen erfordern möglicherweise ein Setup mit Ressourcen, die über den Mindestanforderungen liegen. Beispielsweise Arbeitslasten für Entwickler, die Anwendungen verwenden, die mehr Computing-Ressourcen erfordern.
- Abhängigkeiten: dazu gehören Abhängigkeiten von Infrastruktur, Arbeitsauslastung und anderen Umgebungs Überlegungen außerhalb der Desktop-App von Teams.
- Deaktivierte Features in VDI: Teams deaktiviert GPU-intensive Features für VDI, wodurch die transiente CPU-Auslastung verbessert werden kann. Die folgenden Features sind deaktiviert:
    - Teams-CSS-Animation
    - Giphy Auto-Start

## <a name="teams-on-vdi-with-calling-and-meetings"></a>Teams auf VDI mit anrufen und Besprechungen

Neben Chat und Zusammenarbeit sind auch Teams auf VDI mit anrufen und Besprechungen mit unterstützten ANBIETERPLATTFORMEN für Virtualisierung verfügbar. Unterstützte Features basieren auf der Implementierung des WebRTC-Medien Stapels und des Virtualisierungs-Anbieters. Das folgende Diagramm bietet eine Übersicht über die Architektur.

![Diagramm mit Teams zur VDI-Architektur](media/teams-on-vdi-architecture.png)

> [!IMPORTANT]
> Wenn Sie derzeit Teams ohne AV-Optimierung in VDI ausführen und Features verwenden, die noch nicht für die Optimierung unterstützt werden (wie die Steuerung von übernehmen bei der APP-Freigabe), müssen Sie die Virtualisierungs-Anbieterrichtlinien so festlegen, dass die Umleitung von Teams deaktiviert wird. Das bedeutet, dass die Media-Sitzungen von Teams nicht optimiert werden. Eine schrittweise Anleitung zum Einrichten von Richtlinien zum Deaktivieren der Team Umleitung erhalten Sie von Ihrem Virtualisierungs-Anbieter.

### <a name="network-requirements"></a>Netzwerkanforderungen

Wir empfehlen, dass Sie Ihre Umgebung bewerten, um Risiken und Anforderungen zu identifizieren, die sich auf die gesamte Cloud-sprach-und Videobereitstellung auswirken können. Verwenden Sie das [Skype for Business-Netzwerk Bewertungs Tool](https://www.microsoft.com/download/details.aspx?id=53885) , um zu testen, ob Ihr Netzwerk für Teams bereit ist.

Weitere Informationen dazu, wie Sie Ihr Netzwerk für Teams vorbereiten, finden Sie unter [Vorbereiten des Netzwerks Ihrer Organisation für Teams](prepare-network.md).

### <a name="migrate-from-skype-for-business-on-vdi-to-teams-on-vdi"></a>Migrieren von Skype for Business auf VDI zu Teams auf VDI

Wenn Sie von Skype for Business auf VDI zu Teams auf VDI migrieren, gibt es neben den Unterschieden zwischen den beiden Anwendungen einige Unterschiede, wenn VDI ebenfalls implementiert wird. Einige Funktionen, die derzeit in den VDI-Teams von Skype for Business nicht unterstützt werden, sind wie folgt:

- Plattformspezifische Richtlinie zum Deaktivieren einiger AV-Features in VDI
- Geben und übernehmen der Steuerung bei der APP-Freigabe
- Bildschirmfreigabe aus Chat ohne Audio
- Gleichzeitiges Senden und empfangen von Video-und Bildschirm Freigaben

### <a name="teams-on-chrome-browser-versus-teams-desktop-app-for-vdi"></a>Teams im Chrome-Browser versus Teams-Desktop-App für VDI

Teams im Chrome-Browser bieten keinen Ersatz für die Desktop-App "Teams" für VDI mit AV-Optimierung. Die Chat-und Zusammenarbeits Erfahrung funktioniert wie erwartet. Wenn Medien benötigt werden, gibt es einige Erfahrungen, die möglicherweise die Erwartungen der Benutzer im Chrome-Browser nicht erfüllen:

- Die Audio-und Video-Streaming-Funktionalität ist möglicherweise nicht optimal. Benutzer können Verzögerungen oder geringere Qualität erleben.
- Geräteeinstellungen stehen in den Browsereinstellungen nicht zur Verfügung.
- Die Geräteverwaltung wird über den Browser verarbeitet und erfordert mehrere Einstellungen in den Browser Websiteeinstellungen.
- Geräteeinstellungen müssen möglicherweise auch in der Windows-Geräteverwaltung eingestellt werden.

## <a name="teams-on-vdi-with-chat-and-collaboration"></a>Teams auf VDI mit Chat und Zusammenarbeit

Wenn Ihre Organisation nur Chat-und Zusammenarbeitsfeatures in Teams verwenden möchte, können Sie Richtlinien auf Benutzerebene festlegen, um Anruf-und Besprechungsfunktionen in Teams zu deaktivieren. 

### <a name="set-policies-to-turn-off-calling-and-meeting-functionality"></a>Einrichten von Richtlinien zum Deaktivieren von Anruf-und Besprechungsfunktionen

Sie können Richtlinien mit dem Microsoft Teams Admin Center oder mit PowerShell einrichten. Es kann einige Zeit dauern (einige Stunden), bis die Richtlinienänderungen übertragen werden. Wenn Änderungen für ein bestimmtes Konto nicht sofort angezeigt werden, versuchen Sie es in ein paar Stunden noch einmal.

[**Anruf**](teams-calling-policy.md)Richtlinien: Teams umfasst die integrierte DisallowCalling-Anrufrichtlinie, in der alle Anruffunktionen deaktiviert sind. Weisen Sie die DisallowCalling-Richtlinie allen Benutzern in Ihrer Organisation zu, die Teams in einer virtualisierten Umgebung verwenden.

[**Besprechungsrichtlinien**](meeting-policies-in-teams.md): Teams umfasst die integrierte AllOff-Besprechungsrichtlinie, in der alle besprechungsfeatures deaktiviert sind. Weisen Sie die AllOff-Richtlinie allen Benutzern in Ihrer Organisation zu, die Teams in einer virtualisierten Umgebung verwenden.

#### <a name="assign-policies-using-the-microsoft-teams-admin-center"></a>Zuweisen von Richtlinien mithilfe des Microsoft Teams admin Centers

So weisen Sie einem Benutzer die DisallowCalling-Anrufrichtlinie und die AllOff-Besprechungsrichtlinie zu:

1. Wechseln Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu **Benutzer**.
2. Wählen Sie den Nutzer aus, indem Sie links neben den Nutzernamen klicken, und klicken Sie dann auf **Einstellungen bearbeiten**.
3. Gehen Sie folgendermaßen vor:
    1.  Klicken Sie unter **Anrufrichtlinie** auf **DisallowCalling**.
    2.  Klicken Sie unter **Besprechungsrichtlinie** auf **AllOff**.
4. Klicken Sie auf **Anwenden**.

So weisen Sie mehreren Benutzern gleichzeitig eine Richtlinie zu

1. Wechseln Sie in der linken Navigation des Microsoft Teams Admin Center zu **Benutzer**, und suchen Sie dann nach den gewünschten Benutzern, oder filtern Sie die Ansicht, um die gewünschten Benutzer anzuzeigen.
2. Wählen Sie in der Spalte **&#x2713;** (Häkchen) die Benutzer aus. Um alle Benutzer auszuwählen, klicken Sie am oberen Rand der Tabelle auf &#x2713; (Häkchen).
3. Klicken Sie auf **Einstellungen bearbeiten**, nehmen Sie die gewünschten Änderungen vor, und klicken Sie dann auf **Übernehmen**.

Sie können auch die folgenden Schritte ausführen:

1. Wechseln Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu der Richtlinie, die Sie zuweisen möchten. Beispiel:
    - Wechseln Sie zu **VoIP**-  >  **Anruf Richtlinien**, und klicken Sie dann auf **DisallowCalling**.
    - Wechseln Sie zu den Besprechungsrichtlinien für **Besprechungen**  >  **Meeting policies**, und klicken Sie dann auf **AllOff**.
2. Wählen Sie **Nutzer verwalten** aus.
3. Suchen Sie im Bereich **Nutzer verwalten** anhand des Anzeigenamens oder des Nutzernamens nach dem Nutzer, wählen Sie den Namen und dann **Hinzufügen** aus. Wiederholen Sie diesen Schritt für jeden Nutzer, den Sie hinzufügen möchten.
4. Wenn Sie alle gewünschten Benutzer hinzugefügt haben, klicken Sie auf **Speichern**.

#### <a name="assign-policies-using-powershell"></a>Zuweisen von Richtlinien mithilfe von PowerShell

Im folgenden Beispiel wird gezeigt, wie Sie mit dem [Grant-CsTeamsCallingPolicy](https://docs.microsoft.com/powershell/module/skype/grant-csteamscallingpolicy) die DisallowCalling-Anrufrichtlinie einem Benutzer zuweisen.

```PowerShell
Grant-CsTeamsCallingPolicy -PolicyName DisallowCalling -Identity "user email id"
```

Weitere Informationen zum Verwenden von PowerShell zum Verwalten von Anruf Richtlinien finden Sie unter [CsTeamsCallingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamscallingpolicy).

Im folgenden Beispiel wird gezeigt, wie Sie mit dem [Grant-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/grant-csteamsmeetingpolicy) die AllOff-Besprechungsrichtlinie einem Benutzer zuweisen.

```PowerShell
Grant-CsTeamsMeetingPolicy -PolicyName AllOff -Identity "user email id"
```

Weitere Informationen zum Verwenden von PowerShell zum Verwalten von Besprechungsrichtlinien finden Sie unter [Satz-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy).

## <a name="migrate-teams-on-vdi-with-chat-and-collaboration-to-optimize-teams-with-calling-and-meetings"></a>Migrieren von Teams auf VDI durch Chat und Zusammenarbeit zur Optimierung von Teams mit anrufen und Besprechungen

Wenn Sie über eine vorhandene Implementierung von Teams auf VDI mit Chat und Zusammenarbeit verfügen, bei denen Sie Richtlinien auf Benutzerebene zum Deaktivieren von Anruf-und Besprechungsfunktionen eingerichtet haben und Sie zu Teams mit AV-Optimierung migrieren, müssen Sie Richtlinien für die Aktivierung von Anruf-und Besprechungsfunktionen für diese Teams für VDI-Benutzer einrichten.

### <a name="set-policies-to-turn-on-calling-and-meeting-functionality"></a>Einrichten von Richtlinien zum Aktivieren von Anruf-und Besprechungsfunktionen

Sie können das Microsoft Teams Admin Center oder PowerShell verwenden, um Ihren Benutzern Anruf-und Besprechungsrichtlinien zu definieren und zuzuweisen. Es kann einige Zeit dauern (einige Stunden), bis Richtlinienänderungen übertragen werden. Wenn Änderungen für ein bestimmtes Konto nicht sofort angezeigt werden, versuchen Sie es nach ein paar Stunden noch einmal.

[**Anrufen von Policen**](teams-calling-policy.md): durch das Aufrufen von Richtlinien in Teams wird gesteuert, welche Anruffeatures für Benutzer verfügbar sind. Teams umfasst die integrierte AllowCalling-Anrufrichtlinie, in der alle Anruffunktionen aktiviert sind. Wenn Sie alle Anruffeatures aktivieren möchten, weisen Sie die AllowCalling-Richtlinie zu. Oder erstellen Sie eine benutzerdefinierte Anrufrichtlinie, um die gewünschten Anruffeatures zu aktivieren und Benutzern zuzuweisen. 

[**Besprechungsrichtlinien**](meeting-policies-in-teams.md): Besprechungsrichtlinien in Teams steuern die Typen von Besprechungen, die von Benutzern erstellt werden können, und die Features, die für Besprechungsteilnehmer verfügbar sind, die von Benutzern in Ihrer Organisation geplant werden. Teams umfasst die integrierte Allon-Besprechungsrichtlinie, in der alle besprechungsfeatures aktiviert sind. Wenn Sie alle besprechungsfeatures aktivieren möchten, weisen Sie die Allon-Richtlinie zu. Oder erstellen Sie eine benutzerdefinierte Besprechungsrichtlinie, um die gewünschten besprechungsfeatures zu aktivieren und Benutzern zuzuweisen.

#### <a name="assign-policies-using-the-microsoft-teams-admin-center"></a>Zuweisen von Richtlinien mithilfe des Microsoft Teams admin Centers

So weisen Sie einem Benutzer die AllowCalling-Anrufrichtlinie und die Allon-Besprechungsrichtlinie zu:

1. Wechseln Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu **Benutzer**.
2. Wählen Sie den Nutzer aus, indem Sie links neben den Nutzernamen klicken, und klicken Sie dann auf **Einstellungen bearbeiten**.
3. Gehen Sie folgendermaßen vor:
    1.  Klicken Sie unter **Anrufrichtlinie** auf **AllowCalling**.
    2.  Klicken Sie unter **Besprechungsrichtlinie** auf **Allon**.
4. Klicken Sie auf **Anwenden**.

So weisen Sie mehreren Benutzern gleichzeitig eine Richtlinie zu

1. Wechseln Sie in der linken Navigation des Microsoft Teams Admin Center zu **Benutzer**, und suchen Sie dann nach den gewünschten Benutzern, oder filtern Sie die Ansicht, um die gewünschten Benutzer anzuzeigen.
2. Wählen Sie in der Spalte **&#x2713;** (Häkchen) die Benutzer aus. Wenn Sie alle Benutzer auswählen möchten, klicken Sie oben in der Tabelle auf das **&#x2713;** (Häkchen).
3. Klicken Sie auf **Einstellungen bearbeiten**, nehmen Sie die gewünschten Änderungen vor, und klicken Sie dann auf **Übernehmen**.

Sie können auch die folgenden Schritte ausführen:

1. Wechseln Sie in der linken Navigationsleiste des Microsoft Teams Admin Center zu der Richtlinie, die Sie zuweisen möchten. Beispiel:
    - Wechseln Sie zu **VoIP**-  >  **Anruf Richtlinien**, und klicken Sie dann auf **AllowCalling**.
    - Wechseln Sie zu den Besprechungsrichtlinien für **Besprechungen**  >  **Meeting policies**, und klicken Sie dann auf **Allon**.
2. Wählen Sie **Nutzer verwalten** aus.
3. Suchen Sie im Bereich **Nutzer verwalten** anhand des Anzeigenamens oder des Nutzernamens nach dem Nutzer, wählen Sie den Namen und dann **Hinzufügen** aus. Wiederholen Sie diesen Schritt für jeden Nutzer, den Sie hinzufügen möchten.
4. Wenn Sie alle gewünschten Benutzer hinzugefügt haben, klicken Sie auf **Speichern**.

#### <a name="assign-policies-using-powershell"></a>Zuweisen von Richtlinien mithilfe von PowerShell

Im folgenden Beispiel wird gezeigt, wie Sie mit dem [Grant-CsTeamsCallingPolicy](https://docs.microsoft.com/powershell/module/skype/grant-csteamscallingpolicy) die AllowCalling-Anrufrichtlinie einem Benutzer zuweisen.

```PowerShell
Grant-CsTeamsCallingPolicy -PolicyName AllowCalling -Identity "user email id"
```

Weitere Informationen zum Verwenden von PowerShell zum Verwalten von Anruf Richtlinien finden Sie unter [CsTeamsCallingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamscallingpolicy).

Im folgenden Beispiel wird gezeigt, wie Sie den [Grant-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/grant-csteamsmeetingpolicy) verwenden, um die Allon-Besprechungsrichtlinie einem Benutzer zuzuweisen.

```PowerShell
Grant-CsTeamsMeetingPolicy -PolicyName AllOn -Identity "user email id"
```

Weitere Informationen zum Verwenden von PowerShell zum Verwalten von Besprechungsrichtlinien finden Sie unter [Satz-CsTeamsMeetingPolicy](https://docs.microsoft.com/powershell/module/skype/set-csteamsmeetingpolicy).

## <a name="control-fallback-mode-in-teams"></a>Steuern des Fall Back Modus in Teams

Wenn Benutzer eine Verbindung mit einem nicht unterstützten Endpunkt herstellen, befinden sich die Benutzer im Fallbackmodus, in dem AV nicht optimiert ist. Sie können den Fall Back Modus deaktivieren oder aktivieren, indem Sie einen der folgenden DWORD-Registrierungswerte festlegen:

- HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Teams\DisableFallback
- HKEY_CURRENT_USER\SOFTWARE\Microsoft\Office\Teams\DisableFallback

Um den Fall Back Modus zu deaktivieren, setzen Sie den Wert auf **1**. Wenn Sie nur Audio aktivieren möchten, setzen Sie den Wert auf **2**. Wenn der Wert nicht vorhanden ist oder auf **0** (null) eingestellt ist, ist der Fall Back Modus aktiviert.

Dieses Feature ist in den Teams Version 1.3.00.13565 und höher verfügbar.

## <a name="known-issues-and-limitations"></a>Bekannte Probleme und Einschränkungen

### <a name="client-deployment-installation-and-setup"></a>Client Bereitstellung,-Installation und-Setup

- Bei der Installation pro Computer werden die Teams für VDI nicht automatisch so aktualisiert, wie es Clients außerhalb der VDI-Teams sind. Sie müssen das VM-Abbild aktualisieren, indem Sie eine neue MSI-Datei installieren, wie im Abschnitt [installieren oder Aktualisieren der Desktop-App "Teams" im VDI](#install-or-update-the-teams-desktop-app-on-vdi) -Abschnitt beschrieben. Sie müssen die aktuelle Version deinstallieren, um Sie auf eine neuere Version zu aktualisieren.
- Teams sollten entweder pro Benutzer oder pro Computer bereitgestellt werden. Die Bereitstellung von Teams für Concurrent pro Benutzer und pro Computer wird nicht unterstützt. Wenn Sie von einem einzelnen Computer oder pro Benutzer zu einem dieser Modi migrieren möchten, folgen Sie dem Deinstallationsverfahren, und stellen Sie den jeweiligen Modus erneut bereit.
- Windows Virtual Desktop und VMware unterstützen zurzeit keine MacOS-und Linux-basierten Clients.
- Citrix unterstützt derzeit keine MacOS-Clients.
- Citrix unterstützt nicht die Verwendung von expliziten HTTP-Proxys, die für einen Endpunkt definiert sind.

### <a name="calling-and-meetings"></a>Anrufe und Besprechungen

Die folgenden Anruf-und besprechungsfeatures werden nicht unterstützt:

- Erweiterte Notfalldienste
- HID-Schaltflächen und LED-Steuerungen zwischen der Teams-APP und Geräten
- Hintergrund Unschärfe und Effekte
- Rollen für Broadcast-und Live-Event Producer und Referenten
- Location-Based-Routing (LBR)
- Anruf parken
- Anrufwarteschlange
- Audio/Computer-Sound für Shared System
- Medienumgehung für direkte Weiterleitung

> [!NOTE]
> Wir arbeiten daran, Anruf-und Besprechungsfunktionen hinzuzufügen, die derzeit nur in nicht-VDI-Umgebungen verfügbar sind. Dazu gehören möglicherweise mehr Administrator Kontrolle über die Qualität, zusätzliche Szenarien für die Bildschirmfreigabe und erweiterte Features, die kürzlich zu Teams hinzugefügt wurden. Wenden Sie sich an Ihren Teams-Mitarbeiter, um mehr über bevorstehende Funktionen zu erfahren.

Im folgenden sind bekannte Probleme und Einschränkungen für Anrufe und Besprechungen zu finden:

- Die Interoperabilität mit Skype for Business ist auf Audio-Anrufe limitiert; Es gibt keine Video Modalitäten.
- Nur ein einzelner eingehender Videostream wird in Besprechungen oder Gruppen anrufen unterstützt. Wenn mehrere Personen Video senden, wird nur das Video des dominanten Sprechers zu einem bestimmten Zeitpunkt angezeigt.
- Die Auflösung des eingehenden und ausgehenden Videostroms ist auf 720p-Auflösung limitiert. Hierbei handelt es sich um eine WebRTC-Einschränkung.
- Es wird nur ein Videostream von einer eingehenden Kamera oder einem Bildschirmfreigabe Datenstrom unterstützt. Wenn eine eingehende Bildschirmfreigabe vorhanden ist, wird diese Bildschirmfreigabe anstelle des Videos des dominanten Sprechers angezeigt.
- Teams wechseln nicht, um das letzte Audiogerät zu verwenden, das ein Benutzer ausgewählt hat, wenn das Gerät getrennt ist, und dann wieder verbunden.
- Ausgehende Bildschirmübertragung:
    - Die Anwendungsfreigabe wird nicht unterstützt.
- Kontrolle und Kontrolle übernehmen:
    - Wird während einer Bildschirmfreigabe-oder Anwendungsfreigabesitzung nicht unterstützt.
    - Wird während einer PowerPoint-Freigabesitzung unterstützt.
- Nur Citrix-Einschränkungen
    - Wenn die Bildschirmübertragung in einer Multi-Monitor-Einrichtung erfolgt, wird nur der Hauptmonitor freigegeben.
    - Eine große DPI-Skalierung auf "GAV" wird nicht unterstützt.

Informationen zu bekannten Problemen, die nicht mit VDI in Verbindung stehen, finden Sie unter [Support Teams in Ihrer Organisation](Known-issues.md).

## <a name="troubleshooting"></a>Problembehandlung

### <a name="troubleshoot-citrix-components"></a>Problembehandlung bei Citrix-Komponenten

#### <a name="teams-crashes-or-the-teams-sign-in-screen-is-blank"></a>Teams stürzt ab, oder der Anmeldebildschirm für Teams ist leer

Dies ist ein bekanntes Problem mit den Citrix VDA-Versionen 1906 und 1909. Um dieses Problem zu umgehen, fügen Sie den folgenden Registrierungs DWORD-Wert hinzu, und setzen Sie ihn auf 204 (hexadezimal).

HKEY_LOCAL_MACHINE\SOFTWARE\Citrix\CtxHook\AppInit_Dlls\SfrHook\Teams.exe

Starten Sie dann VDA neu. Weitere Informationen finden Sie in diesem Citrix Support Artikel zur [Problembehandlung bei der HDX-Optimierung für Teams](https://support.citrix.com/article/CTX253754).

## <a name="related-topics"></a>Verwandte Themen

- [Installieren von Microsoft Teams mithilfe eines MSI-Pakets](msi-deployment.md)
- [Übersicht über PowerShell für Microsoft Teams](teams-powershell-overview.md)
- [Verwenden von Microsoft Teams auf dem virtuellen Windows-Desktop](https://docs.microsoft.com/azure/virtual-desktop/teams-on-wvd)
