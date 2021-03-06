---
title: Überprüfen von Normalisierungsregeln für den Parken von Anrufen in Skype for Business
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: quickstart
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.collection:
- IT_Skype16
- Strat_SB_Admin
ms.custom: ''
ms.assetid: deaa170f-041e-45cb-8eab-f02931ab541e
description: Informieren Sie sich über Normalisierungsregeln für den Parken von Anrufen in Skype for Business Server Enterprise-VoIP.
ms.openlocfilehash: 769d9f9becccf4df24a33a11e8814350cfb091e8
ms.sourcegitcommit: dd3a3ab4ddbdcfe772f30fb01ba3b97c45c43dd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "41766888"
---
# <a name="verify-normalization-rules-for-call-park-in-skype-for-business"></a>Überprüfen von Normalisierungsregeln für den Parken von Anrufen in Skype for Business
 
Informieren Sie sich über Normalisierungsregeln für den Parken von Anrufen in Skype for Business Server Enterprise-VoIP.
  
Orbits für das Parken von anrufen dürfen nicht normalisiert werden. Überprüfen Sie Ihre Wählpläne, um sicherzustellen, dass Ihre Orbit-Nummern nicht normalisiert sind. Wenn Sie eine zusätzliche Normalisierungsregel erstellen müssen, um zu verhindern, dass ihre Umlaufbahnen normalisiert werden, führen Sie die Schritte unter [erstellen oder Ändern eines Wählplans in Skype for Business Server](dial-plans.md) aus, um eine neue Normalisierungsregel zu definieren, damit das **übereinstimmende Muster** den Umlaufbahn Bereich und das **Übersetzungsmuster** auf **$1**angibt. Wenn beispielsweise der Orbit-Bereich Ihres Anruf Parks 7000-7999 ist, ist das **Muster, das übereinstimmen** soll, **^ (7 \ d{3}) $** , und das **Übersetzungsmuster** ist **$1**.
  
> [!IMPORTANT]
> Stellen Sie sicher, dass die Standard Normalisierungsregel in ihren Wählplänen **^ (\d\*)** nicht enthält. Andernfalls wird Ihre Normalisierungsregel für den Anruf Park nie ausgeführt.
  
## <a name="see-also"></a>Siehe auch

[Erstellen oder Ändern eines Wählplans in Skype for Business Server](dial-plans.md)

