---
title: Zurücksetzen der Audiokonferenz-PIN in Microsoft Teams
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.topic: article
ms.assetid: 67866a47-89c1-4593-8766-3a68777e2be6
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
- M365-voice
- M365-collaboration
audience: Admin
appliesto:
- Microsoft Teams
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Audio Conferencing
- seo-marvel-apr2020
description: Hier erfahren Sie, wie Sie die PIN für die Audiokonferenz eines Benutzers in Microsoft Teams zurücksetzen und wichtige Informationen zu Pins erfahren.
ms.openlocfilehash: 8926218c72c888edb00480ff8382672a3730cf15
ms.sourcegitcommit: f586d2765195dbd5b7cf65615a03a1cb098c5466
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "44666187"
---
# <a name="reset-the-audio-conferencing-pin-in-microsoft-teams"></a>Zurücksetzen der Audiokonferenz-PIN in Microsoft Teams

Eine PIN ist ein aus Zahlen bestehender Code, der für jeden Microsoft Teams-Benutzer erstellt wird, der für Audiokonferenzen aktiviert ist. Besprechungsorganisatoren verwenden Audiokonferenz-PINs, um sich als Besprechungsorganisator auszuweisen und Besprechungen per Telefon zu starten. Wenn der Organisator zum Starten einer Besprechung die Microsoft Teams-App verwendet, ist keine PIN erforderlich. Wenn Benutzer ihre PIN vergessen und sie nicht in der E-Mail finden, die sie bei ihrer Aktivierung für Audiokonferenzen erhalten haben, kann die PIN von einem Administrator zurückgesetzt werden. Die Benutzer können ihre PIN auch selbst zurücksetzen.
  
Besprechungen können gestartet werden, wenn ein authentifizierter Benutzer über die Microsoft Teams-App teilnimmt oder wenn der Organisator per Telefon mit seiner PIN teilnimmt. Wenn die Besprechung zum Starten eine PIN erfordert, werden alle Benutzer, die sich per Telefon einwählen standardmäßig im Wartebereich platziert und hören Warteschleifenmusik, bis die Besprechung beginnt. Wenn der Organisator einer Besprechung keine PIN zum Starten der Besprechung per Telefon benötigt, werden Anrufer nicht nach einer PIN gefragt, wenn sie sich für die Besprechung einwählen.

## <a name="reset-a-users-pin"></a>Zurücksetzen der PIN eines Benutzers

![Ein Symbol mit dem Microsoft Teams-Logo](media/teams-logo-30x30.png) **Verwenden des Microsoft Teams Admin Centers**

1. Klicken Sie in der linken Navigationsleiste auf **Benutzer**, und wählen Sie dann den Benutzer aus der Liste der verfügbaren Benutzer aus.

2. Klicken Sie auf **Bearbeiten**.

3. Klicken Sie unter **Audiokonferenzen**auf **PIN zurücksetzen**.

4. Klicken Sie auf **Zurücksetzen**.
 
> [!Note]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]
   
## <a name="have-a-user-reset-his-or-her-own-pin"></a>Festlegen, dass ein Benutzer seine eigene Pin zurücksetzt

