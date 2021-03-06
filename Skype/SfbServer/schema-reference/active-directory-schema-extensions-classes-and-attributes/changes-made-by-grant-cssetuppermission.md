---
title: Von Grant-CsSetupPermission in Skype for Business Server vorgenommene Änderungen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
ms.date: 10/20/2015
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
description: Um das Setup zu delegieren, können Sie der universellen RTCUniversalServerAdmins-Gruppe Berechtigungen für eine bestimmte Active Directory-Organisationseinheit erteilen und Mitgliedern der RTCUniversalServerAdmins-Gruppe in dieser OU die Installation von Skype for Business Server im angegebene Domäne, ohne Mitglieder der Gruppe "Domänen-Admins" zu sein.
ms.openlocfilehash: 844cfa586523750b804564482146c0e76b39fc38
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41815513"
---
# <a name="changes-made-by-grant-cssetuppermission-in-skype-for-business-server"></a>Von Grant-CsSetupPermission in Skype for Business Server vorgenommene Änderungen
 
Um das Setup zu delegieren, können Sie der universellen RTCUniversalServerAdmins-Gruppe Berechtigungen für eine bestimmte Active Directory-Organisationseinheit erteilen und Mitgliedern der RTCUniversalServerAdmins-Gruppe in dieser OU die Installation von Skype for Business Server im angegebene Domäne, ohne Mitglieder der Gruppe "Domänen-Admins" zu sein. 
  
Das Cmdlet **Grant-CsSetupPermission** gewährt der RTCUniversalServerAdmins-Gruppe Berechtigungen für eine OU, wie in der folgenden Tabelle angegeben:
  
**Berechtigungen, die Objekten in der Organisationseinheit gewährt werden**

|**Berechtigungen gelten für:**|**Gewährte Berechtigungen sind:**|
|:-----|:-----|
|RTCUniversalServerAdmins  <br/> | Spezieller Zugriff: <br/>  Lesen von servicePrincipalName <br/>  Schreiben von servicePrincipalName <br/>  Struktur löschen <br/>  Replizieren von Verzeichnisänderungen <br/> |
|Nachfolger serviceConnectionPoint-Objekte  <br/> | Spezieller Zugriff: <br/>  Leseberechtigungen <br/>  Schreibberechtigungen <br/>  Erstellen eines untergeordneten Elements <br/>  Untergeordnetes Element löschen <br/>  Listeninhalt <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|NachfolgerAttribut msRTCSIP-Server Objekte  <br/> | Spezieller Zugriff: <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|NachfolgerAttribut msRTCSIP – Webkomponenten Objekte  <br/> | Spezieller Zugriff: <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|NachfolgerAttribut msRTCSIP-MCU-Objekte  <br/> | Spezieller Zugriff: <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|NachfolgerAttribut msRTCSIP-MediationServer-Objekte  <br/> | Spezieller Zugriff: <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|NachfolgerAttribut msRTCSIP-ApplicationServer-Objekte  <br/> | Spezieller Zugriff: <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|NachfolgerAttribut msRTCSIP-ConnectionPoint-Objekte  <br/> | Spezieller Zugriff: <br/>  Write-Eigenschaft <br/>  Read-Eigenschaft <br/>  Struktur löschen <br/> |
|Nachfolger Computer Objekte  <br/> | Spezieller Zugriff für serviceConnectionPoint: <br/>  Erstellen von untergeordneten Objekten <br/>  Löschen von untergeordneten Objekten <br/>  Struktur löschen <br/>  Spezieller Zugriff für öffentliche Informationen: <br/>  Read-Eigenschaft <br/>  Spezieller Zugriff auf den DNS-Hostname: <br/>  Read-Eigenschaft <br/> |
   

