---
title: Director (Planning Tool)
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.plan.Director
- ms.lync.plan.Director
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 02795b46-21ec-4a85-9890-959c91d97df3
ROBOTS: NOINDEX, NOFOLLOW
description: Ein Director ist ein Server, auf dem die Skype for Business Server-Kommunikationssoftware ausgeführt wird, mit der Benutzeranforderungen authentifiziert werden können, aber keine Benutzerkonten zu Hause sind.
ms.openlocfilehash: 4247642851b104b999521b664931ccbd3d6d5f61
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41797336"
---
# <a name="director-planning-tool"></a>Director (Planning Tool)
 
Ein Director ist ein Server, auf dem die Skype for Business Server-Kommunikationssoftware ausgeführt wird, mit der Benutzeranforderungen authentifiziert werden können, aber keine Benutzerkonten zu Hause sind. 
  
Diese Rolle ist optional, wenn Sie einen Director in den beiden folgenden Szenarien bereitstellen möchten:
  
- Wenn Sie den Zugriff von externen Benutzern durch die Bereitstellung von Edge-Servern aktivieren, sollten Sie auch einen Director bereitstellen. In diesem Szenario authentifiziert der Director die externen Benutzer und übergibt dann den Datenverkehr an interne Server. Wenn ein Director zur Authentifizierung externer Benutzer verwendet wird, entlastet es Front-End-Pool Server vor dem mehr Aufwand bei der Authentifizierung dieser Benutzer. Darüber hinaus können Sie interne Front-End-Pools vor böswilligem Datenverkehr wie Denial-of-Service-Angriffen isolieren. Wenn das Netzwerk bei einem solchen Angriff mit einem ungültigen externen Datenverkehr überflutet wird, endet dieser Datenverkehr beim Director.
    
- Wenn Sie mehrere Front-End-Pools an einem zentralen Standort bereitstellen, indem Sie dieser Website einen Director hinzufügen, können Sie Authentifizierungsanforderungen rationalisieren und die Leistung verbessern. In diesem Szenario gehen alle Anforderungen zuerst an den Director, der Sie dann an den richtigen Front-End-Pool weiterleitet.
    

