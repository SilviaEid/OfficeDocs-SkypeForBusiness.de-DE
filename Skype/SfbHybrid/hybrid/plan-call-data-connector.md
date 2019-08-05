---
title: Plan Call Data Connector | Anrufqualität Dashboard Monitoring Hybrid Analytics
ms.reviewer: ''
ms.author: crowe
author: CarolynRowe
manager: serdars
audience: ITPro
ms.topic: article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.collection: ''
description: Übersicht über die Verwendung Skype for Business Online Telemetrie-Tools zum Überwachen einer lokalen Implementierung in einem Hybrid Szenario.
ms.openlocfilehash: dc129ed99e1ed69e3faf5d2a7b6923f818c482eb
ms.sourcegitcommit: ab47ff88f51a96aaf8bc99a6303e114d41ca5c2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2019
ms.locfileid: "36160589"
---
# <a name="plan-call-data-connector"></a><span data-ttu-id="40d56-103">Planen des Connectors für die Anrufdaten</span><span class="sxs-lookup"><span data-stu-id="40d56-103">Plan Call Data Connector</span></span>

## <a name="overview"></a><span data-ttu-id="40d56-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="40d56-104">Overview</span></span>

<span data-ttu-id="40d56-105">In diesem Thema werden die Vorteile, Planungsüberlegungen und Anforderungen für die Implementierung Skype for Business Server Anrufdaten-Konnektors beschrieben.</span><span class="sxs-lookup"><span data-stu-id="40d56-105">This topic describes benefits, planning considerations, and requirements for implementing Skype for Business Server Call Data Connector.</span></span> <span data-ttu-id="40d56-106">Weitere Informationen zum Konfigurieren des Anruf datenkonnektors finden Sie unter [configure Call Data Connector](configure-call-data-connector.md).</span><span class="sxs-lookup"><span data-stu-id="40d56-106">For more information on configuring Call Data Connector, see [Configure Call Data Connector](configure-call-data-connector.md).</span></span>

> [!NOTE]
> <span data-ttu-id="40d56-107">Im öffentlichen Preview-Release steht nur das anrufanalyse-Dashboard zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="40d56-107">At public preview release, only Call Analytics dashboard is available.</span></span>

<span data-ttu-id="40d56-108">Call Data Connector vereinfacht die Anrufüberwachung in einer Hybridumgebung erheblich, da Sie nicht mehr unterschiedliche Sätze von lokalen und Online Tools verwenden müssen, um die Anrufqualität Ihrer Benutzer zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="40d56-108">Call Data Connector greatly simplifies call monitoring in a hybrid environment because you no longer need to use different sets of on-premises and online tools to monitor all of your users call quality.</span></span> <span data-ttu-id="40d56-109">Unabhängig davon, ob Ihre Benutzer lokal oder online verwaltet werden, können Sie die Anrufqualität für Ihre gesamte Organisation online anzeigen.</span><span class="sxs-lookup"><span data-stu-id="40d56-109">Whether your users are homed on premises or online, you can choose to view call quality for your entire organization online.</span></span>

<span data-ttu-id="40d56-110">Mit dem Call Data Connector können Sie die folgenden Aufgaben mithilfe eines einzelnen Toolsets ausführen:</span><span class="sxs-lookup"><span data-stu-id="40d56-110">With Call Data Connector, you can perform the following tasks by using a single toolset:</span></span>

- <span data-ttu-id="40d56-111">Überwachen Sie die Benutzeroberfläche in Microsoft Teams, Skype for Business Online und Skype for Business Server.</span><span class="sxs-lookup"><span data-stu-id="40d56-111">Monitor your user experience across Microsoft Teams, Skype for Business Online, and Skype for Business Server.</span></span>

- <span data-ttu-id="40d56-112">Anzeigen und Beheben von Problemen in Ihrem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="40d56-112">View and troubleshoot problems across your network.</span></span>

- <span data-ttu-id="40d56-113">Zuweisen von Helpdesk-und Administratorrollen für die anrufanalyse, sodass Sie Helpdesk-Mitarbeitern die Möglichkeit geben können, ihre Zuständigkeitsbereiche anzuzeigen und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="40d56-113">Assign helpdesk and administrator roles for Call Analytics, so that you can empower helpdesk workers to view and troubleshoot their areas of responsibility.</span></span>

<span data-ttu-id="40d56-114">Mit dem Anrufdaten-Konnektor legt das Skype for Business Server Anrufdaten an den clouddienst weiter, damit Sie die Tools für die Skype for Business Online Call Analytics (ca) und CQD (Call Quality Dashboard) nutzen können, wie im folgenden Diagramm dargestellt:</span><span class="sxs-lookup"><span data-stu-id="40d56-114">With Call Data Connector, the Skype for Business Server pushes call data to the cloud service so that you can leverage the Skype for Business Online Call Analytics (CA) and Call Quality Dashboard (CQD) tools, as shown in the following diagram:</span></span>

