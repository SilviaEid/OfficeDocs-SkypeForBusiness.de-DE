---
title: Remoteverwaltung einer Microsoft Teams rooms-Konsoleneinstellungen mit einer XML-Konfigurationsdatei
ms.author: jambirk
author: jambirk
ms.reviewer: gregbari
manager: serdars
audience: ITPro
ms.topic: article
ms.service: msteams
localization_priority: Normal
ms.collection: M365-voice
description: In diesem Artikel wird die Remoteverwaltung der Standardeinstellungen beschrieben, die von einem Microsoft Teams rooms-Gerät verwendet werden, einschließlich der Anwendung eines benutzerdefinierten Designs.
ms.openlocfilehash: ee4e674ff3d518e9f70ff17926bebf99eef65552
ms.sourcegitcommit: 2453f87088fc2f8034726c14699aacb65d859b1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "36436367"
---
# <a name="content-cameras"></a><span data-ttu-id="a0262-103">Content-Kameras</span><span class="sxs-lookup"><span data-stu-id="a0262-103">Content cameras</span></span>

<span data-ttu-id="a0262-104">Sie können jetzt eine Inhalts Kamera mit einem Microsoft Teams Room-System verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0262-104">You can now use a content camera with a Microsoft Teams Room system.</span></span> <span data-ttu-id="a0262-105">Eine Inhalts Kamera interagiert mit spezieller Bildverarbeitungssoftware und einem Whiteboard, damit ein Referent auf einem analogen Whiteboard zeichnen und den Inhalt für Remote Teilnehmer freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="a0262-105">A content camera interacts with special image-processing software and a whiteboard to allow a presenter to draw on an analog whiteboard and share the content with remote participants.</span></span>

