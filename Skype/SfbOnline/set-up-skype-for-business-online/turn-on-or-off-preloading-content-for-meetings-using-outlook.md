---
title: Das Vorab-Laden von Inhalten für Besprechungen mit Outlook ein- oder ausschalten
ms.reviewer: ''
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.topic: article
ms.assetid: d217d422-f7e9-433d-ad24-bf41751f65ca
ms.tgt.pltfrm: cloud
ms.service: skype-for-business-online
search.appverid: MET150
ms.collection: Adm_Skype4B_Online
audience: Admin
appliesto:
- Skype for Business
localization_priority: Normal
f1.keywords:
- NOCSH
ms.custom:
- Setup
description: 'Hier erfahren Sie, wie Sie vorab geladene Inhalte für Skype for Business-Besprechungen mithilfe von Dateien oder Anlagen in einer Outlook-Besprechungseinladung aktivieren oder deaktivieren. '
ms.openlocfilehash: 079d0642158aa6d28b3c92a63e77afa0a0024d94
ms.sourcegitcommit: 1a31ff16b8218d30059f15c787e157d06260666f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "47814584"
---
# <a name="turn-on-or-off-allowing-content-to-be-preloaded-for-meetings-using-outlook"></a>Das Vorab-Laden von Inhalten für Besprechungen mit Outlook ein- oder ausschalten

