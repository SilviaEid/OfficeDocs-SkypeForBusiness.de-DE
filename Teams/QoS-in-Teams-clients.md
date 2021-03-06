---
title: Implementieren von Quality of Service (QoS) in Microsoft Teams-Clients
author: SerdarSoysal
ms.author: serdars
manager: Serdars
ms.topic: article
ms.service: msteams
ms.reviewer: vkorlep, siunies
audience: admin
description: Erfahren Sie, wie QoS (Quality of Service) zur Optimierung des Netzwerkverkehrs für den Microsoft Teams-Desktop Client verwendet wird.
localization_priority: Normal
search.appverid: MET150
f1.keywords:
- NOCSH
ms.collection:
- M365-collaboration
appliesto:
- Microsoft Teams
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
ms.openlocfilehash: bc352303cf63ea966927aece0aef36854a0ace1b
ms.sourcegitcommit: 4d6bf5c58b2c553dc1df8375ede4a9cb9eaadff2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "48526402"
---
# <a name="implement-quality-of-service-qos-in-microsoft-teams-clients"></a>Implementieren von Quality of Service (QoS) in Microsoft Teams-Clients

Sie können die richtlinienbasierte QoS (Quality of Service) in Gruppenrichtlinien verwenden, um den Quellportbereich für den vordefinierten DSCP-Wert im Teams-Client festzulegen. Die in der folgenden Tabelle angegebenen Portbereiche stellen einen Ausgangspunkt zum Erstellen einer Richtlinie für jede Arbeitsauslastung dar.

*Tabelle 1 Empfohlene anfängliche Portbereiche*

|Typ des Mediendatenverkehrs| Client-Quellportbereich  |Protokoll|DSCP-Wert|DSCP-Klasse|
|:--- |:--- |:--- |:--- |:--- |
|Audio| 50.000–50.019|TCP/UDP|46|Expedited Forwarding (EF)|
|Video| 50.020–50.039|TCP/UDP|34|Assured Forwarding (AF41)|
|Anwendung/Bildschirmfreigabe| 50.040–50.059|TCP/UDP|18|Assured Forwarding (AF21)|
| | | | | |