![SFB Cloud Voicemail](../../sfbserver2019/media/call-data-connector-plan-1.png)

<span data-ttu-id="40d56-116">Der Server drückt sowohl QoE-(Quality of Experience) als auch KDS-Daten (Call Detail Recording) an den Onlinedienst aus.</span><span class="sxs-lookup"><span data-stu-id="40d56-116">The server pushes both Quality of Experience (QoE) and Call Detail Recording (CDR) data to the online service.</span></span>

<span data-ttu-id="40d56-117">Mit den Tools für die anrufanalyse und das CQD können Sie die Qualität von Anrufen überwachen und Verbindungsprobleme mit Microsoft Teams und Skype for Business Diensten wie folgt beheben:</span><span class="sxs-lookup"><span data-stu-id="40d56-117">The Call Analytics and CQD tools enable you to monitor the quality of calls and troubleshoot connection problems with Microsoft Teams and Skype for Business services as follows:</span></span>

- <span data-ttu-id="40d56-118">Die anrufanalyse konzentriert sich auf Qualitätsprobleme mit bestimmten anrufen.</span><span class="sxs-lookup"><span data-stu-id="40d56-118">Call Analytics focuses on quality problems with specific calls.</span></span> <span data-ttu-id="40d56-119">Es werden detaillierte Informationen zu anrufen und Besprechungen für jeden Benutzer in einem Skype for Business Konto angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40d56-119">It shows detailed information about calls and meetings for each user in a Skype for Business account.</span></span>  <span data-ttu-id="40d56-120">Mit der anrufanalyse können Sie einer Helpdesk-Vermittlungsstelle Berechtigungen zuweisen, die Anrufe dann überwachen können, ohne Zugriff auf den Rest des Skype for Business admin Centers zu haben.</span><span class="sxs-lookup"><span data-stu-id="40d56-120">With Call Analytics, you can assign permissions to a helpdesk operator who can then monitor calls without having access to the rest of the Skype for Business Admin center.</span></span>

- <span data-ttu-id="40d56-121">Das Dashboard für die Anrufqualität konzentriert sich auf die Netzwerkleistung und die Probleme in einer Organisation.</span><span class="sxs-lookup"><span data-stu-id="40d56-121">Call Quality Dashboard focuses on network performance and issues across an organization.</span></span> <span data-ttu-id="40d56-122">Skype for Business Administratoren und Netzwerktechniker verwenden dieses Tool zur Problembehandlung und Optimierung der Netzwerkleistung.</span><span class="sxs-lookup"><span data-stu-id="40d56-122">Skype for Business administrators and network engineers use this tool to troubleshoot and optimize network performance.</span></span>

