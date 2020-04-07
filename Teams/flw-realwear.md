---
title: Informationen für IT-Administratoren zum Microsoft Teams-für-RealWear-Client (Vorschau)
author: MicrosoftHeidi
ms.author: heidip
manager: serdars
ms.topic: reference
ms.service: msteams
audience: admin
ms.reviewer: ''
description: Eine Erläuterung des Microsoft Teams-für-RealWear-Clients für IT-Administratoren.
localization_priority: Priority
search.appverid: MET150
f1.keywords:
- NOCSH
ms.collection:
- M365-collaboration
- Teams_ITAdmin_RemoteWorkers
- remotework
appliesto:
- Microsoft Teams
ms.openlocfilehash: e95440652111dbcd39b756ef942e7a974ef31de0
ms.sourcegitcommit: dc6108917392754d950cea47b92f871211bf4212
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2020
ms.locfileid: "43131203"
---
# <a name="microsoft-teams-for-realwear"></a><span data-ttu-id="16c2f-103">Microsoft Teams für RealWear</span><span class="sxs-lookup"><span data-stu-id="16c2f-103">Microsoft Teams for RealWear</span></span>

> [!NOTE]
> <span data-ttu-id="16c2f-104">Dies ist eine Vorschauversion oder eine Vorabfunktion.</span><span class="sxs-lookup"><span data-stu-id="16c2f-104">This is a preview or early release feature.</span></span>

<span data-ttu-id="16c2f-105">Dieser Artikel befasst sich mit dem Microsoft Teams-Client für am Kopf getragene RealWear-Geräte.</span><span class="sxs-lookup"><span data-stu-id="16c2f-105">This article covers the Microsoft Teams client for RealWear head-mounted wearables.</span></span> <span data-ttu-id="16c2f-106">Mitarbeiter mit RealWear HMT-1 und HMT-1Z1 können nun über einen Videoanruf in Teams mit einem Remoteexperten zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="16c2f-106">FirstLine Workers using RealWear HMT-1 and HMT-1Z1 can now collaborate with a remote expert using video calling on Teams.</span></span> <span data-ttu-id="16c2f-107">Mithilfe einer sprachgesteuerten Benutzeroberfläche ermöglicht Teams für RealWear, dass Außendienstmitarbeiter die Hände jederzeit frei haben, während das Lagebewusstsein in lauten und gefährlichen Umgebungen aufrechterhalten wird.</span><span class="sxs-lookup"><span data-stu-id="16c2f-107">Through a voice-controlled user interface, Teams for RealWear allows field workers to remain 100% hands-free while maintaining situational awareness in loud and hazardous environments.</span></span> <span data-ttu-id="16c2f-108">Indem sie in Echtzeit zeigen, was sie sehen, können Außendienstmitarbeiter die Zeit zur Lösung von Problemen zu verkürzen und das Risiko eines teuren Ausfalls reduzieren.</span><span class="sxs-lookup"><span data-stu-id="16c2f-108">By showing what they see in real-time, field workers can accelerate the time to resolve issues and reduce the risk of an expensive downtime.</span></span>

## <a name="how-to-deploy-microsoft-teams-for-realwear"></a><span data-ttu-id="16c2f-109">Wie man Microsoft Teams für RealWear einsetzt</span><span class="sxs-lookup"><span data-stu-id="16c2f-109">How to deploy Microsoft Teams for RealWear</span></span>

<span data-ttu-id="16c2f-110">Der Microsoft Teams-Client für RealWear befindet sich derzeit in der Public Preview.</span><span class="sxs-lookup"><span data-stu-id="16c2f-110">Microsoft Teams client for RealWear is currently in Public Preview.</span></span> <span data-ttu-id="16c2f-111">Um an dieser Vorschau teilzunehmen, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16c2f-111">To participate in this preview, you will need the following:</span></span>

