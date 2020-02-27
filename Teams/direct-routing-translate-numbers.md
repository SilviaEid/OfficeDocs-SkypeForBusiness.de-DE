---
title: Übersetzen von Telefonnummern für die direkte Weiterleitung
ms.reviewer: ''
ms.author: crowe
author: CarolynRowe
manager: serdars
audience: ITPro
ms.topic: article
ms.service: msteams
localization_priority: Normal
search.appverid: MET150
ms.collection:
- M365-voice
appliesto:
- Microsoft Teams
f1.keywords:
- NOCSH
description: Hier erfahren Sie, wie Sie das direkte Routing des Microsoft Phone-Systems konfigurieren.
ms.openlocfilehash: 2b675948153589c73fa545a95ac785b716b55265
ms.sourcegitcommit: 0289062510f0791906dab2791c5db8acb1cf849a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "42157972"
---
# <a name="translate-phone-numbers-to-an-alternate-format"></a><span data-ttu-id="d6514-103">Übersetzen von Telefonnummern in ein anderes Format</span><span class="sxs-lookup"><span data-stu-id="d6514-103">Translate phone numbers to an alternate format</span></span>

<span data-ttu-id="d6514-104">In diesem Artikel wird beschrieben, wie Sie zahlen für ausgehende und eingehende Anrufe in ein alternatives Format übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d6514-104">This article describes how to translate numbers for outbound and inbound calls to an alternate format.</span></span>  <span data-ttu-id="d6514-105">Dies ist Schritt 4 der folgenden Schritte zum Konfigurieren des direkten Routings:</span><span class="sxs-lookup"><span data-stu-id="d6514-105">This is step 4 of the following steps for configuring Direct Routing:</span></span>

- <span data-ttu-id="d6514-106">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="d6514-106">Step 1.</span></span> [<span data-ttu-id="d6514-107">Verbinden des SBC mit dem Microsoft Phone-System und Überprüfen der Verbindung</span><span class="sxs-lookup"><span data-stu-id="d6514-107">Connect the SBC with Microsoft Phone System and validate the connection</span></span>](direct-routing-connect-the-sbc.md) 
- <span data-ttu-id="d6514-108">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="d6514-108">Step 2.</span></span> [<span data-ttu-id="d6514-109">Aktivieren von Benutzern für Direct Routing, Voicemail und Voicemail</span><span class="sxs-lookup"><span data-stu-id="d6514-109">Enable users for Direct Routing, voice, and voicemail</span></span>](direct-routing-enable-users.md)   
- <span data-ttu-id="d6514-110">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="d6514-110">Step 3.</span></span> [<span data-ttu-id="d6514-111">Konfigurieren des VoIP-Routings</span><span class="sxs-lookup"><span data-stu-id="d6514-111">Configure voice routing</span></span>](direct-routing-voice-routing.md)
- <span data-ttu-id="d6514-112">**Schritt 4. Übersetzen von Zahlen in ein alternatives Format** (dieser Artikel)</span><span class="sxs-lookup"><span data-stu-id="d6514-112">**Step 4. Translate numbers to an alternate format**   (This article)</span></span>

<span data-ttu-id="d6514-113">Informationen zu allen Schritten, die für das Einrichten des direkten Routings erforderlich sind, finden Sie unter [Konfigurieren des direkten Routings](direct-routing-configure.md).</span><span class="sxs-lookup"><span data-stu-id="d6514-113">For information on all the steps required for setting up Direct Routing, see [Configure Direct Routing](direct-routing-configure.md).</span></span>

<span data-ttu-id="d6514-114">Manchmal möchten mandantenadministratoren die Nummer für ausgehende und/oder eingehende Anrufe basierend auf den von Ihnen erstellten Mustern ändern, um die Interoperabilität mit Session Border Controllers (SBCS) zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="d6514-114">Sometimes tenant administrators may want to change the number for outbound and/or inbound calls based on the patterns they created to ensure interoperability with Session Border Controllers (SBCs).</span></span> <span data-ttu-id="d6514-115">In diesem Artikel wird beschrieben, wie Sie eine Richtlinie für die Nummernübersetzung angeben können, um Zahlen in ein alternatives Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d6514-115">This article describes how you can specify a Number Translation Rules policy to translate numbers to an alternate format.</span></span> 

