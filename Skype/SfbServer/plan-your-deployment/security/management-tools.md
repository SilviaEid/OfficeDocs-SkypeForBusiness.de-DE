---
title: Windows PowerShell und Skype for Business Server-Verwaltungstools
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: 6a285f7c-0ef5-4cab-9976-d03be276e35d
description: 'In Skype for Business Server werden Verwaltungstools mithilfe von Windows PowerShell implementiert. Windows PowerShell umfasst eine Befehlszeilenumgebung, produktspezifische Befehle und eine vollständige Skriptsprache. Zu den Skype for Business Server-Tools, die mit Windows PowerShell implementiert werden, gehören die folgenden:'
ms.openlocfilehash: f20a78729e778b069f7e84c9b7ed53e8564d2516
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41815643"
---
# <a name="windows-powershell-and-skype-for-business-server-management-tools"></a>Windows PowerShell und Skype for Business Server-Verwaltungstools
 
In Skype for Business Server werden Verwaltungstools mithilfe von Windows PowerShell implementiert. Windows PowerShell umfasst eine Befehlszeilenumgebung, produktspezifische Befehle und eine vollständige Skriptsprache. Zu den Skype for Business Server-Tools, die mit Windows PowerShell implementiert werden, gehören die folgenden: 
  
- **Topologie-Generator** Sie verwenden den Topologie-Generator zum Erstellen, anpassen und Veröffentlichen Ihrer geplanten Topologie, und Sie überprüft Ihre Topologie, bevor Sie mit Server Installationen beginnen. Wenn Sie Skype for Business Server auf einzelnen Servern installieren, lesen die Server die veröffentlichte Topologie als Teil des Installationsvorgangs, und das Installationsprogramm stellt den Server gemäß den Anweisungen in der Topologie bereit. Nach dem Setup werden die Konfigurationsinformationen automatisch auf alle Server repliziert. Komponenten können Ihrer Bereitstellung nur mithilfe des Topologie-Generators hinzugefügt werden.
    
- **Skype for Business Server-Verwaltungsshell**. Sie können die Skype for Business Server-Verwaltungsshell für die vollständige Befehlszeilenverwaltung Ihrer Bereitstellung verwenden.
    
- **Skype for Business Server-System**Steuerung. Sie können die Benutzeroberfläche von Skype for Business Server Control Panel verwenden, um die häufigsten Aufgaben in Ihrer Bereitstellung zu verwalten.
    
Diese Tools verwenden Windows PowerShell-Cmdlets für die Verwaltung Ihrer Bereitstellung, einschließlich in der Nähe von 550-produktspezifischen Cmdlets. Die Sicherheits-Cmdlets, die in Skype for Business Server enthalten sind, werden in erster Linie zum Verwalten von Authentifizierung und Benutzerrechten und-Berechtigungen verwendet. Zum Verwalten der Authentifizierung stehen vielfältige Cmdlets zur Verfügung, darunter Cmdlets für die Zertifikat- und PIN-Authentifizierung. Darüber hinaus können Sie mit einer Reihe von Cmdlets die neue rollenbasierte Zugriffssteuerungsfunktion (Role-Based Access Control, RBAC) verwenden, um die administrative Steuerung von Skype for Business Server zu delegieren. Details zu den Skype for Business Server-Cmdlets finden Sie unter [Skype for Business Server-Verwaltungsshell](../../manage/management-shell.md).
  
Die Skript Sicherheitsfeatures für Windows PowerShell wurden speziell entwickelt, um zu verhindern, dass einige der Skript bezogenen Sicherheitsprobleme älterer Technologien, einschließlich Microsoft Visual Basic Scripting Edition (VBScript), unterstützt werden. Die Windows PowerShell-Sicherheitsfeatures sollen eine Umgebung erstellen, in der Benutzer keine einfachen oder unwissentlichen Skripts ausführen können. Standardmäßig sind die Windows PowerShell-Sicherheitsfeatures aktiviert. Sie können den Zustand dieser Features ändern, damit Sie Ihren Skriptanforderungen und einer Reihe von Sicherheitszielen gerecht werden. Dies soll nicht heißen, dass die Shell es Benutzern unmöglich macht, Skripts auszuführen. Stattdessen erschwert die Shell standardmäßig, dass Benutzer Skripts ausführen können, ohne dass dies zu erkennen ist. Ausführliche Informationen finden Sie unter [Windows PowerShell-Skriptsicherheit](https://go.microsoft.com/fwlink/p/?LinkId=213145).
  