Benutzer können Inhalte, Dateien oder Anlagen, die an eine Outlook-Besprechungseinladung angefügt sind, in eine Skype for Business Online-Besprechung laden, aber Sie können Sie aktivieren oder deaktivieren. Sie ist für alle Organisationen, die Skype for Business Online verwenden, standardmäßig aktiviert. Hier erfahren Sie, wie [Anlagen für eine Skype for Business-Besprechung geladen](https://support.office.com/article/fd3d9f9d-b448-4754-b813-02e49393f251)werden.
  
> [!NOTE]
> Derzeit stehen in Skype for Business Online keine Cmdlets zum Festlegen oder Anzeigen von Online Werten für  _MaxContentStorageMB_ und _MaxUploadFileMB_zur Verfügung. Sie sind nur für Bereitstellungen vor Ort verfügbar. Es ist wichtig zu wissen, dass Inhalte nicht in eine Besprechung hochgeladen werden, wenn die angefügten Inhalte die  _MaxUploadFileSizeMB_ überschreiten oder wenn die _MaxContentStorageMB_ -Grenze erreicht ist.
  
## <a name="to-get-you-started"></a>Erste Schritte

### 

 **Überprüfen, ob Windows PowerShell 3.0 oder höher ausgeführt wird**
  
1. Zur Überprüfung ob Sie Version 3.0 oder höher verwenden: **Start Menu** > **Windows PowerShell**.
    
2. Überprüfen Sie die Version, indem Sie im Fenster _Windows PowerShell_ die Zeichenfolge **Get-Host** eingeben.
    
3. Wenn Sie nicht über Version 3.0 oder eine höhere Version verfügen, müssen Sie Updates für Windows PowerShell herunterladen und installieren. Informationen zum herunterladen und Aktualisieren von Windows PowerShell auf Version 4,0 finden Sie unter [Windows Management Framework 4,0](https://go.microsoft.com/fwlink/?LinkId=716845) . Starten Sie Ihren Computer neu, wenn Sie dazu aufgefordert werden.
    
4. Sie müssen auch das Windows PowerShell-Modul für Skype for Business Online installieren, mit dem Sie eine Windows PowerShell-Remotesitzung erstellen können, die eine Verbindung mit Skype for Business Online herstellt. Dieses Modul, das nur auf 64-Bit-Computern unterstützt wird, kann aus dem Microsoft Download Center unter [Windows PowerShell-Modul für Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=294688) heruntergeladen werden. Starten Sie Ihren Computer neu, wenn Sie dazu aufgefordert werden.
    
Wenn Sie weitere Informationen benötigen, lesen Sie [Herstellen einer Verbindung mit allen Microsoft 365-oder Office 365-Diensten in einem einzigen Windows PowerShell-Fenster](https://technet.microsoft.com/library/dn568015.aspx).
  
### 

 **Starten einer Windows PowerShell-Sitzung**
  
1. Vom **Start Menu** > **Windows PowerShell**.
    
2. Stellen Sie im **Windows PowerShell** -Fenster eine Verbindung mit Ihrem Microsoft 365 oder Office 365 her, indem Sie Folgendes ausführen:
    
> [!NOTE]
> Skype for Business Online Connector ist derzeit Teil des neuesten Teams PowerShell-Moduls.
>
> Wenn Sie die neueste Version von [Teams PowerShell](https://www.powershellgallery.com/packages/MicrosoftTeams/)verwenden, müssen Sie den Skype for Business Online-Connector nicht installieren.
  
```PowerShell
Import-Module -Name MicrosoftTeams
$credential = Get-Credential
$session = New-CsOnlineSession -Credential $credential
Import-PSSession $session
```

Wenn Sie weitere Informationen zum Starten von Windows PowerShell benötigen, lesen Sie [Herstellen einer Verbindung mit allen Microsoft 365-oder Office 365-Diensten in einem einzelnen Windows PowerShell-Fenster](https://technet.microsoft.com/library/dn568015.aspx) oder [Einrichten Ihres Computers für Windows PowerShell](../set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell.md).
  
## <a name="turning-it-on-or-off"></a>Aktivieren oder Deaktivieren dieser Funktion

Die Möglichkeit zum Laden von Inhalten, die an eine Outlook-Besprechungseinladung zu Skype for Business Online-Besprechungen angefügt sind, ist standardmäßig aktiviert, doch müssen Sie möglicherweise verhindern, dass Benutzer in Ihrer Organisation Inhalte in ihren Besprechungen Vorabladen.
  
> [!IMPORTANT]
> Diese Einstellung kann nur für Ihre gesamte Organisation aktiviert oder deaktiviert werden. Sie können die Funktion nicht für einen einzelnen Benutzer aktivieren oder deaktivieren. 
  
 **Um die Funktion zu deaktivieren, öffnen Sie Windows PowerShell und führen Sie die folgenden Schritte aus:**
  
```PowerShell
Grant-CsGraphPolicy -PolicyName GraphDisabled 
```

 **Wenn Sie sie wieder aktivieren möchten, öffnen Sie Windows PowerShell und gehen Sie wie folgt vor:**
  
```PowerShell
Grant-CsGraphPolicy -PolicyName GraphEnabled 
```

## <a name="want-to-know-more-about-windows-powershell"></a>Möchten Sie mehr über Windows PowerShell erfahren?

- Bei Windows PowerShell dreht sich alles um das Verwalten von Benutzern und Funktionen, die Benutzer verwenden oder nicht verwenden können. Mit Windows PowerShell können Sie Microsoft 365 oder Office 365 und Skype for Business Online mit einem zentralen Verwaltungspunkt verwalten, der Ihre tägliche Arbeit vereinfachen kann, wenn mehrere Aufgaben ausgeführt werden müssen. Informieren Sie sich in den folgenden Artikeln über die Verwendung von Windows PowerShell:
    
  - [Einführung in Windows PowerShell und Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525039)
    
  - [Sechs Gründe für die Verwendung von Windows PowerShell zum Verwalten von Microsoft 365 oder Office 365](https://go.microsoft.com/fwlink/?LinkId=525041)
    
- Windows PowerShell bietet zahlreiche Vorteile in Geschwindigkeit, Einfachheit und Produktivität, wenn Sie nur das Microsoft 365 Admin Center verwenden, beispielsweise wenn Sie für viele Benutzer gleichzeitig Einstellungsänderungen vornehmen. Informationen zu diesen Vorteilen finden Sie unter den folgenden Themen:
    
  - [Beste Möglichkeiten zum Verwalten von Microsoft 365 oder Office 365 mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=525142)
    
  - [Verwenden von Windows PowerShell zum Verwalten von Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525453)
    
  - [Verwenden von Windows PowerShell für die Durchführung gängiger Verwaltungsaufgaben von Skype for Business Online](https://go.microsoft.com/fwlink/?LinkId=525038)
    
## <a name="related-topics"></a>Verwandte Themen
[Einrichten von Skype for Business Online](set-up-skype-for-business-online.md)

[Zulassen, dass Skype for Business-Benutzer Skype-Kontakte hinzufügen](let-skype-for-business-users-add-skype-contacts.md)

  
 