<span data-ttu-id="d6514-116">Sie können die Richtlinien für die Zahlen Übersetzung verwenden, um Zahlen für Folgendes zu übersetzen:</span><span class="sxs-lookup"><span data-stu-id="d6514-116">You can use the Number Translation Rules policy to translate numbers for the following:</span></span>

- <span data-ttu-id="d6514-117">Eingehende Anrufe: Anrufe von einem PSTN-Endpunkt (Anrufer) an einen Teams-Client (angerufener)</span><span class="sxs-lookup"><span data-stu-id="d6514-117">Inbound calls: Calls from a PSTN endpoint (caller) to a Teams client (callee)</span></span>
- <span data-ttu-id="d6514-118">Ausgehende Anrufe: Anrufe von einem Team-Client (Anrufer) an einen PSTN-Endpunkt (angerufener)</span><span class="sxs-lookup"><span data-stu-id="d6514-118">Outbound calls: Calls from a Teams client (caller) to a PSTN endpoint (callee)</span></span>

<span data-ttu-id="d6514-119">Die Richtlinie wird auf der SBC-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="d6514-119">The policy is applied at the SBC level.</span></span> <span data-ttu-id="d6514-120">Sie können einem SBC mehrere Übersetzungsregeln zuweisen, die in der Reihenfolge angewendet werden, in der Sie angezeigt werden, wenn Sie Sie in PowerShell auflisten.</span><span class="sxs-lookup"><span data-stu-id="d6514-120">You can assign multiple translation rules to an SBC, which are applied in the order that they appear when you list them in PowerShell.</span></span> <span data-ttu-id="d6514-121">Sie können auch die Reihenfolge der Regeln in der Richtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="d6514-121">You can also change the order of the rules in the policy.</span></span>