<span data-ttu-id="a0262-106">Sehen Sie sich die Video [Arbeit an, wie Sie sich an einem Ort befinden, mit Microsoft Teams-Chatrooms,](https://www.youtube.com/watch?v=1XvgH2rNpmk) um ein Beispiel für die Funktionalität der Inhalts Kamera zu finden.</span><span class="sxs-lookup"><span data-stu-id="a0262-106">See the video [Work like you are in one place, with Microsoft Teams Rooms](https://www.youtube.com/watch?v=1XvgH2rNpmk) for an example of content camera functionality.</span></span>

## <a name="set-up-a-content-camera"></a><span data-ttu-id="a0262-107">Einrichten einer Inhalts Kamera</span><span class="sxs-lookup"><span data-stu-id="a0262-107">Set up a content camera</span></span>

> [!NOTE]
> <span data-ttu-id="a0262-108">Halten Sie sich immer an den GEBÄUDECODE Ihres Landes oder Gebiets fest, der einen Mindestabstand vom Fußboden oder eine Voraussetzung für die Befestigung von decken Geräten an einem Sparren oder einer anderen Struktur definieren kann.</span><span class="sxs-lookup"><span data-stu-id="a0262-108">Always adhere to your country or area's building code, which may define a minimum distance from the floor or a requirement that ceiling-mounted equipment be secured to a rafter or other structure.</span></span> <span data-ttu-id="a0262-109">Befolgen Sie die Einbauanleitung für die Hardware, die mit der ausgewählten Kamera geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0262-109">Follow the mounting instruction for the hardware provided with the camera you‘ve selected.</span></span> <span data-ttu-id="a0262-110">Zu den OEM-Kamera Befestigungskits gehören eine Kamera, USB-2,0-Extender und erforderliche Kabel.</span><span class="sxs-lookup"><span data-stu-id="a0262-110">OEM camera mounting kits include a camera, USB 2.0 extenders and required cabling.</span></span>

<span data-ttu-id="a0262-111">Die Größe des für die Freigabe verwendeten Whiteboards wirkt sich auf die Position der Kamera aus.</span><span class="sxs-lookup"><span data-stu-id="a0262-111">The size of the whiteboard used for sharing affects the placement of the camera.</span></span> <span data-ttu-id="a0262-112">Empfehlungen für die Boardgröße:</span><span class="sxs-lookup"><span data-stu-id="a0262-112">Board size recommendations are:</span></span>

- <span data-ttu-id="a0262-113">3 – 6 ft (0,9 – 1,8 m) breit – unterstützt</span><span class="sxs-lookup"><span data-stu-id="a0262-113">3–6 ft. (0.9–1.8 m) wide — Supported</span></span>
- <span data-ttu-id="a0262-114">1,8 bis 2,7 m breit – empfohlen</span><span class="sxs-lookup"><span data-stu-id="a0262-114">6–9 ft. (1.8–2.7 m) wide — Recommended</span></span>
- <span data-ttu-id="a0262-115">2,7 bis 3,6 m breit – unterstützt</span><span class="sxs-lookup"><span data-stu-id="a0262-115">9–12 ft. (2.7–3.6 m) wide — Supported</span></span>
- <span data-ttu-id="a0262-116">Über 12 ft (3,6 m) breit – Kamera bezieht sich auf 9 bis 12 ft (2,7 bis 3,6 m) und schneidet den anderen ab.</span><span class="sxs-lookup"><span data-stu-id="a0262-116">Above 12 ft. (3.6 m) wide — camera covers 9–12 ft. (2.7–3.6 m) and crops the rest.</span></span>

## <a name="camera-location"></a><span data-ttu-id="a0262-117">Kamerastandort</span><span class="sxs-lookup"><span data-stu-id="a0262-117">Camera location</span></span>

<span data-ttu-id="a0262-118">Die ideale Platzierung einer Inhalts Kamera wird vertikal und horizontal auf dem Whiteboard zentriert.</span><span class="sxs-lookup"><span data-stu-id="a0262-118">Ideal placement of a content camera is centered vertically and horizontally on the whiteboard.</span></span> <span data-ttu-id="a0262-119">Bei lokalen baucodes können Höhen Einschränkungen festgestellt werden, bei denen die Kamera höher als der obere Rand der weißen Tafel sein muss.</span><span class="sxs-lookup"><span data-stu-id="a0262-119">Local building codes may have height restrictions that require the camera be elevated higher than the top of the white board.</span></span>

<span data-ttu-id="a0262-120">Sie können die Kamera bis zu 6 in installieren.</span><span class="sxs-lookup"><span data-stu-id="a0262-120">You can install the camera up to 6 in.</span></span> <span data-ttu-id="a0262-121">(152 mm) über dem oberen Rand des Whiteboards und zentriert auf der weißen Tafel (siehe Abbildung).</span><span class="sxs-lookup"><span data-stu-id="a0262-121">(152 mm) higher than the top of the whiteboard, and centered on the white board as shown.</span></span> <span data-ttu-id="a0262-122">Stellen Sie sicher, dass das Kamerabild mindestens eine 6 in enthält.</span><span class="sxs-lookup"><span data-stu-id="a0262-122">Make sure that the camera image includes at least a 6 in.</span></span> <span data-ttu-id="a0262-123">(152 mm) Rahmen auf beiden Seiten horizontal.</span><span class="sxs-lookup"><span data-stu-id="a0262-123">(152 mm) border on both sides horizontally.</span></span> <span data-ttu-id="a0262-124">Sie können die Kameravorschau in der Microsoft Teams-app "rooms" verwenden, um die endgültige Platzierung der Kamera festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a0262-124">You can use the camera preview in the Microsoft Teams Rooms app to determine final placement of the camera.</span></span>

![Inhalts Kamera-Platzierungs Diagramm](../media/Magic-whiteboard.png)

### <a name="camera-distances"></a><span data-ttu-id="a0262-126">Kamera Abstände</span><span class="sxs-lookup"><span data-stu-id="a0262-126">Camera distances</span></span>

<span data-ttu-id="a0262-127">Bei Verwendung typischer Whiteboard-Marker bietet die optimale Remotebenutzeroberfläche die Freigabe von Freihandstrichen im Bereich von 1 – 2 mm pro Pixel im Bild der Inhalts Kamera, und die besten Ergebnisse verwenden 1,5 mm pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="a0262-127">Using typical whiteboard markers, the optimal remote user experience is to share ink strokes in the 1–2 mm per pixel range in the content camera image, and the best results use 1.5 mm per pixel.</span></span> <span data-ttu-id="a0262-128">Alle unterstützten Kameras bieten eine Auflösung von 1920 x 1080, und einige können diese Auflösung überschreiten.</span><span class="sxs-lookup"><span data-stu-id="a0262-128">All supported cameras provide 1920 x 1080 resolution, and some can exceed that resolution.</span></span>

<span data-ttu-id="a0262-129">Der Abstand der Kamera vom Whiteboard kombiniert sich mit der Kamera Auflösung und HFoV, um den Abstand vom Whiteboard zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a0262-129">The distance of the camera from the whiteboard combines with the camera resolution and HFoV to determine the distance from the whiteboard.</span></span> <span data-ttu-id="a0262-130">Die folgende Tabelle enthält Beispiele für Entfernungen für verschiedene Whiteboard-Größen.</span><span class="sxs-lookup"><span data-stu-id="a0262-130">The following table shows examples of distances for various whiteboard sizes.</span></span> <span data-ttu-id="a0262-131">Sie können diese Werte als Ausgangspunkte verwenden, um die endgültige Platzierung der Inhalts Kamera festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a0262-131">You can use these values as starting points to determine final placement of the content camera.</span></span>

<span data-ttu-id="a0262-132">**Kameraabstand vom Whiteboard**</span><span class="sxs-lookup"><span data-stu-id="a0262-132">**Camera distance from whiteboard**</span></span>

| <span data-ttu-id="a0262-133">Kamera HFoV</span><span class="sxs-lookup"><span data-stu-id="a0262-133">Camera HFoV</span></span> |<span data-ttu-id="a0262-134">0,91 m</span><span class="sxs-lookup"><span data-stu-id="a0262-134">3 ft. (0.91 m)</span></span>     | <span data-ttu-id="a0262-135">1,8 m</span><span class="sxs-lookup"><span data-stu-id="a0262-135">6 ft. (1.8 m)</span></span>    | <span data-ttu-id="a0262-136">2,74 m</span><span class="sxs-lookup"><span data-stu-id="a0262-136">9 ft. (2.74 m)</span></span>        |<span data-ttu-id="a0262-137">12 ft.  (3,65 m)</span><span class="sxs-lookup"><span data-stu-id="a0262-137">12 ft.  (3.65 m)</span></span>         | <span data-ttu-id="a0262-138">Maximale Entfernung vom Whiteboard</span><span class="sxs-lookup"><span data-stu-id="a0262-138">Max distance from Whiteboard</span></span>  |
|:---         |:---               |:---                |:---                 |:---             | :--- |
| <span data-ttu-id="a0262-139">80 °</span><span class="sxs-lookup"><span data-stu-id="a0262-139">80°</span></span>         | <span data-ttu-id="a0262-140">0,54 m (1,79 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-140">1.79 ft. (0.54 m)</span></span> | <span data-ttu-id="a0262-141">1,09 m (3,58 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-141">3.58 ft. (1.09 m)</span></span>  | <span data-ttu-id="a0262-142">1,6 m (5,36 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-142">5.36 ft. (1.6 m)</span></span>    |<span data-ttu-id="a0262-143">2,17 m (7,15 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-143">7.15 ft. (2.17 m)</span></span> |<span data-ttu-id="a0262-144">2,28 m (7,51 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-144">7.51 ft. (2.28 m)</span></span> |
| <span data-ttu-id="a0262-145">90 °</span><span class="sxs-lookup"><span data-stu-id="a0262-145">90°</span></span>         | <span data-ttu-id="a0262-146">0,45 m (1,5 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-146">1.5 ft. (0.45 m)</span></span> | <span data-ttu-id="a0262-147">0,91 m (3,00 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-147">3.00 ft. (0.91 m)</span></span>   | <span data-ttu-id="a0262-148">1,37 m (4,5 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-148">4.5 ft. (1.37 m)</span></span>    |<span data-ttu-id="a0262-149">1,82 m (6,0 Ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-149">6.0 ft. (1.82 m)</span></span>    |<span data-ttu-id="a0262-150">1,92 m (6,3 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-150">6.3 ft. (1.92 m)</span></span> |
| <span data-ttu-id="a0262-151">100 °</span><span class="sxs-lookup"><span data-stu-id="a0262-151">100°</span></span>        | <span data-ttu-id="a0262-152">0,38 m (1,26 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-152">1.26 ft. (0.38 m)</span></span>| <span data-ttu-id="a0262-153">0,77 m (2,52 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-153">2.52 ft. (0.77 m)</span></span>   | <span data-ttu-id="a0262-154">1,15 m (3,78 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-154">3.78 ft. (1.15 m)</span></span>   |<span data-ttu-id="a0262-155">1,53 m (5,03 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-155">5.03 ft. (1.53 m)</span></span>   |<span data-ttu-id="a0262-156">1,61 m (5,29 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-156">5.29 ft. (1.61 m)</span></span> |
| <span data-ttu-id="a0262-157">110 °</span><span class="sxs-lookup"><span data-stu-id="a0262-157">110°</span></span>        | <span data-ttu-id="a0262-158">0,32 m (1,05 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-158">1.05 ft. (0.32 m)</span></span>| <span data-ttu-id="a0262-159">0,64 m (2,10 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-159">2.10 ft. (0.64 m)</span></span>   | <span data-ttu-id="a0262-160">0,96 m (3,15 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-160">3.15 ft. (0.96 m)</span></span>   |<span data-ttu-id="a0262-161">1,28 m (4,2 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-161">4.2 ft. (1.28 m)</span></span>    |<span data-ttu-id="a0262-162">1,31 m (4,41 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-162">4.41 ft. (1.31 m)</span></span> |
| <span data-ttu-id="a0262-163">120 °</span><span class="sxs-lookup"><span data-stu-id="a0262-163">120°</span></span>        | <span data-ttu-id="a0262-164">0,26 m (0,87 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-164">0.87 ft. (0.26 m)</span></span>| <span data-ttu-id="a0262-165">0,52 m (1,73 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-165">1.73 ft. (0.52 m)</span></span>   | <span data-ttu-id="a0262-166">0,79 m (2,60 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-166">2.60 ft. (0.79 m)</span></span>   |<span data-ttu-id="a0262-167">1,05 m (3,46 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-167">3.46 ft. (1.05 m)</span></span>   |<span data-ttu-id="a0262-168">1,10 m (3,64 ft.)</span><span class="sxs-lookup"><span data-stu-id="a0262-168">3.64 ft. (1.10 m)</span></span> |
|             |               |                  |                  |        |                    |                  |

<span data-ttu-id="a0262-169">Der Abstand zwischen der Inhalts Kamera und der Wand, auf der das Whiteboard bereitgestellt wird, hängt vom HFoV für dieses Kameramodell ab, das unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="a0262-169">The distance between the content camera and the wall the whiteboard is mounted on depends on the HFoV for that model of camera, which varies.</span></span> <span data-ttu-id="a0262-170">Installieren Sie Kameras mit einem größeren HFoV (beispielsweise 120 Grad) näher an der Wand, und Kameras mit einem schmaleren HFoV weiter von der Wand entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0262-170">Install cameras with a larger HFoV (120 degrees for example) closer to the wall, and cameras with a narrower HFoV farther away from the wall.</span></span> <span data-ttu-id="a0262-171">Überprüfen Sie die HFoV, bevor Sie mit der Installation der ausgewählten Kamera beginnen.</span><span class="sxs-lookup"><span data-stu-id="a0262-171">Check the HFoV before you start to install the chosen camera.</span></span>

<span data-ttu-id="a0262-172">Wenn Sie über Whiteboards mit einer Größe von mehr als 12 ft (3,65 m) oder ohne Ecken (wie vollständige Wand Whiteboards) verfügen, können Sie die Kamera an einer beliebigen Stelle in der Mitte platzieren.</span><span class="sxs-lookup"><span data-stu-id="a0262-172">If you have whiteboards larger than 12 ft. (3.65 m) or with no corners (like full wall whiteboards), you can place the camera anywhere in the middle.</span></span> <span data-ttu-id="a0262-173">Die Erweiterungssoftware wählt einen Bereich in der Mitte aus, wenn keine Whiteboard-Ecken gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a0262-173">The enhancement software selects an area in the middle if it fails to find whiteboard corners.</span></span>

> [!NOTE]
> <span data-ttu-id="a0262-174">Sie können dunkel gefärbtes Klebeband oder andere Elemente verwenden, um einen definierten Inhalt Kamera Bereich auf einer vollständigen weißen Tafel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0262-174">You can use dark-colored tape or other items to create a defined content camera area on a full-wall white board.</span></span>
>
> <span data-ttu-id="a0262-175">Sie können festlegen, dass die Kamera an einem beweglichen Stativ statt an einer permanenten Halterung montiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0262-175">You can choose to have the camera mounted on a moveable tripod instead of a permanent mount.</span></span> <span data-ttu-id="a0262-176">Setzen Sie das Stativ mittig auf das Whiteboard.</span><span class="sxs-lookup"><span data-stu-id="a0262-176">Place the tripod centered on the whiteboard.</span></span> <span data-ttu-id="a0262-177">Diese Einrichtung kann temporär sein oder verwendet werden, wenn es kaum eine Möglichkeit gibt, das Gerät zu überfallen.</span><span class="sxs-lookup"><span data-stu-id="a0262-177">This setup may be temporary or used where there is little chance of knocking over the equipment.</span></span> <span data-ttu-id="a0262-178">Wenn Sie eine temporäre Halterung verwenden, denken Sie daran, dass die Inhaltserweiterung beeinträchtigt wird, wenn Sie die Kamera nach der ersten Freigabe verschieben und Sie erneut freigeben müssen, um die Bewegung zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="a0262-178">If you use a temporary mount, remember that content enhancement will be impacted if you move the camera after the initial share and you will need to re-share to correct for movement.</span></span>
>
> <span data-ttu-id="a0262-179">Eine Schreibtafel, die nicht weiß ist, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0262-179">A writing board that isn't white is not supported.</span></span>

## <a name="supported-cameras"></a><span data-ttu-id="a0262-180">Unterstützte Kameras</span><span class="sxs-lookup"><span data-stu-id="a0262-180">Supported cameras</span></span>

<span data-ttu-id="a0262-181">Wenn Sie feststellen möchten, ob Sie eine Kamera als Inhalts Kamera verwenden können, lesen Sie [zertifizierte Firmware-Versionen für USB-Audio-und Video-Peripheriegeräte](requirements.md#certified-firmware-versions-for-usb-audio-and-video-peripherals).</span><span class="sxs-lookup"><span data-stu-id="a0262-181">To determine whether you can use a camera as a content camera, refer to [Certified firmware versions for USB audio and video peripherals](requirements.md#certified-firmware-versions-for-usb-audio-and-video-peripherals).</span></span>

<span data-ttu-id="a0262-182">Oder lesen Sie den Microsoft Teams-Gerätemarkt für unterstützte Content Camera Kits unter [aka.ms/teamsdevices](https://aka.ms/teamsdevices).</span><span class="sxs-lookup"><span data-stu-id="a0262-182">Or, refer to the Microsoft Teams devices marketplace for supported Content Camera Kits at [aka.ms/teamsdevices](https://aka.ms/teamsdevices).</span></span>

## <a name="camera-settings"></a><span data-ttu-id="a0262-183">Kameraeinstellungen</span><span class="sxs-lookup"><span data-stu-id="a0262-183">Camera settings</span></span>

<span data-ttu-id="a0262-184">Nachdem Sie die Kamera im Chatroom installiert haben, richten Sie Sie in der Microsoft Teams rooms-Konsole des Chatrooms ein:</span><span class="sxs-lookup"><span data-stu-id="a0262-184">Once the camera is installed in the room, set it up on that room's Microsoft Teams Rooms console:</span></span>

1. <span data-ttu-id="a0262-185">Wählen \*\*\*\* ![Sie das Symbol](../media/70f1b43f-16d6-4172-9139-71d845c4ed5c.png)Einstellungen Einstellungen aus, melden Sie sich als Administrator an, und wählen Sie **Geräteeinstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="a0262-185">Select **Settings** ![Settings icon](../media/70f1b43f-16d6-4172-9139-71d845c4ed5c.png),  log in as Admin, and select **Device Settings**.</span></span>
2. <span data-ttu-id="a0262-186">Wählen Sie im Abschnitt **Camera defaults** die Inhalts Kamera aus, und stellen Sie sicher, dass die Option **Inhalts Erweiterungen** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a0262-186">In the **Camera Defaults** section, select the content camera and make sure that the **Content enhancements** option is selected.</span></span>
3. <span data-ttu-id="a0262-187">Optional Wenn die Kamera auf den Kopf gestellt wurde, weil die Kamera von der Decke montiert wurde, aktivieren Sie die Option " **Inhalts Kamera 180 ° drehen** ".</span><span class="sxs-lookup"><span data-stu-id="a0262-187">(Optional) If the camera was installed upside down because the camera was mounted from the ceiling, check the **Rotate content camera 180°** option.</span></span>
4. <span data-ttu-id="a0262-188">Wählen Sie **Speichern und beenden**aus.</span><span class="sxs-lookup"><span data-stu-id="a0262-188">Select **Save and exit**.</span></span>

![Einrichten der Inhalts Kamera](../media/content-camera.png)

<span data-ttu-id="a0262-190">Sie können diese Einstellungen auch Remote mithilfe einer [XML-Konfigurationsdatei](xml-config-file.md)anpassen.</span><span class="sxs-lookup"><span data-stu-id="a0262-190">You can also adjust these settings remotely using an [XML configuration file](xml-config-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0262-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0262-191">See also</span></span>

[<span data-ttu-id="a0262-192">Remoteverwaltung einer Microsoft Teams rooms-Konsoleneinstellungen mit einer XML-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="a0262-192">Manage a Microsoft Teams Rooms console settings remotely with an XML configuration file</span></span>](xml-config-file.md)

[<span data-ttu-id="a0262-193">Anforderungen für Microsoft Teams-Räume</span><span class="sxs-lookup"><span data-stu-id="a0262-193">Microsoft Teams Rooms requirements</span></span>](requirements.md)