<span data-ttu-id="16c2f-112">RealWear-Geräte, die auf Version 10.5.0 oder höher aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="16c2f-112">RealWear devices updated to release 10.5.0 or above.</span></span> <span data-ttu-id="16c2f-113">Weitere Informationen finden Sie [hier](https://realwear.com/knowledge-center/configure-on-release-10/wireless-update/).</span><span class="sxs-lookup"><span data-stu-id="16c2f-113">More information [here](https://realwear.com/knowledge-center/configure-on-release-10/wireless-update/).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16c2f-114">Registrieren Sie sich [hier](https://www.realwear.com/solutions/microsoft-teams/#C1) für den Zugriff auf den Teams für RealWear-Client in [RealWear Foresight](https://cloud.realwear.com/).</span><span class="sxs-lookup"><span data-stu-id="16c2f-114">Register [here](https://www.realwear.com/solutions/microsoft-teams/#C1) for access to Teams for RealWear client in [RealWear Foresight](https://cloud.realwear.com/).</span></span>

## <a name="required-licenses"></a><span data-ttu-id="16c2f-115">Erforderliche Lizenzen</span><span class="sxs-lookup"><span data-stu-id="16c2f-115">Required Licenses</span></span>

<span data-ttu-id="16c2f-116">Microsoft Teams-Lizenzen sind Bestandteil von Office 365-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="16c2f-116">Microsoft Teams licenses are part of Office 365 subscriptions.</span></span> <span data-ttu-id="16c2f-117">Für die Nutzung von Teams für RealWear sind keine weiteren Lizenzen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="16c2f-117">No additional licensing is required to use Teams for RealWear.</span></span> <span data-ttu-id="16c2f-118">Weitere Informationen zum Erhalten von Teams finden Sie unter [Wie erhalte ich Zugriff auf Microsoft Teams?](https://support.office.com/article/fc7f1634-abd3-4f26-a597-9df16e4ca65b).</span><span class="sxs-lookup"><span data-stu-id="16c2f-118">For more information about getting Teams, check out [How do I get access to Microsoft Teams](https://support.office.com/article/fc7f1634-abd3-4f26-a597-9df16e4ca65b).</span></span>

## <a name="managing-realwear-devices"></a><span data-ttu-id="16c2f-119">Verwalten von RealWear-Geräten</span><span class="sxs-lookup"><span data-stu-id="16c2f-119">Managing RealWear devices</span></span>

### <a name="microsoft-endpoint-manager"></a><span data-ttu-id="16c2f-120">Microsoft Endpunkt-Manager</span><span class="sxs-lookup"><span data-stu-id="16c2f-120">Microsoft Endpoint Manager</span></span>

<span data-ttu-id="16c2f-121">RealWear-Geräte können über den Modus „Android-Geräteadministrator“ verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="16c2f-121">RealWear devices can be managed using Android Device Administrator mode.</span></span> <span data-ttu-id="16c2f-122">Die Unterstützung für die Verwaltung über Android Enterprise ist begrenzt, da auf den Geräten derzeit keine Google Mobile-Dienste (GMS) zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="16c2f-122">Support for management via Android Enterprise is limited, as the devices currently don't have Google Mobile Services (GMS) available.</span></span>

- <span data-ttu-id="16c2f-123">Weitere Informationen zum Verwalten von RealWear-Geräten in Microsoft Endpoint Manager finden Sie unter [Registrierung von Android-Geräteadministratoren in Intune](https://docs.microsoft.com/mem/intune/enrollment/android-enroll-device-administrator).</span><span class="sxs-lookup"><span data-stu-id="16c2f-123">To learn more about managing RealWear devices on Microsoft Endpoint Manager, see [Android device administrator enrollment in Intune](https://docs.microsoft.com/mem/intune/enrollment/android-enroll-device-administrator).</span></span>
- <span data-ttu-id="16c2f-124">Weitere Informationen zu Richtlinien finden Sie unter [Verwenden von InTune in Umgebungen ohne Google Mobile Services](https://docs.microsoft.com/mem/intune/apps/manage-without-gms).</span><span class="sxs-lookup"><span data-stu-id="16c2f-124">For more details on policies, see [How to use Intune in environments without Google Mobile Services](https://docs.microsoft.com/mem/intune/apps/manage-without-gms).</span></span>

### <a name="third-party-enterprise-mobility-managers-emms"></a><span data-ttu-id="16c2f-125">Drittanbieter für Enterprise Mobility-Manager (EMMs)</span><span class="sxs-lookup"><span data-stu-id="16c2f-125">Third-party Enterprise Mobility Managers (EMMs)</span></span>

<span data-ttu-id="16c2f-126">Anleitungen zu EMM von Drittanbietern finden Sie unter [Unterstützte Enterprise Mobility-Verwaltungsanbieter](https://www.realwear.com/knowledge-center/configure-on-release-10/remote-from-a-web-browser/emm/).</span><span class="sxs-lookup"><span data-stu-id="16c2f-126">For guidance on third-party EMMs, see [Supported Enterprise Mobility Management Providers](https://www.realwear.com/knowledge-center/configure-on-release-10/remote-from-a-web-browser/emm/).</span></span>

## <a name="end-user-content"></a><span data-ttu-id="16c2f-127">Endbenutzer-Inhalte</span><span class="sxs-lookup"><span data-stu-id="16c2f-127">End-user content</span></span>

<span data-ttu-id="16c2f-128">Wenn Sie weitere Inhalte aus der Sicht des Endbenutzers lesen möchten, finden Sie diese unter [Verwenden von Microsoft Teams für RealWear](https://support.office.com/article/using-microsoft-teams-for-realwear-af20d232-d18c-476f-8031-843a4edccd5f).</span><span class="sxs-lookup"><span data-stu-id="16c2f-128">For further reading on this from an end-user perspective, please check out [Using Microsoft Teams for RealWear](https://support.office.com/article/using-microsoft-teams-for-realwear-af20d232-d18c-476f-8031-843a4edccd5f).</span></span>