<span data-ttu-id="d6514-122">Zum Erstellen, ändern, anzeigen und Löschen von Regeln für die Nummern Manipulation verwenden Sie die Cmdlets [New-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/new-csteamstranslationrule), [Sets-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/set-csteamstranslationrule), [Get-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/get-csteamstranslationrule)und [Remove-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/remove-csteamstranslationrule) .</span><span class="sxs-lookup"><span data-stu-id="d6514-122">To create, modify, view, and delete number manipulation rules, use the [New-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/new-csteamstranslationrule), [Set-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/set-csteamstranslationrule), [Get-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/get-csteamstranslationrule), and [Remove-CsTeamsTranslationRule](https://docs.microsoft.com/powershell/module/skype/remove-csteamstranslationrule) cmdlets.</span></span>

<span data-ttu-id="d6514-123">Verwenden Sie die Cmdlets [New-CSOnlinePSTNGateway](https://docs.microsoft.com/powershell/module/skype/new-csonlinepstngateway) und [setCSOnlinePSTNGateway](https://docs.microsoft.com/powershell/module/skype/set-csonlinepstngateway) zusammen mit den Cmdlets InboundTeamsNumberTranslationRules, InboundPSTNNumberTranslationRules, OutboundTeamsNumberTranslationRules, OutboundPSTNNumberTranslationRules, InboundTeamsNumberTranslationRulesList, InboundPSTNNumberTranslationRulesList, OutboundTeamsNumberTranslationRulesList und OutboundPSTNNumberTranslationRulesList, um Regeln für die Nummern Manipulation in SBCS zuzuweisen, zu konfigurieren und zu Listen. Parameter.</span><span class="sxs-lookup"><span data-stu-id="d6514-123">To assign, configure, and list number manipulation rules on SBCs, use the [New-CSOnlinePSTNGateway](https://docs.microsoft.com/powershell/module/skype/new-csonlinepstngateway) and [Set-CSOnlinePSTNGateway](https://docs.microsoft.com/powershell/module/skype/set-csonlinepstngateway) cmdlets together with the  InboundTeamsNumberTranslationRules, InboundPSTNNumberTranslationRules, OutboundTeamsNumberTranslationRules, OutboundPSTNNumberTranslationRules, InboundTeamsNumberTranslationRulesList, InboundPSTNNumberTranslationRulesList, OutboundTeamsNumberTranslationRulesList, and OutboundPSTNNumberTranslationRulesList parameters.</span></span>


## <a name="example-sbc-configuration"></a><span data-ttu-id="d6514-124">Beispiel-SBC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d6514-124">Example SBC configuration</span></span>

<span data-ttu-id="d6514-125">Für dieses Szenario wird das ```New-CsOnlinePSTNGateway``` Cmdlet ausgeführt, um die folgende SBC-Konfiguration zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d6514-125">For this scenario, the ```New-CsOnlinePSTNGateway``` cmdlet is run to create the following SBC configuration:</span></span>

```PowerShell
New-CSOnlinePSTNGateway -Identity sbc1.contoso.com -SipSignalingPort 5061 –InboundTeamsNumberTranslationRulesList ‘AddPlus1’, ‘AddE164SeattleAreaCode’ -InboundPSTNNumberTranslationRulesList ‘AddPlus1’ -OnboundPSTNNumberTranslationRulesList ‘AddSeattleAreaCode’,  -OutboundTeamsNumberTranslationRulesList ‘StripPlus1’
```

<span data-ttu-id="d6514-126">Die dem SBC zugewiesenen Übersetzungsregeln sind in der folgenden Tabelle zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="d6514-126">The translation rules assigned to the SBC are summarized in the following table:</span></span>

|<span data-ttu-id="d6514-127">Name</span><span class="sxs-lookup"><span data-stu-id="d6514-127">Name</span></span>  |<span data-ttu-id="d6514-128">Muster</span><span class="sxs-lookup"><span data-stu-id="d6514-128">Pattern</span></span> |<span data-ttu-id="d6514-129">Übersetzung</span><span class="sxs-lookup"><span data-stu-id="d6514-129">Translation</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="d6514-130">AddPlus1</span><span class="sxs-lookup"><span data-stu-id="d6514-130">AddPlus1</span></span>     |<span data-ttu-id="d6514-131">^ (\d{10}) $</span><span class="sxs-lookup"><span data-stu-id="d6514-131">^(\d{10})$</span></span>          |<span data-ttu-id="d6514-132">+1$1</span><span class="sxs-lookup"><span data-stu-id="d6514-132">+1$1</span></span>          |
|<span data-ttu-id="d6514-133">AddE164SeattleAreaCode</span><span class="sxs-lookup"><span data-stu-id="d6514-133">AddE164SeattleAreaCode</span></span>      |<span data-ttu-id="d6514-134">^ (\d{4}) $</span><span class="sxs-lookup"><span data-stu-id="d6514-134">^(\d{4})$</span></span>          | <span data-ttu-id="d6514-135">+ 1206555 $1</span><span class="sxs-lookup"><span data-stu-id="d6514-135">+1206555$1</span></span>         |
|<span data-ttu-id="d6514-136">AddSeattleAreaCode</span><span class="sxs-lookup"><span data-stu-id="d6514-136">AddSeattleAreaCode</span></span>    |<span data-ttu-id="d6514-137">^ (\d{4}) $</span><span class="sxs-lookup"><span data-stu-id="d6514-137">^(\d{4})$</span></span>          | <span data-ttu-id="d6514-138">425555 $1</span><span class="sxs-lookup"><span data-stu-id="d6514-138">425555$1</span></span>         |
|<span data-ttu-id="d6514-139">StripPlus1</span><span class="sxs-lookup"><span data-stu-id="d6514-139">StripPlus1</span></span>    |<span data-ttu-id="d6514-140">^ + 1 (\d{10}) $</span><span class="sxs-lookup"><span data-stu-id="d6514-140">^+1(\d{10})$</span></span>          | <span data-ttu-id="d6514-141">$1</span><span class="sxs-lookup"><span data-stu-id="d6514-141">$1</span></span>         |

<span data-ttu-id="d6514-142">In den folgenden Beispielen gibt es zwei Benutzer: Alice und Bob.</span><span class="sxs-lookup"><span data-stu-id="d6514-142">In the following examples, there are two users, Alice and Bob.</span></span> <span data-ttu-id="d6514-143">Alice ist ein Team Benutzer, dessen Nummer + 1 206 555 0100 ist.</span><span class="sxs-lookup"><span data-stu-id="d6514-143">Alice is a Teams user whose number is +1 206 555 0100.</span></span> <span data-ttu-id="d6514-144">Bob ist ein PSTN-Benutzer, dessen Nummer + 1 425 555 0100 ist.</span><span class="sxs-lookup"><span data-stu-id="d6514-144">Bob is a PSTN user whose number is +1 425 555 0100.</span></span>

## <a name="example-1-inbound-call-to-a-ten-digit-number"></a><span data-ttu-id="d6514-145">Beispiel 1: eingehender Anruf an eine zehnstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="d6514-145">Example 1: Inbound call to a ten-digit number</span></span>

<span data-ttu-id="d6514-146">Bob ruft Alice mit einer nicht-E. 164-zehnstelligen Zahl an.</span><span class="sxs-lookup"><span data-stu-id="d6514-146">Bob calls Alice using a non-E.164 ten-digit number.</span></span> <span data-ttu-id="d6514-147">Bob wählt 2065550100, um Alice zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d6514-147">Bob dials 2065550100 to reach Alice.</span></span>
<span data-ttu-id="d6514-148">SBC verwendet 2065550100 in den RequestURI und den Headern und 4255550100 im from-Header.</span><span class="sxs-lookup"><span data-stu-id="d6514-148">SBC uses 2065550100 in the RequestURI and To headers and 4255550100 in the From header.</span></span>


|<span data-ttu-id="d6514-149">Header</span><span class="sxs-lookup"><span data-stu-id="d6514-149">Header</span></span>  |<span data-ttu-id="d6514-150">Original</span><span class="sxs-lookup"><span data-stu-id="d6514-150">Original</span></span> |<span data-ttu-id="d6514-151">Übersetzte Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d6514-151">Translated header</span></span> |<span data-ttu-id="d6514-152">Parameter und Regel angewendet</span><span class="sxs-lookup"><span data-stu-id="d6514-152">Parameter and rule applied</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="d6514-153">RequestURI</span><span class="sxs-lookup"><span data-stu-id="d6514-153">RequestURI</span></span>  |<span data-ttu-id="d6514-154">Einladen von SIP:2065550100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-154">INVITE sip:2065550100@sbc.contoso.com</span></span>|<span data-ttu-id="d6514-155">Einladen von SIP:+12065550100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-155">INVITE sip:+12065550100@sbc.contoso.com</span></span>|<span data-ttu-id="d6514-156">InboundTeamsNumberTranslationRulesList 'AddPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-156">InboundTeamsNumberTranslationRulesList ‘AddPlus1’</span></span>|
|<span data-ttu-id="d6514-157">An</span><span class="sxs-lookup"><span data-stu-id="d6514-157">TO</span></span>    |<span data-ttu-id="d6514-158">An: \<SIP:2065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-158">TO: \<sip:2065550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-159">An: \<SIP:+12065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-159">TO: \<sip:+12065550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-160">InboundTeamsNumberTranlationRulesList 'AddPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-160">InboundTeamsNumberTranlationRulesList ‘AddPlus1’</span></span>|
|<span data-ttu-id="d6514-161">Von</span><span class="sxs-lookup"><span data-stu-id="d6514-161">FROM</span></span>   |<span data-ttu-id="d6514-162">Von: \<SIP:4255550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-162">FROM: \<sip:4255550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-163">Von: \<SIP:+14255550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-163">FROM: \<sip:+14255550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-164">InboundPSTNNumberTranslationRulesList 'AddPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-164">InboundPSTNNumberTranslationRulesList ‘AddPlus1’</span></span>|

## <a name="example-2-inbound-call-to-a-four-digit-number"></a><span data-ttu-id="d6514-165">Beispiel 2: eingehende Anrufe an eine vierstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="d6514-165">Example 2: Inbound call to a four-digit number</span></span>

<span data-ttu-id="d6514-166">Bob ruft Alice mit einer vierstelligen Zahl an.</span><span class="sxs-lookup"><span data-stu-id="d6514-166">Bob calls Alice using a four-digit number.</span></span> <span data-ttu-id="d6514-167">Bob wählt 0100, um Alice zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d6514-167">Bob dials 0100 to reach Alice.</span></span>
<span data-ttu-id="d6514-168">SBC verwendet 0100 in den RequestURI und den Headern und 4255550100 im from-Header.</span><span class="sxs-lookup"><span data-stu-id="d6514-168">SBC uses 0100 in the RequestURI and To headers and 4255550100 in the From header.</span></span>


|<span data-ttu-id="d6514-169">Header</span><span class="sxs-lookup"><span data-stu-id="d6514-169">Header</span></span>  |<span data-ttu-id="d6514-170">Original</span><span class="sxs-lookup"><span data-stu-id="d6514-170">Original</span></span> |<span data-ttu-id="d6514-171">Übersetzte Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d6514-171">Translated header</span></span> |<span data-ttu-id="d6514-172">Parameter und Regel angewendet</span><span class="sxs-lookup"><span data-stu-id="d6514-172">Parameter and rule applied</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="d6514-173">RequestURI</span><span class="sxs-lookup"><span data-stu-id="d6514-173">RequestURI</span></span>  |<span data-ttu-id="d6514-174">Einladen von SIP:0100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-174">INVITE sip:0100@sbc.contoso.com</span></span>          |<span data-ttu-id="d6514-175">Einladen von SIP:+12065550100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-175">INVITE sip:+12065550100@sbc.contoso.com</span></span>           |<span data-ttu-id="d6514-176">InboundTeamsNumberTranlationRulesList 'AddE164SeattleAreaCode'</span><span class="sxs-lookup"><span data-stu-id="d6514-176">InboundTeamsNumberTranlationRulesList ‘AddE164SeattleAreaCode’</span></span>        |
|<span data-ttu-id="d6514-177">An</span><span class="sxs-lookup"><span data-stu-id="d6514-177">TO</span></span>    |<span data-ttu-id="d6514-178">An: \<SIP:0100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-178">TO: \<sip:0100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-179">An: \<SIP:+12065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-179">TO: \<sip:+12065550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-180">InboundTeamsNumberTranlationRulesList 'AddE164SeattleAreaCode'</span><span class="sxs-lookup"><span data-stu-id="d6514-180">InboundTeamsNumberTranlationRulesList ‘AddE164SeattleAreaCode’</span></span>         |
|<span data-ttu-id="d6514-181">Von</span><span class="sxs-lookup"><span data-stu-id="d6514-181">FROM</span></span>   |<span data-ttu-id="d6514-182">Von: \<SIP:4255550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-182">FROM: \<sip:4255550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-183">Von: \<SIP:+14255550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-183">FROM: \<sip:+14255550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-184">InboundPSTNNumberTranlationRulesList 'AddPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-184">InboundPSTNNumberTranlationRulesList ‘AddPlus1’</span></span>        |

## <a name="example-3-outbound-call-using-a-ten-digit-non-e164-number"></a><span data-ttu-id="d6514-185">Beispiel 3: ausgehender Anruf mit einer zehnstelligen nicht-E. 164-Nummer</span><span class="sxs-lookup"><span data-stu-id="d6514-185">Example 3: Outbound call using a ten-digit non-E.164 number</span></span>

<span data-ttu-id="d6514-186">Alice ruft Bob mit einer zehnstelligen Zahl an.</span><span class="sxs-lookup"><span data-stu-id="d6514-186">Alice calls Bob using a ten-digit number.</span></span> <span data-ttu-id="d6514-187">Alice wählt 425 555 0100, um Bob zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d6514-187">Alice dials 425 555 0100 to reach Bob.</span></span>
<span data-ttu-id="d6514-188">SBC ist für die Verwendung von nicht-E. 164-Nummern für Teams und PSTN-Benutzer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d6514-188">SBC is configured to use non-E.164 ten-digit numbers for both Teams and PSTN users.</span></span>

<span data-ttu-id="d6514-189">In diesem Szenario übersetzt ein Wählplan die Nummer vor dem Senden an die direkte Routing Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d6514-189">In this scenario, a dial plan translates the number before sending it to the Direct Routing interface.</span></span> <span data-ttu-id="d6514-190">Wenn Alice in den Teams-Client 425 555 0100 eingibt, wird die Nummer im Länder Wählplan in + 14255550100 übersetzt.</span><span class="sxs-lookup"><span data-stu-id="d6514-190">When Alice enters 425 555 0100 in the Teams client, the number is translated to +14255550100 by the country dial plan.</span></span> <span data-ttu-id="d6514-191">Bei den resultierenden Zahlen handelt es sich um eine kumulative Normalisierung der Wähl Plan Regeln und der Übersetzungsregeln für Teams.</span><span class="sxs-lookup"><span data-stu-id="d6514-191">The resulting numbers are a cumulative normalization of the dial plan rules and Teams translation rules.</span></span> <span data-ttu-id="d6514-192">Die Übersetzungsregeln für Teams entfernen das "+ 1", das vom Wählplan hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6514-192">The Teams translation rules remove the "+1" that was added by the dial plan.</span></span>


|<span data-ttu-id="d6514-193">Header</span><span class="sxs-lookup"><span data-stu-id="d6514-193">Header</span></span>  |<span data-ttu-id="d6514-194">Original</span><span class="sxs-lookup"><span data-stu-id="d6514-194">Original</span></span> |<span data-ttu-id="d6514-195">Übersetzte Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d6514-195">Translated header</span></span> |<span data-ttu-id="d6514-196">Parameter und Regel angewendet</span><span class="sxs-lookup"><span data-stu-id="d6514-196">Parameter and rule applied</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="d6514-197">RequestURI</span><span class="sxs-lookup"><span data-stu-id="d6514-197">RequestURI</span></span>  |<span data-ttu-id="d6514-198">Einladen von SIP:+14255550100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-198">INVITE sip:+14255550100@sbc.contoso.com</span></span>          |<span data-ttu-id="d6514-199">Einladen von SIP:4255550100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-199">INVITE sip:4255550100@sbc.contoso.com</span></span>       |<span data-ttu-id="d6514-200">OutboundPSTNNumberTranlationRulesList 'StripPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-200">OutboundPSTNNumberTranlationRulesList ‘StripPlus1’</span></span>         |
|<span data-ttu-id="d6514-201">An</span><span class="sxs-lookup"><span data-stu-id="d6514-201">TO</span></span>    |<span data-ttu-id="d6514-202">An: \<SIP:+14255550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-202">TO: \<sip:+14255550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-203">An: \<SIP:4255555555@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-203">TO: \<sip:4255555555@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-204">OutboundPSTNNumberTranlationRulesList 'StripPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-204">OutboundPSTNNumberTranlationRulesList ‘StripPlus1’</span></span>       |
|<span data-ttu-id="d6514-205">Von</span><span class="sxs-lookup"><span data-stu-id="d6514-205">FROM</span></span>   |<span data-ttu-id="d6514-206">Von: \<SIP:+12065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-206">FROM: \<sip:+12065550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-207">Von: \<SIP:2065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-207">FROM: \<sip:2065550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-208">OutboundTeamsNumberTranlationRulesList 'StripPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-208">OutboundTeamsNumberTranlationRulesList ‘StripPlus1’</span></span>         |

## <a name="example-4-outbound-call-using-a-four-digit-non-e164-number"></a><span data-ttu-id="d6514-209">Beispiel 4: Outbound-Anruf mit einer vierstelligen nicht-E. 164-Nummer</span><span class="sxs-lookup"><span data-stu-id="d6514-209">Example 4: Outbound call using a four-digit non-E.164 number</span></span>

<span data-ttu-id="d6514-210">Alice ruft Bob mit einer vierstelligen Zahl an.</span><span class="sxs-lookup"><span data-stu-id="d6514-210">Alice calls Bob using a four-digit number.</span></span> <span data-ttu-id="d6514-211">Alice verwendet 0100, um Bob von anrufen oder über einen Kontakt zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d6514-211">Alice uses 0100 to reach Bob from Calls or by using a contact.</span></span>
<span data-ttu-id="d6514-212">SBC ist für die Verwendung von nicht-E. 164-vierstelligen Zahlen für Teams-Benutzer und zehnstellige Zahlen für PSTN-Benutzer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d6514-212">SBC is configured to use non-E.164 four-digit numbers for Teams users and ten-digit numbers for PSTN users.</span></span> <span data-ttu-id="d6514-213">In diesem Szenario wird der Wählplan nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="d6514-213">The dial plan isn't applied in this scenario.</span></span>


|<span data-ttu-id="d6514-214">Header</span><span class="sxs-lookup"><span data-stu-id="d6514-214">Header</span></span>  |<span data-ttu-id="d6514-215">Original</span><span class="sxs-lookup"><span data-stu-id="d6514-215">Original</span></span> |<span data-ttu-id="d6514-216">Übersetzte Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d6514-216">Translated header</span></span> |<span data-ttu-id="d6514-217">Parameter und Regel angewendet</span><span class="sxs-lookup"><span data-stu-id="d6514-217">Parameter and rule applied</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="d6514-218">RequestURI</span><span class="sxs-lookup"><span data-stu-id="d6514-218">RequestURI</span></span>  |<span data-ttu-id="d6514-219">Einladen von SIP:0100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-219">INVITE sip:0100@sbc.contoso.com</span></span>           |<span data-ttu-id="d6514-220">Einladen von SIP:4255550100@SBC.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6514-220">INVITE sip:4255550100@sbc.contoso.com</span></span>       |<span data-ttu-id="d6514-221">InboundTeamsNumberTranlationRulesList 'AddSeattleAreaCode'</span><span class="sxs-lookup"><span data-stu-id="d6514-221">InboundTeamsNumberTranlationRulesList ‘AddSeattleAreaCode’</span></span>         |
|<span data-ttu-id="d6514-222">An</span><span class="sxs-lookup"><span data-stu-id="d6514-222">TO</span></span>    |<span data-ttu-id="d6514-223">An: \<SIP:0100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-223">TO: \<sip:0100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-224">An: \<SIP:4255555555@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-224">TO: \<sip:4255555555@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-225">InboundTeamsNumberTranlationRulesList 'AddSeattleAreaCode'</span><span class="sxs-lookup"><span data-stu-id="d6514-225">InboundTeamsNumberTranlationRulesList ‘AddSeattleAreaCode’</span></span>       |
|<span data-ttu-id="d6514-226">Von</span><span class="sxs-lookup"><span data-stu-id="d6514-226">FROM</span></span>   |<span data-ttu-id="d6514-227">Von: \<SIP:+12065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-227">FROM: \<sip:+12065550100@sbc.contoso.com></span></span>|<span data-ttu-id="d6514-228">Von: \<SIP:2065550100@SBC.contoso.com></span><span class="sxs-lookup"><span data-stu-id="d6514-228">FROM: \<sip:2065550100@sbc.contoso.com></span></span>| <span data-ttu-id="d6514-229">InboundPSTNNumberTranlationRulesList 'StripPlus1'</span><span class="sxs-lookup"><span data-stu-id="d6514-229">InboundPSTNNumberTranlationRulesList ‘StripPlus1’</span></span> |

## <a name="see-also"></a><span data-ttu-id="d6514-230">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6514-230">See also</span></span>

[<span data-ttu-id="d6514-231">Planen von direktem Routing</span><span class="sxs-lookup"><span data-stu-id="d6514-231">Plan Direct Routing</span></span>](direct-routing-plan.md)

[<span data-ttu-id="d6514-232">Konfigurieren von direktem Routing</span><span class="sxs-lookup"><span data-stu-id="d6514-232">Configure Direct Routing</span></span>](direct-routing-configure.md)