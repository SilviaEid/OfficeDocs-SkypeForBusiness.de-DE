---
title: Nicht zugewiesene Telefonnummer, neue erstellen oder vorhandene bearbeiten
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: article
ms.custom:
- ms.lync.lscp.VoiceFeaVacantNumEdit
ms.prod: skype-for-business-itpro
f1.keywords:
- CSH
localization_priority: Normal
ms.assetid: 58903e40-6b93-40d6-88f8-1201743cd9be
ROBOTS: NOINDEX, NOFOLLOW
description: Nicht zugewiesene Nummern sind Rufnummern, die für Ihre Organisation gültig sind, jedoch keinem Benutzer oder Telefon zugewiesen sind. In der Tabelle mit den nicht zugewiesenen Nummern ist angegeben, wie Anrufe bei nicht zugewiesenen Nummern behandelt werden sollen.
ms.openlocfilehash: 87d83f6285e36abf6b063ba7d6c4d1a93cadc633
ms.sourcegitcommit: b1229ed5dc25a04e56aa02aab8ad3d4209559d8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41792163"
---
# <a name="unassigned-phone-number-create-new-or-edit-existing"></a>Nicht zugewiesene Telefonnummer: Erstellen einer neuen oder Bearbeiten einer vorhandenen nicht zugewiesenen Nummer

> [!NOTE]
> Exchange um bleibt in Skype for Business Server 2019 verfügbar, wenn Sie Skype for Business 2019 mit Exchange 2013 oder Exchange 2016 integrieren. Aufgrund von Änderungen an der Unterstützung in Exchange 2019 wird die Exchange um-Integration zu Gunsten der Features Cloud Voicemail und Cloud-automatische Telefonzentrale de-hervorgehoben.

Nicht zugewiesene Nummern sind Rufnummern, die für Ihre Organisation gültig sind, jedoch keinem Benutzer oder Telefon zugewiesen sind. In der Tabelle mit den nicht zugewiesenen Nummern ist angegeben, wie Anrufe bei nicht zugewiesenen Nummern behandelt werden sollen.

> [!IMPORTANT]
> Wenn Sie mit dem Erstellen eines neuen nicht zugewiesenen Nummernbereichs fertig sind oder ein vorhandenes ändern möchten, klicken Sie auf **OK** , um zur Seite nicht **zugewiesene Zahl** zurückzukehren, auf der alle Nummernbereiche aufgelistet sind. Die Änderungen, die Sie auf der Seite "nicht **zugewiesene Nummernbereich** " oder "nicht zugewiesene **Nummer bearbeiten** " vorgenommen haben, werden nicht in die Datenbank übernommen, bis Sie auf der Seite "nicht **zugewiesene Nummer** " auf " **alle festlegen** " klicken.

## <a name="ui-reference"></a>Referenz zur Benutzeroberfläche

In der folgenden Liste werden die Felder der Seite beschrieben.

- **Name** Geben Sie einen aussagekräftigen Namen ein, der den nicht zugewiesenen Nummernbereich kennzeichnet. Nachdem Sie den Bereich gespeichert haben, kann dieser Name nicht geändert werden.

- **Nummernbereich** Geben Sie im ersten Feld die Anfangszahl des nicht zugewiesenen Nummernbereichs ein. Geben Sie im zweiten Feld die letzte Zahl für den Bereich ein.

  - Die Startnummer für den Bereich muss kleiner oder gleich der Endnummer sein.

  - Wenn die erste Nummer im Bereich oder die letzte Nummer im Bereich eine Durchwahl umfassen, müssen sowohl die erste als auch die letzte Nummer im Bereich einen Durchwahl aufweisen und die Durchwahlnummer muss für die erste und die letzte Nummer übereinstimmen.

  - Die Nummer muss mit dem regulären Ausdruck übereinstimmen (Tel:)? ( \+)? [1-9] \d{0,17}(; ext = [1-9] \d{0,9})? Dies bedeutet, dass die Nummer mit der Zeichenfolge Tel beginnen kann: (wenn Sie diese Zeichenfolge nicht angeben, wird Sie automatisch für Sie hinzugefügt), ein Pluszeichen (+) und eine Ziffer 1 bis 9. Die Telefonnummer kann bis zu 17 Zeichen umfassen, gefolgt von einer Durchwahl im Format ";ext=" plus der Durchwahlnummer.

- **Ankündigungsdienst** Wählen Sie **Ankündigung** aus, damit die Ankündigungs Anwendung den eingehenden Anruf oder **Exchange um** verarbeitet, damit der eingehende Anruf von einer automatischen Exchange UM-Telefonzentrale verarbeitet wird.

- Wenn Sie **Ankündigung** für **Ankündigungsdienst**ausgewählt haben:

  - **FQDN des Zielservers** Wählen Sie die Dienst-ID des Anwendungsdiensts aus, der die Ankündigungs Anwendung ausführt, mit der eingehende Anrufe an diesen Bereich nicht zugewiesener Nummern verarbeitet werden.

  - **Ankündigung** Wählen Sie die Ansage aus, die für diesen Bereich nicht zugewiesener Nummern abgespielt werden soll.

- Wenn Sie **Exchange um** für **Ankündigungsdienst**ausgewählt haben:

  - **Telefonnummer der automatischen Telefonzentrale** Wählen Sie die Telefonnummer für die automatische Exchange UM-Telefonzentrale aus.

Details zu Ankündigungs Features und-Funktionen finden Sie unter [Planen der Ankündigungs Anwendung in Skype for Business](../../../plan-your-deployment/enterprise-voice-solution/announcement.md) in der Planungsdokumentation. Ausführliche Informationen zur Verwendung von Bereichen nicht zugewiesener Nummern finden Sie in der Betriebsdokumentation unter [Configure Routing of Unassigned Phone Numbers](https://technet.microsoft.com/library/a0650659-dce7-455f-8977-02454bbfa400.aspx).


