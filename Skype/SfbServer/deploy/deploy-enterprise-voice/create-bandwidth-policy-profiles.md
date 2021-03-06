---
title: Erstellen von Bandbreitenrichtlinien Profilen in Skype for Business Server
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
ms.assetid: a71881ef-b04a-465e-9abb-0577bfd182f3
description: Sie können Bandbreitenrichtlinien erstellen oder ändern, die von der Sprachanruf Steuerung für Unternehmen in Skype for Business Server verwendet werden.
ms.openlocfilehash: e54fc20c142e0eacc2758d97bdeba8043511b3fe
ms.sourcegitcommit: dd3a3ab4ddbdcfe772f30fb01ba3b97c45c43dd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "41767948"
---
# <a name="create-bandwidth-policy-profiles-in-skype-for-business-server"></a>Erstellen von Bandbreitenrichtlinien Profilen in Skype for Business Server 
 
Sie können Bandbreitenrichtlinien erstellen oder ändern, die von der Sprachanruf Steuerung für Unternehmen in Skype for Business Server verwendet werden. 
  
Bandbreitenrichtlinien definieren Einschränkungen zur Bandbreitenauslastung für in Echtzeit übertragene Audio- und Videodaten. Bandbreitenrichtlinien gelten für Richtlinien Profile, die für die Anrufsteuerung auf mehrere Netzwerk Websites angewendet werden können.
  
Richtlinien zu den Bandbreiteneinschränkungen, die Sie in ihrer CAC-Bereitstellung festlegen sollten, finden Sie unter [Planen der Anrufsteuerung in Skype for Business Server](../../plan-your-deployment/enterprise-voice-solution/call-admission-control.md).
  
Die im folgenden Verfahren erstellten Beispielrichtlinien legen Einschränkungen für den Audiodatenverkehr insgesamt, einzelne Audiositzungen, den Videodatenverkehr insgesamt und einzelne Videositzungen fest. Das Bandbreitenrichtlinienprofil „5Mb_Link“ legt beispielsweise folgende Einschränkungen fest: 
  
- Grenzwert für Audio: 2.000 KBit/s
    
- Grenzwert für Audiositzung: 200 KBit/s
    
- Grenzwert für Video: 1.400 KBit/s
    
- Grenzwert für Videositzung: 700 KBit/s
    
> [!NOTE]
> Der Mindestgrenzwert für Audiositzungen ist 40 KBit/s. Der Mindestgrenzwert für Videositzungen ist 100 KBit/s. 
  
### <a name="to-create-bandwidth-policy-profiles-by-using-skype-for-business-server-management-shell"></a>So erstellen Sie bandbreitenrichtlinienprofile mithilfe der Skype for Business Server-Verwaltungsshell

1. Starten Sie die Skype for Business Server-Verwaltungsshell: Klicken Sie auf **Start**, zeigen Sie auf **Alle Programme** und dann auf **Skype for Business 2015** und klicken Sie anschließend auf **Skype for Business Server-Verwaltungsshell**.
    
2. Führen Sie für jedes Bandbreitenrichtlinienprofil, das Sie erstellen möchten, das Cmdlet „New-CsNetworkBandwidthPolicyProfile“ aus. Führen Sie beispielsweise den folgenden Befehl aus:
    
   ```powershell
   New-CsNetworkBandwidthPolicyProfile -Identity 5Mb_Link -Description "BW profile for 5Mb links" -AudioBWLimit 2000 -AudioBWSessionLimit 200 -VideoBWLimit 1400   -VideoBWSessionLimit 700
   ```

   ```powershell
   New-CsNetworkBandwidthPolicyProfile -Identity 10Mb_Link -Description "BW profile for 10Mb links" -AudioBWLimit 4000 -AudioBWSessionLimit 200 -VideoBWLimit 2800 -VideoBWSessionLimit 700
   ```

   ```powershell
   New-CsNetworkBandwidthPolicyProfile -Identity 50Mb_Link -Description "BW profile for 50Mb links" -AudioBWLimit 20000 -AudioBWSessionLimit 200 -VideoBWLimit 14000 -VideoBWSessionLimit 700
   ```

   ```powershell
   New-CsNetworkBandwidthPolicyProfile -Identity 25Mb_Link -Description "BW profile for 25Mb links" -AudioBWLimit 10000 -AudioBWSessionLimit 200 -VideoBWLimit 7000 -VideoBWSessionLimit 700
   ```

### <a name="to-create-bandwidth-policy-profiles-by-using-skype-for-business-server-control-panel"></a>So erstellen Sie bandbreitenrichtlinienprofile mithilfe der Skype for Business Server-Systemsteuerung

1. Öffnen Sie die Skype for Business Server-Systemsteuerung.
    
2. Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration**.
    
3. Klicken Sie auf die Navigationsschaltfläche **Richtlinienprofil**.
    
4. Klicken Sie auf **Neu**.
    
5. Klicken Sie auf der Seite **Neues Richtlinienprofil** auf **Name** und geben Sie einen Namen für das Bandbreitenrichtlinienprofil ein.
    
6. Klicken Sie auf **Audiolimit** und geben Sie die Höchstzahl an KBit/s ein, die für alle Audiositzungen insgesamt zulässig sein soll.
    
7. Klicken Sie auf **Grenzwert für Audiositzung** und geben Sie die Höchstzahl an KBit/s ein, die für jede einzelne Audiositzung zulässig sein soll.
    
8. Klicken Sie auf **Videolimit** und geben Sie die Höchstzahl an KBit/s ein, die für alle Videositzungen insgesamt zulässig sein soll.
    
9. Klicken Sie auf **Grenzwert für Videositzung** und geben Sie die Höchstzahl an KBit/s ein, die für jede einzelne Videositzung zulässig sein soll.
    
10. Klicken Sie optional auf **Beschreibung** und geben Sie zusätzliche Informationen zur Beschreibung dieses Bandbreitenrichtlinienprofils ein.
    
11. Klicken Sie auf **Commit ausführen**.
    
12. Wiederholen Sie die Schritte 4 bis 11 mit Einstellungen für andere Bandbreitenrichtlinienprofile, um die Erstellung von Bandbreitenrichtlinienprofilen für Ihre Topologie abzuschließen.
    
## <a name="see-also"></a>Siehe auch

[New-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/new-csnetworkbandwidthpolicyprofile?view=skype-ps)
  
[Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/get-csnetworkbandwidthpolicyprofile?view=skype-ps)
  
[Set-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/set-csnetworkbandwidthpolicyprofile?view=skype-ps)
  
[Remove-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/remove-csnetworkbandwidthpolicyprofile?view=skype-ps)