1. Lassen Sie den Benutzer wechseln [https://admin0m.online.lync.com/lscp/usp/pstnconferencing](https://admin0m.online.lync.com/lscp/usp/pstnconferencing) .
2. Klicken Sie auf **PIN zurücksetzen**. 


## <a name="what-else-should-you-know-about-pins"></a>Was sollten Sie sonst über PINs wissen?

- Aus Sicherheitsgründen wird die PIN einem Administrator nur ein Mal gezeigt, wenn die PIN zurückgesetzt wird. Nachdem die PIN von einem Administrator zurückgesetzt wurde, wird die PIN als * * * * * * * * * * * angezeigt.
    
- Das automatische Senden von e-Mails an Benutzer ist standardmäßig aktiviert, und Benutzer erhalten eine e-Mail mit ihrer PIN, wenn Sie für Audiokonferenzen aktiviert sind oder wenn die PIN zurückgesetzt wird. Wenn Sie jedoch das automatische Senden von e-Mails deaktiviert haben, wird eine e-Mail mit Pin-Reset nicht an einen Benutzer gesendet, und Sie müssen die PIN-Informationen manuell an den Benutzer senden.
    
- Beim Start einer Besprechung nehmen alle Benutzer im Wartebereich automatisch an dieser teil. Wenn beispielsweise 2 Teilnehmer versuchen, vor dem Start der Besprechung an dieser teilzunehmen, werden sie im Wartebereich platziert und hören Warteschleifenmusik. Sobald der Organisator der Besprechung mit seiner PIN per Telefon teilnimmt, beginnt die Besprechung und alle Teilnehmer im Wartebereich nehmen an der Besprechung teil.
    
- Die Standardeinstellung ist, dass eine Besprechung nicht von anonymen Anrufern gestartet werden kann.
    
- Wenn Sie einen Benutzer für Audiokonferenzen aktivieren, werden standardmäßig e-Mail-Nachrichten gesendet, die Konferenz Informationen und Ihre PIN enthalten. Der Benutzer muss über ein Microsoft 365-oder Office 365-Postfach verfügen, denn wenn eine PIN zurückgesetzt wird, wird eine neue PIN an den Benutzer in einer e-Mail an die primäre SMTP-Adresse (Alias) gesendet, die für den Benutzer festgelegten ist.
    
- Wenn Sie Audiokonferenzen einrichten, legen Sie die Ziffern fest, die für die Pins in Ihrer Organisation erforderlich sind. PINs können 4 bis 12 Ziffern enthalten, standardmäßig werden 5 Ziffern verwendet. Wenn Sie die Einstellung für die PIN-Länge ändern, wird die Einstellung nur auf neu generierte Pins angewendet und nicht auf die PIN-Einstellung für vorhandene Benutzer angewendet, die für Audiokonferenzen aktiviert sind. Informationen finden Sie unter [Festlegung der Länge der PIN für Audiokonferenz-Besprechungen](Set-the-PIN-length-for-Audio-Conferencing-meetings-in-teams.md).
    
- Die e-Mail-Adresse ist standardmäßig auf die primäre SMTP-Adresse des Benutzers Microsoft 365 oder Office 365 eingestellt. Sie können eine e-Mail-Adresse an eine nicht von Microsoft 365-oder nicht-Office 365-Adresse senden, beispielsweise eine Hotmail-oder MSN-e-Mail-Adresse. Sie können die Standard-e-Mail-Adresse mithilfe von Windows PowerShell außer Kraft setzen. Dies ist hilfreich, wenn die Benutzer kein Exchange-Postfach in Microsoft 365 oder Office 365 haben.

    

## <a name="want-to-know-more-about-windows-powershell"></a>Möchten Sie mehr über Windows PowerShell erfahren?

Bei Windows PowerShell dreht sich alles um das Verwalten von Benutzern und Funktionen, die Benutzer verwenden oder nicht verwenden können. Mit Windows PowerShell können Sie Microsoft 365 oder Office 365 mithilfe einer zentralen Verwaltungsstelle verwalten, die Ihre tägliche Arbeit vereinfachen kann, wenn mehrere Aufgaben ausgeführt werden müssen. Informieren Sie sich in den folgenden Themen über die Verwendung von Windows PowerShell:
    
  - [Warum Sie Office 365 PowerShell verwenden müssen](https://go.microsoft.com/fwlink/?LinkId=525041)
    
  - [Beste Möglichkeiten zum Verwalten von Microsoft 365 oder Office 365 mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=525142)
    
Weitere Informationen zu Windows PowerShell finden Sie in der [PowerShell-Referenz für Microsoft Teams](https://docs.microsoft.com/powershell/module/teams/?view=teams-ps).
  
## <a name="related-topics"></a>Verwandte Themen

[Zurücksetzen einer Konferenzkennung für einen Benutzer](reset-a-conference-id-for-a-user-in-teams.md)
