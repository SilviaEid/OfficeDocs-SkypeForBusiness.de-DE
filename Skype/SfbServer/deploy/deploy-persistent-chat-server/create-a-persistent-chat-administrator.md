---
title: Erstellen eines Administrators für beständigen Chat in Skype for Business Server 2015
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
ms.date: 3/28/2016
audience: ITPro
ms.topic: quickstart
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: 5c3892e4-ebae-453e-8107-f42ec0436ea2
description: 'Zusammenfassung: Lesen Sie dieses Thema, um zu erfahren, wie Sie eine Server Administratorrolle für beständigen Chat erstellen, um die anfängliche Konfiguration und Verwaltung beständiger Chat Dienste in Skype for Business Server 2015 zu ermöglichen.'
ms.openlocfilehash: 987183b8ca5cc32e2888040b43d61e5d6fcac09b
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41794103"
---
# <a name="create-a-persistent-chat-administrator-in-skype-for-business-server-2015"></a>Erstellen eines Administrators für beständigen Chat in Skype for Business Server 2015
 
**Zusammenfassung:** In diesem Thema erfahren Sie, wie Sie eine Server Administratorrolle für beständigen Chat erstellen, um die anfängliche Konfiguration und Verwaltung beständiger Chat Dienste in Skype for Business Server 2015 zu ermöglichen.
  
In Skype for Business Server müssen Benutzer, die bestimmte Aufgaben ausführen, Mitgliedern einer oder mehrerer bestimmter Gruppen zugewiesen werden. Rollenbasierte Zugriffssteuerung wird verwendet, um Berechtigungen zu gewähren, indem Benutzer vordefinierten Skype for Business Server-Administratorrollen zugewiesen werden. Diese Rollen entsprechen den allgemeinen Sicherheitsgruppen in den Active Directory-Domänendiensten. Mitgliedern der Gruppe "beständiger Chat-Administrator", CsPersistentChatAdministrator, wird der Zugriff auf die Server-Cmdlets des beständigen Chats gewährt, die entweder über die Skype for Business Server-Verwaltungsshell oder über Skype for Business ausgeführt werden können. Server-Systemsteuerung.
  
Bevor Sie den Server für beständigen Chat konfigurieren und verwalten, sollten Sie sicherstellen, dass die entsprechenden Rechte und Berechtigungen vorhanden sind und dass alle Benutzer, die als Administratoren für den beständigen Chat fungieren sollen, der Administrator-Sicherheitsgruppe für den beständigen Chat hinzugefügt werden.
  
> [!NOTE] 
> Der beständige Chat ist in Skype for Business Server 2015 verfügbar, wird aber in Skype for Business Server 2019 nicht mehr unterstützt. In Teams steht dieselbe Funktionalität zur Verfügung. Weitere Informationen finden Sie unter [Erste Schritte mit dem Upgrade für Microsoft Teams](/microsoftteams/upgrade-start-here). Wenn Sie den beständigen Chat verwenden müssen, können Sie entweder Benutzer migrieren, die diese Funktion für Teams benötigen, oder die Verwendung von Skype for Business Server 2015 fortsetzen.

## <a name="create-a-persistent-chat-administrator"></a>Create a Persistent Chat administrator

Führen Sie die folgenden Schritte aus, um einen Benutzer zur Administrator Sicherheitsgruppe für beständigen Chat hinzuzufügen: CsPersistentChatAdministrator
  
1. Melden Sie sich über ein Konto mit Berechtigung zum Ändern der Mitgliedschaft einer Active Directory-Gruppe an dem Computer an, auf dem „Active Directory-Benutzer und -Computer“ installiert ist.
    
2. Klicken Sie nacheinander auf Start, Alle Programme, Verwaltung und Active Directory-Benutzer und -Computer.
    
3. Erweitern Sie in „Active Directory-Benutzer und -Computer“ den Namen Ihrer Domäne und klicken Sie auf den Container „Users“.
    
4. Klicken Sie mit der rechten Maustaste auf die Sicherheitsgruppe „CsPersistentChatAdministrator“ und dann auf „Eigenschaften“.
    
5. Klicken Sie im Dialogfeld „Eigenschaften“auf die Registerkarte „Mitglieder“ und anschließend auf „Hinzufügen“.
    
6. Geben Sie im Dialogfeld „Benutzer, Computer, Kontakte oder Gruppen auswählen“ im Feld „Geben Sie die zu verwendenden Objektnamen ein“ den Benutzer- oder Anzeigenamen des Benutzers ein, der zur Gruppe hinzugefügt werden soll, und klicken Sie auf „OK“.
    
7. Klicken Sie im Dialogfeld „Eigenschaften“ auf „OK“.
    

