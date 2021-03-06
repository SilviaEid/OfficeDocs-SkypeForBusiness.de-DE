---
title: Deaktivieren von gebührenfreien Telefonnummern für bestimmte Microsoft Teams-Benutzer
ms.author: tonysmit
author: tonysmit
manager: serdars
ms.reviewer: oscarr
ms.topic: article
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
- seo-marvel-mar2020
description: Erfahren Sie, wie Sie steuern können, wie Organisatoren gebührenfreie Nummern für Ihre Audiokonferenz-Bridge-Besprechungen verwenden können.
ms.openlocfilehash: 517ffea6a15cd625320f33e3eb4911f4a250d51d
ms.sourcegitcommit: a9e16aa3539103f3618427ffc7ebbda6919b5176
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "43904570"
---
# <a name="disabling-toll-free-numbers-for-specific-teams-users"></a>Deaktivieren von gebührenfreien Telefonnummern für bestimmte Microsoft Teams-Benutzer

Wenn die Microsoft-Audiokonferenzbrücke Ihrer Organisation gebührenfreie Telefonnummern enthält, können Sie die Verwendung dieser Nummern in den Besprechungen bestimmter Organisatoren zulassen oder verhindern.  

Standardmäßig ist die Verwendung von gebührenfreien Telefonnummern für alle Benutzer in der Organisation aktiviert. Das heißt, wenn diese Nummern verfügbar sind, können sie von Teilnehmern für die Teilnahme an den Besprechungen der Benutzer verwendet werden. Wenn dieses Verhalten für einige Benutzer in der Organisation nicht gewünscht wird, können Sie über ein Steuerelement für die Aktivierung gebührenfreier Telefonnummern festlegen, dass bestimmte Benutzer diese Nummern nicht in ihren Besprechungen verwenden können. 

Wenn gebührenfreie Telefonnummern für einen bestimmten Organisator deaktiviert sind, gilt Folgendes: 
 - Die Besprechungseinladungen dieses Benutzers enthalten keine gebührenfreie Telefonnummer mehr. 
 - Gebührenfreie Telefonnummern werden nicht mehr auf der Seite „Lokale Rufnummer suchen“ aufgelistet, auf die in den Besprechungseinladungen dieses Benutzers verwiesen wird. 
 - Teilnehmer können nicht an der Besprechung des entsprechenden Organisators teilnehmen, wenn sie eine gebührenfreie Telefonnummer der Organisation wählen. 
 - Alle Besprechungen des Organisators werden automatisch neu geplant, und die gebührenfreie Telefonnummer wird aus den Besprechungen entfernt.  

    > [!IMPORTANT]
    > Dies bedeutet, dass alle E-Mail-Einladungen des Organisators erneut an die Teilnehmer dieser Besprechungen gesendet werden. 

 - Die Teilnehmer können weiterhin über gebührenpflichtige Telefonnummern an den Besprechungen des Organisators teilnehmen. 

## <a name="disabling-toll-free-numbers-for-specific-users"></a>Deaktivieren von gebührenfreien Telefonnummern für bestimmte Benutzer 

Im **Microsoft Teams Admin Center**:

1. Klicken Sie in der linken Navigationsleiste auf **Benutzer**, und wählen Sie dann den Benutzer aus der Liste der verfügbaren Benutzer aus.

2. Klicken Sie neben **Audiokonferenz** auf **Bearbeiten**.

3. Legen Sie **gebührenfreie Nummern in Besprechungsanfragen von diesem Benutzer** auf **aus**. 

4. Klicken Sie auf **Speichern**. 

 
> [!Note]
> [!INCLUDE [updating-admin-interfaces](includes/updating-admin-interfaces.md)]
 
**Verwenden von PowerShell**  

Weitere Informationen finden Sie in der [PowerShell-Referenz für Microsoft Teams](https://docs.microsoft.com/powershell/module/teams/?view=teams-ps).