<span data-ttu-id="40d56-123">Weitere Informationen finden Sie unter [anrufanalyse und Anruf Qualitäts Dashboard](https://docs.microsoft.com/SkypeForBusiness/using-call-quality-in-your-organization/difference-between-call-analytics-and-call-quality-dashboard).</span><span class="sxs-lookup"><span data-stu-id="40d56-123">For more information, see [Call Analytics and Call Quality Dashboard](https://docs.microsoft.com/SkypeForBusiness/using-call-quality-in-your-organization/difference-between-call-analytics-and-call-quality-dashboard).</span></span>

<span data-ttu-id="40d56-124">Natürlich möchten Sie möglicherweise einige Daten zur Anrufqualität lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="40d56-124">Of course, you might want to keep some call quality data on premises.</span></span> <span data-ttu-id="40d56-125">Dies kann beispielsweise der Fall sein, wenn Sie eine Drittanbieterlösung mit angepassten Berichten und Workflows verwenden.</span><span class="sxs-lookup"><span data-stu-id="40d56-125">This might be the case, for example, if you are using a third-party solution with customized reports and workflows.</span></span>  <span data-ttu-id="40d56-126">Mit Call Data Connector können Sie das Senden von Daten an den Onlinedienst konfigurieren und gleichzeitig eine Kopie der Daten auf dem lokalen Server speichern, wie im folgenden Diagramm dargestellt:</span><span class="sxs-lookup"><span data-stu-id="40d56-126">Call Data Connector allows you to configure sending data to the online service while also keeping a copy of the data on your on-premises server, as shown in the following diagram:</span></span>

![SFB Cloud Voicemail](../../sfbserver2019/media/call-data-connector-plan-2.png)

## <a name="requirements"></a><span data-ttu-id="40d56-128">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="40d56-128">Requirements</span></span>

<span data-ttu-id="40d56-129">Bei den folgenden Anforderungen wird vorausgesetzt, dass Sie bereits Skype for Business Server in einer unterstützten Topologie bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="40d56-129">The following requirements assume that you already have Skype for Business Server deployed in a supported topology.</span></span>  <span data-ttu-id="40d56-130">Weitere Informationen zum Bereitstellen von Skype for Business Server und unterstützten Topologien finden Sie unter [Topologie Basics](https://docs.microsoft.com/SkypeForBusiness/plan-your-deployment/topology-basics/topology-basics).</span><span class="sxs-lookup"><span data-stu-id="40d56-130">For more information about deploying Skype for Business Server and supported topologies, see [Topology Basics](https://docs.microsoft.com/SkypeForBusiness/plan-your-deployment/topology-basics/topology-basics).</span></span> <span data-ttu-id="40d56-131">Zum Konfigurieren von Call Data Connector müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="40d56-131">To configure Call Data Connector, you must:</span></span>

- <span data-ttu-id="40d56-132">Aktivieren Sie die Hybrid Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="40d56-132">Enable Hybrid connectivity.</span></span> <span data-ttu-id="40d56-133">Wenn Sie bereits Skype for Business Server bereitgestellt haben und den Anruf Datenkonnektor aktivieren möchten, müssen Sie sicherstellen, dass Sie eine hybride Konnektivität zwischen Ihren lokalen und Online-Umgebungen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="40d56-133">If you already have Skype for Business Server deployed and you want to enable Call Data Connector, you must ensure that you have hybrid connectivity set up between your on-premises and online environments.</span></span> <span data-ttu-id="40d56-134">Dies wird manchmal als geteilte Domänenkonfiguration bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="40d56-134">This is sometimes called a split domain configuration.</span></span>

   <span data-ttu-id="40d56-135">Weitere Informationen finden Sie unter [Planen der Hybrid Konnektivität zwischen Skype for Business Server und Office 365](plan-hybrid-connectivity.md) und [Konfigurieren der Hybrid Konnektivität zwischen Skype for Business Server und Office 365](configure-hybrid-connectivity.md).</span><span class="sxs-lookup"><span data-stu-id="40d56-135">For more information, see [Plan hybrid connectivity between Skype for Business Server and Office 365](plan-hybrid-connectivity.md) and [Configure hybrid connectivity between Skype for Business Server and Office 365](configure-hybrid-connectivity.md).</span></span>

- <span data-ttu-id="40d56-136">Authentifizieren Sie sich bei Ihrem Office 365 Mandanten, und stellen Sie sicher, dass die folgenden Rollen aktiviert sind:</span><span class="sxs-lookup"><span data-stu-id="40d56-136">Authenticate to your Office 365 tenant and ensure that you have the following roles enabled:</span></span>

  - <span data-ttu-id="40d56-137">Skype for Business Server Administrator</span><span class="sxs-lookup"><span data-stu-id="40d56-137">Skype for Business Server Administrator</span></span>
  - <span data-ttu-id="40d56-138">Office 365 globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="40d56-138">Office 365 Global Administrator</span></span>

- <span data-ttu-id="40d56-139">Wenn Sie dies noch nicht getan haben, aktivieren Sie das Anruf qualitätsdashboard wie unter [aktivieren und Verwenden des Anruf Qualitäts Dashboards für Microsoft Teams und Skype for Business Online](/microsoftteams/turning-on-and-using-call-quality-dashboard)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="40d56-139">If you have not already done so, turn on Call Quality Dashboard as described in [Turning on and using Call Quality Dashboard for Microsoft Teams and Skype for Business Online](/microsoftteams/turning-on-and-using-call-quality-dashboard).</span></span>

- <span data-ttu-id="40d56-140">Aktivieren Sie den Front-End-Pool für die Überwachung mit lokalen LCSCdr-und QoEMetrics-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="40d56-140">Enable the front end pool for Monitoring, with local LCSCdr and QoEMetrics databases.</span></span> <span data-ttu-id="40d56-141">Ohne diesen Parameter verfügt der Anrufdaten-Konnektor nicht über Metrikdaten, mit denen Sie arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="40d56-141">Without this, Call Data Connector won't have metrics data to work with.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40d56-142">Der Anrufdaten-Konnektor funktioniert nicht, wenn die Überwachung im Front-End-Pool nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="40d56-142">Call Data Connector will not function if Monitoring is not enabled on the front end pool.</span></span>

## <a name="comparison-of-on-premises-and-online-call-quality-dashboard-cqd-reports"></a><span data-ttu-id="40d56-143">Vergleich von CQD-Berichten (on-premises und Online Call Quality Dashboard)</span><span class="sxs-lookup"><span data-stu-id="40d56-143">Comparison of on-premises and online Call Quality Dashboard (CQD) reports</span></span>

| <span data-ttu-id="40d56-144">Funktions Berichte</span><span class="sxs-lookup"><span data-stu-id="40d56-144">Feature reports</span></span> | <span data-ttu-id="40d56-145">Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="40d56-145">Skype for Business Online</span></span> | <span data-ttu-id="40d56-146">Skype for Business Server</span><span class="sxs-lookup"><span data-stu-id="40d56-146">Skype for Business Server</span></span>   |
|:---------------------------|:---------------------|:---------------------|:------------------|
| <span data-ttu-id="40d56-147">Metrik für die Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="40d56-147">Application sharing metric</span></span> |<span data-ttu-id="40d56-148">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-148">Yes</span></span> | <span data-ttu-id="40d56-149">Beschränkt</span><span class="sxs-lookup"><span data-stu-id="40d56-149">Limited</span></span> |
| <span data-ttu-id="40d56-150">Informationen zum Kunden Gebäude</span><span class="sxs-lookup"><span data-stu-id="40d56-150">Customer building information</span></span>| <span data-ttu-id="40d56-151">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-151">Yes</span></span> | <span data-ttu-id="40d56-152">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-152">Yes</span></span> |
| <span data-ttu-id="40d56-153">Drilldown-Analyse</span><span class="sxs-lookup"><span data-stu-id="40d56-153">Drill-down analytics</span></span> | <span data-ttu-id="40d56-154">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-154">Yes</span></span> | <span data-ttu-id="40d56-155">Nein</span><span class="sxs-lookup"><span data-stu-id="40d56-155">No</span></span> |
| <span data-ttu-id="40d56-156">Metriken für die Medien Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="40d56-156">Media reliability metrics</span></span> | <span data-ttu-id="40d56-157">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-157">Yes</span></span> | <span data-ttu-id="40d56-158">Beschränkt</span><span class="sxs-lookup"><span data-stu-id="40d56-158">Limited</span></span> |
| <span data-ttu-id="40d56-159">Out-of-the-Box-Berichte</span><span class="sxs-lookup"><span data-stu-id="40d56-159">Out-of-the-box reports</span></span> | <span data-ttu-id="40d56-160">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-160">Yes</span></span> | <span data-ttu-id="40d56-161">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-161">Yes</span></span> |
| <span data-ttu-id="40d56-162">Übersicht Berichte</span><span class="sxs-lookup"><span data-stu-id="40d56-162">Overview reports</span></span> | <span data-ttu-id="40d56-163">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-163">Yes</span></span> | <span data-ttu-id="40d56-164">Nein</span><span class="sxs-lookup"><span data-stu-id="40d56-164">No</span></span> |
| <span data-ttu-id="40d56-165">Berichte pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="40d56-165">Per user reports</span></span> | <span data-ttu-id="40d56-166">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-166">Yes</span></span> | <span data-ttu-id="40d56-167">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-167">Yes</span></span> |
| <span data-ttu-id="40d56-168">Anpassung des Berichtssatzes</span><span class="sxs-lookup"><span data-stu-id="40d56-168">Report set customization</span></span> <br> <span data-ttu-id="40d56-169">(hinzufügen, löschen, Ändern von Berichten)</span><span class="sxs-lookup"><span data-stu-id="40d56-169">(add, delete, modify reports)</span></span> | <span data-ttu-id="40d56-170">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-170">Yes</span></span> | <span data-ttu-id="40d56-171">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-171">Yes</span></span> |
| <span data-ttu-id="40d56-172">Metriken für die Video basierte Bildschirmfreigabe</span><span class="sxs-lookup"><span data-stu-id="40d56-172">Video-based screen sharing metrics</span></span> | <span data-ttu-id="40d56-173">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-173">Yes</span></span> | <span data-ttu-id="40d56-174">Nein</span><span class="sxs-lookup"><span data-stu-id="40d56-174">No</span></span> |
| <span data-ttu-id="40d56-175">Daten-APIs für den programmatischen Zugriff</span><span class="sxs-lookup"><span data-stu-id="40d56-175">Data APIs for programmatic access</span></span> <br> <span data-ttu-id="40d56-176">zu CQD</span><span class="sxs-lookup"><span data-stu-id="40d56-176">to CQD</span></span> | <span data-ttu-id="40d56-177">Nein</span><span class="sxs-lookup"><span data-stu-id="40d56-177">No</span></span> | <span data-ttu-id="40d56-178">Ja</span><span class="sxs-lookup"><span data-stu-id="40d56-178">Yes</span></span> |
||||