Konfigurieren Sie, wenn möglich, richtlinienbasierte QoS-Einstellungen in einem Gruppenrichtlinienobjekt. Die folgenden Schritte ähneln dem  [Konfigurieren von Portbereichen und einer Quality of Service-Richtlinie für Ihre Clients in Skype for Business Server](https://docs.microsoft.com/SkypeForBusiness/manage/network-management/qos/configuring-port-ranges-for-your-skype-clients#configure-quality-of-service-policies-for-clients-running-on-windows-10), die einige zusätzliche Details enthält, die möglicherweise nicht erforderlich sind.

Wenn Sie eine QoS-audiorichtlinie für mit der Domäne verbundene Windows 10-Computer erstellen möchten, melden Sie sich zuerst bei einem Computer an, auf dem die Gruppenrichtlinienverwaltung installiert wurde. Öffnen Sie die Gruppenrichtlinienverwaltung (Klicken Sie auf Start, zeigen Sie auf Verwaltung, und klicken Sie dann auf Gruppenrichtlinienverwaltung), und führen Sie dann die folgenden Schritte aus:

1. Suchen Sie in der Gruppenrichtlinienverwaltung nach dem Container, in dem die neue Richtlinie erstellt werden soll. Wenn sich beispielsweise alle Ihre Clientcomputer in einer Organisationseinheit mit dem Namen " **Clients**" befinden, sollte die neue Richtlinie in der Organisationseinheit "Clients" erstellt werden.

1. Klicken Sie mit der rechten Maustaste auf den entsprechenden Container, und klicken Sie dann auf **Gruppenrichtlinienobjekt in dieser Domäne erstellen, und verknüpfen Sie es hier**.

1. Geben Sie im Dialogfeld **neues GPO** im Feld **Name** einen Namen für das neue Gruppenrichtlinienobjekt ein, und klicken Sie dann auf **OK**.

1. Klicken Sie mit der rechten Maustaste auf die neu erstellte Richtlinie, und klicken Sie dann auf **Bearbeiten**.

1. Erweitern Sie im Gruppenrichtlinien-Verwaltungs-Editor **Computer Konfiguration**, erweitern Sie **Windows-Einstellungen**, klicken Sie mit der rechten Maustaste auf **richtlinienbasierte QoS**, und klicken Sie dann auf **neue Richtlinie erstellen**.

1. Geben Sie im Dialogfeld **richtlinienbasierte QoS** auf der Seite öffnen im Feld **Name** einen Namen für die neue Richtlinie ein. Wählen Sie **DSCP-Wert angeben** aus, und legen Sie den Wert auf **46**fest. Geben Sie die **ausgehende Drosselungs Rate** nicht ausgewählt ein, und klicken Sie dann auf **weiter**.

1. Wählen Sie auf der nächsten Seite **nur Anwendungen mit diesem ausführbaren Namen** aus, geben Sie den Namen **Teams.exe**ein, und klicken Sie dann auf **weiter**. Mit dieser Einstellung wird die Richtlinie angewiesen, nur den übereinstimmenden Datenverkehr vom Team-Client zu priorisieren.

1. Stellen Sie auf der dritten Seite sicher, dass sowohl **eine Quell-** als auch **eine beliebige Ziel-IP-Adresse** ausgewählt ist, und klicken Sie dann auf **weiter**. Durch diese beiden Einstellungen wird sichergestellt, dass Pakete unabhängig davon verwaltet werden, auf welchem Computer (IP-Adresse) die Pakete gesendet werden und auf welchem Computer (IP-Adresse) die Pakete empfangen werden.

1. Wählen Sie auf Seite 4 **TCP und UDP** aus der Dropdownliste **Wählen Sie das Protokoll aus, auf das diese QoS-Richtlinie angewendet werden soll** . TCP (Transmission Control Protocol) und UDP (User Datagram Protocol) sind die beiden am häufigsten verwendeten Netzwerkprotokolle.

1. Wählen Sie unter der Überschrift **die Quellportnummer**aus, und wählen Sie **aus diesem Quell Port oder-Bereich aus**. Geben Sie im Feld Begleittext den Portbereich ein, der für Audioübertragungen reserviert ist. Wenn Sie beispielsweise Ports 50000 über Ports 50019 für den Audioverkehr reserviert haben, geben Sie den Portbereich mit folgendem Format ein: **50000:50019**. Klicken Sie auf **Fertig stellen**.

1. Wiederholen Sie die Schritte 5-10, um Richtlinien für die Video-und Anwendungs-und Desktop Freigabe zu erstellen und die entsprechenden Werte in den Schritten 6 und 10 zu ersetzen.

Die neu erstellten Richtlinien werden erst wirksam, nachdem die Gruppenrichtlinien auf Ihren Clientcomputern aktualisiert wurden. Obwohl Gruppenrichtlinien regelmäßig für sich selbst aktualisiert werden, können Sie eine sofortige Aktualisierung erzwingen, indem Sie die folgenden Schritte ausführen:

1. Öffnen Sie auf jedem Computer, für den Sie die Gruppenrichtlinie aktualisieren möchten, eine Eingabeaufforderung als Administrator (*als Administrator ausführen*).

1. Geben Sie an der Eingabeaufforderung Folgendes ein:

   ```console
   gpupdate /force
   ```

## <a name="verify-dscp-markings-in-the-group-policy-object"></a>Überprüfen von DSCP-Markierungen im Gruppenrichtlinienobjekt

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob die Werte aus dem Gruppenrichtlinienobjekt festgesetzt wurden:

1. Öffnen Sie eine Eingabeaufforderung als Administrator (*als Administrator ausführen*).

1. Geben Sie an der Eingabeaufforderung Folgendes ein:

   ```console
   gpresult /R > gp.txt
   ```

   Dadurch wird ein Bericht über angewendete GPOs generiert und an eine Textdatei mit dem Namen *gp.txt*gesendet.

   Geben Sie den folgenden Befehl ein, um einen besser lesbaren HTML-Bericht mit dem Namen *gp.html*zu finden:

   ```console
   gpresult /H gp.html
   ```

1. Suchen Sie in der generierten Datei nach der Überschrift **angewendete Gruppenrichtlinienobjekte** , und überprüfen Sie, ob die Namen der zuvor erstellten Gruppenrichtlinienobjekte in der Liste der angewendeten Richtlinien aufgeführt sind.

1. Öffnen Sie den Registrierungs-Editor, und wechseln Sie zu

   HKEY \_ - \_ Software Richtlinien für lokale Computer \\ \\ \\ Microsoft \\ Windows- \\ QoS

   Überprüfen Sie die Werte für die Registrierungseinträge, die in Tabelle 2 aufgeführt sind.

   *Tabelle 2. Werte für Windows-Registrierungseinträge für QoS*

   |          Name          |  Typ  |    Daten     |
   |         :---:          | :---:  |    :---:    |
   |    Application Name    | REG_SZ |  Teams.exe  |
   |       DSCP Value       | REG_SZ |     46      |
   |        Local IP        | REG_SZ |     \*      |
   | Local IP Prefix Length | REG_SZ |     \*      |
   |       Local Port       | REG_SZ | 50000-50019 |
   |        Protokoll        | REG_SZ |     \*      |
   |       Remote IP        | REG_SZ |     \*      |
   |    Remote-IP-Präfix    | REG_SZ |     \*      |
   |      Remote Port       | REG_SZ |     \*      |
   |     Throttle Rate      | REG_SZ |     -1      |
   | | | |

1. Überprüfen Sie, ob der Wert für den Anwendungsnamen Eintrag für den verwendeten Client richtig ist, und überprüfen Sie, ob der DSCP-Wert und die lokalen Port Einträge die Einstellungen im Gruppenrichtlinienobjekt widerspiegeln.


## <a name="related-topics"></a>Verwandte Themen

[Implementieren von Quality of Service (QoS) in Teams](QoS-in-Teams.md)