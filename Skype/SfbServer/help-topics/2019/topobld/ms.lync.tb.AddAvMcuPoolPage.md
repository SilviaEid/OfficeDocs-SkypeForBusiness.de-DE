---
title: Hinzufügen des A/V-MCU-Pools
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
f1.keywords:
- CSH
ms.custom:
- ms.lync.tb.AddAvMcuPoolPage
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: e201875e-1e81-4756-942f-c17d177e997b
ROBOTS: NOINDEX, NOFOLLOW
description: Alle Enterprise Edition-Front-End-Server eines zentralen Standorts, die keinen a/v-Konferenzdienst haben, können denselben eigenständigen a/v-Konferenz Pool verwenden. Für jeden a/v-Konferenz Pool müssen Sie einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Pool angeben und angeben, ob nur ein einzelner a/v-Konferenzserver oder mehrere Server mit Lastenausgleich für a/v-Konferenzen vorhanden sein sollen.
ms.openlocfilehash: b2fd57f0a6c9f39638f62a9bae7c9ed29a73a779
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41794834"
---
# <a name="add-av-mcu-pool"></a>Hinzufügen des A/V-MCU-Pools
 
Alle Enterprise Edition-Front-End-Server eines zentralen Standorts, die keinen a/v-Konferenzdienst haben, können denselben eigenständigen a/v-Konferenz Pool verwenden. Für jeden a/v-Konferenz Pool müssen Sie einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Pool angeben und angeben, ob nur ein einzelner a/v-Konferenzserver oder mehrere Server mit Lastenausgleich für a/v-Konferenzen vorhanden sein sollen.
  
> [!IMPORTANT]
> Sie können einen Pool mit einem einzelnen Server nicht in einen Pool mit mehreren Servern konvertieren. Wenn Sie später entscheiden, dass Ihre Organisation einen Pool mit mehreren Servern benötigt, müssen Sie den Pool mit einem Server löschen und dann den Pool mit mehreren Servern hinzufügen. 
  
> [!TIP]
> Wenn Sie beabsichtigen, in Zukunft einen A/V-Konferenz Pool zu implementieren, wählen Sie den **Pool für mehrere Computer**aus. Wenngleich ein Pool per Definition mindestens zwei Computer mit Lastenausgleich umfasst, können Sie einen Pool mit einem einzigen Computer sowie einen Pool-FQDN für diesen einzelnen Computer erstellen. Wenn Sie bereit sind, dem Pool später weitere Computer hinzuzufügen, müssen Sie den Topologie-Generator erneut definieren, um das neue Poolmitglied zu definieren, die neue Topologie zu veröffentlichen und dann das neue A/V-Konferenz Poolmitglied über den Skype for Business Server-Bereitstellungs-Assistenten einzurichten. A/V-Konferenz Server Pools sind einzigartig, da Sie keine Lastenausgleichsfunktionen zum Erstellen eines Pools benötigen. A/V-Konferenz Pools laden den Lastenausgleich intern und benötigen keine zusätzliche Hardware. 
  

