---
title: Authentifizierung in Microsoft Teams-Räumen
ms.author: dstrome
author: dstrome
ms.reviewer: sohailta
manager: serdars
audience: ITPro
ms.topic: conceptual
ms.service: msteams
f1.keywords:
- NOCSH
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-collaboration
description: Informationen zum Konfigurieren der modernen Authentifizierung für Microsoft Teams-Chatrooms
ms.openlocfilehash: 41a65743e5da851dd8e0197e9382deaf696cd9ec
ms.sourcegitcommit: 975f81d9e595dfb339550625d7cef8ad84449e20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "49662580"
---
# <a name="authentication-in-microsoft-teams-rooms"></a>Authentifizierung in Microsoft Teams-Räumen

Die Kontoverwaltung für Microsoft Teams rooms-Geräte wird auf Anwendungsebene verarbeitet. Die Anwendung stellt eine Verbindung mit Microsoft Teams, Skype for Business und Exchange her, um Ressourcen für das Raumkonto abzurufen, um Anrufe und Besprechungs Erlebnisse zu ermöglichen. Auf dem Gerät werden die Konto Unabhängigkeit beibehalten, damit stets aktivierte Funktionen, Anrufszenarien (für Geräte, die mit einem Anrufplan konfiguriert sind) sowie benutzerdefinierte Lockdown-Mechanismen auf diesen Geräten implementiert werden. Dies bedeutet, dass die Authentifizierung für diese Geräte auf eine andere Weise als für endbenutzergeräte erfolgt.  

Die moderne Authentifizierung wird für alle Kunden empfohlen, die Microsoft Teams rooms-Geräte mit Microsoft 365 oder Office 365 verwenden. Wenn Sie über eine lokale Bereitstellung von Exchange Server oder Skype for Business Server verfügen, konfigurieren Sie die [moderne Hybrid Authentifizierung](https://docs.microsoft.com/office365/enterprise/hybrid-modern-auth-overview) mit Azure Active Directory (Azure AD), um die Verwendung der modernen Authentifizierung zu ermöglichen.

Die moderne Authentifizierung wird in Microsoft Teams rooms Version 4.4.25.0 und höher unterstützt.

## <a name="modern-authentication"></a>Moderne Authentifizierung

Wenn Sie die moderne Authentifizierung in der Microsoft Teams rooms-Anwendung verwenden, wird die Active Directory Authentication Library (Adal) verwendet, um eine Verbindung mit Microsoft Teams, Exchange und Skype for Business herzustellen. Ein Microsoft Teams rooms-Gerät ist ein freigegebenes Gerät und führt einen nächtlichen Neustart durch, um einen reibungslosen Betrieb zu gewährleisten und kritische Betriebssystem-, Treiber-, Firmware-oder Anwendungsupdates zu erhalten. Der moderne Authentifizierungsmechanismus verwendet den Berechtigungs Zuteilungs " [Ressourcenbesitzer Kennwort](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth-ropc) " in OAuth 2,0, der keine Benutzerintervention erfordert. Dies ist einer der wichtigsten Unterschiede zwischen der Funktionsweise der modernen Authentifizierung für Benutzerkonten und Ressourcenkonten, die von der Microsoft Teams rooms-Anwendung verwendet werden. Aus diesem Grund sollten Microsoft Teams rooms-Ressourcenkonten nicht so konfiguriert werden, dass Sie mehrstufige Authentifizierung (MFA), Smartcard-Authentifizierung oder Clientzertifikat basierte Authentifizierung verwenden (die alle für Endbenutzer verfügbar sind).

Der andere wichtige Unterschied zwischen der Funktionsweise der modernen Authentifizierung in Microsoft Teams rooms-Geräten und Endbenutzergeräten besteht darin, dass Sie kein Ressourcenkonto verwenden können, um bedingte Zugriffsrichtlinien auf Geräteebene in Azure Active Directory und Endpoint Manager anzuwenden, da Geräteinformationen bei Verwendung dieses Grant-Typs nicht übergeben werden. Stattdessen können Sie ein Gerät in Microsoft Endpoint Manager registrieren und Konformitätsrichtlinien anwenden, indem Sie die Anleitungen unter [Verwalten von Teams-Besprechungsräumen mit InTune](https://techcommunity.microsoft.com/t5/intune-customer-success/managing-teams-meeting-rooms-with-intune/ba-p/1069230)verwenden.

## <a name="enable-modern-authentication-on-a-microsoft-teams-rooms-device"></a>Aktivieren der modernen Authentifizierung auf einem Microsoft Teams rooms-Gerät

Damit Microsoft Teams rooms die moderne Authentifizierung mit Skype for Business und Exchange verwenden können, aktivieren Sie die clientseitige Einstellung für die moderne Authentifizierung auf dem Microsoft Teams rooms-Gerät. Dies können Sie in den Geräteeinstellungen oder in der XML-Konfigurationsdatei vornehmen.

> [!NOTE]
> Bevor Sie die clientseitige Einstellung für die moderne Authentifizierung aktivieren, stellen Sie sicher, dass Ihre Umgebung ordnungsgemäß eingerichtet ist, um die moderne Authentifizierung zu verwenden.

### <a name="using-device-settings"></a>Verwenden von Geräteeinstellungen

1. Wechseln Sie auf dem Gerät Microsoft Team Rooms zu **mehr** (**.**..).
    
2. Wählen Sie **Einstellungen** aus, und geben Sie dann den Benutzernamen und das Kennwort für den Geräteadministrator ein.
3. Wechseln Sie zur Registerkarte **Konto** , aktivieren Sie die **moderne Authentifizierung**, und wählen Sie dann **Speichern und beenden** aus.

### <a name="using-the-xml-config-file"></a>Verwenden der XML-Konfigurationsdatei

Legen Sie in ihrer SkypeSettings.xml-Datei das moderne Authentifizierungs-XML-Element wie folgt auf **true** fest.

```
<ModernAuthEnabled>True</ModernAuthEnabled>
```

Informationen zum Anwenden der Einstellung finden Sie unter [Verwalten von Microsoft Teams rooms-Konsoleneinstellungen Remote mit einer XML-Konfigurationsdatei](xml-config-file.md).

## <a name="prepare-your-environment-for-modern-authentication"></a>Vorbereiten Ihrer Umgebung für eine moderne Authentifizierung

Bevor Sie beginnen, sollten Sie sich mit den Identitäts Modellen vertraut machen, die mit Office 365 und Azure AD zu verwenden sind. Weitere Informationen finden Sie unter [Office 365-Identitäts Modellen und Azure Active Directory](https://docs.microsoft.com/Office365/Enterprise/about-office-365-identity) sowie bei [Hybrid Identität und Verzeichnissynchronisierung für Microsoft 365 oder Office 365](https://docs.microsoft.com/Office365/Enterprise/plan-for-directory-synchronization).

### <a name="enable-modern-authentication-in-microsoft-365-or-office-365"></a>Aktivieren der modernen Authentifizierung in Microsoft 365 oder Office 365

Informationen zum Aktivieren der modernen Authentifizierung für Exchange Online finden Sie unter [Aktivieren der modernen Authentifizierung in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online). Wenn Sie Skype for Business Online verwenden, sollten Sie auch sicherstellen, dass die moderne Authentifizierung für Skype for Business Online aktiviert ist. Weitere Informationen finden Sie unter [Skype for Business Online: Aktivieren Ihres Mandanten für moderne Authentifizierung](https://aka.ms/SkypeModernAuth).

Wir empfehlen, dass Sie die grundlegenden Authentifizierungsrichtlinien für Exchange Online nicht entfernen oder die Standardauthentifizierung für Ihren Mandanten deaktivieren, bis Sie überprüft haben, dass sich Microsoft Teams rooms-Geräte erfolgreich mit Exchange Online, Teams und Skype for Business Online anmelden können.

Weitere Informationen zum Deaktivieren der Standardauthentifizierung in Exchange Online finden Sie unter [Deaktivieren der Standardauthentifizierung in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/disable-basic-authentication-in-exchange-online).

## <a name="hybrid-modern-authentication"></a>Moderne Hybrid Authentifizierung

Um eine erfolgreiche Authentifizierung für Ihren lokalen Exchange-Server und/oder Skype for Business Server sicherzustellen, müssen Sie sicherstellen, dass das Ressourcenkonto, das mit Microsoft Teams-Räumen verwendet wird, so konfiguriert ist, dass es die Autorisierung von Azure AD erhält. 

Teams rooms die Authentifizierungs Flüsse variieren je nach Authentifizierungskonfiguration. Für Kunden, die eine verwaltete Domäne verwenden, verwendet Teams rooms die [Anmeldeinformationen des OAuth 2,0-Ressourcen Besitzers](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth-ropc) mit Azure Active Directory. Für Kunden, die eine Federated-Domäne verwenden, wird jedoch [OAuth 2,0 SAML Bearer-Assertions Fluss](https://docs.microsoft.com/azure/active-directory/develop/v2-saml-bearer-assertion) verwendet.

> [!NOTE]
> Ihr Identitätsanbieter benötigt möglicherweise bestimmte Konfigurationen oder Einstellungen für die Integration in Azure Active Directory oder Office 365. Wenden Sie sich an Ihren Identitätsanbieter, wenn Sie Hilfe beim Konfigurieren der Authentifizierung mit Teams-Chatrooms benötigen.


### <a name="prerequisites-specific-to-microsoft-teams-rooms"></a>Für Microsoft Teams-Räume spezifische Voraussetzungen

Die Voraussetzungen für die Aktivierung der modernen Authentifizierung in ihrer Hybrid Topologie sind unter [Übersicht über hybride moderne Authentifizierung und Voraussetzungen für die Verwendung mit lokalen Skype for Business-und Exchange-Servern](https://docs.microsoft.com/office365/enterprise/hybrid-modern-auth-overview). Es gelten alle im Artikel besprochenen Voraussetzungen.

Da die Microsoft Teams-Räume jedoch die Autorisierung für das [Kennwort des Ressourcen Besitzers](https://tools.ietf.org/html/rfc6749#section-1.3.3) und die zugrunde liegenden Ruhe-APIs für die moderne Authentifizierung verwenden, sind die folgenden wichtigen Unterschiede zu beachten, die speziell für Microsoft Teams-Räume gelten.

- Sie müssen über Exchange Server 2016 CU8 oder höher oder Exchange Server 2019 CU1 oder höher verfügen.
- Sie müssen über Skype for Business Server 2015 CU5 oder höher oder Skype for Business Server 2019 oder höher verfügen.
- MFA wird unabhängig von der verwendeten Topologie nicht unterstützt.
- Microsoft Teams rooms unterstützt keine fehlenden SIP-und UPN-Konflikte. Sie müssen ein Microsoft Teams rooms-Konto mit dem gleichen UPN und SIP erstellen, damit es funktioniert.
- Wenn Sie einen von Azure AD unterstützten Drittanbieter-Authentifizierungsanbieter verwenden, muss er einen aktiven Authentifizierungs Fluss über WS-Trust unterstützen.
- Verwenden Sie keine Richtlinien für den bedingten Zugriff auf Geräteebene für ein mit der Anwendung konfiguriertes Ressourcenkonto. Dies führt zu Anmeldefehlern. Registrieren Sie stattdessen ein Gerät in Microsoft InTune, und wenden Sie Konformitätsrichtlinien mithilfe der in [Verwalten von Teams-Besprechungsräumen mit InTune](https://techcommunity.microsoft.com/t5/intune-customer-success/managing-teams-meeting-rooms-with-intune/ba-p/1069230)veröffentlichten Anleitungen an.

### <a name="configure-exchange-server"></a>Konfigurieren von Exchange Server

Informationen zum Aktivieren der modernen Hybrid Authentifizierung in Exchange Server finden Sie unter [Konfigurieren von Exchange Server lokal für die Verwendung der modernen Hybrid Authentifizierung](https://docs.microsoft.com/Office365/Enterprise/configure-exchange-server-for-hybrid-modern-authentication).

### <a name="configure-skype-for-business-server"></a>Konfigurieren von Skype for Business Server

Informationen zum Aktivieren der modernen Hybrid Authentifizierung mit Skype for Business Server finden Sie unter [Konfigurieren von Skype for Business lokal für die Verwendung der modernen Hybrid Authentifizierung](https://docs.microsoft.com/Office365/Enterprise/configure-exchange-server-for-hybrid-modern-authentication).

### <a name="remove-or-disable-skype-for-business-and-exchange"></a>Entfernen oder Deaktivieren von Skype for Business und Exchange

Wenn Ihr Setup keine Hybride moderne Authentifizierung zulässt oder Sie die moderne Hybrid Authentifizierung für Exchange oder Skype for Business entfernen oder deaktivieren müssen, lesen Sie [Entfernen oder Deaktivieren der modernen Hybrid Authentifizierung in Skype for Business und Exchange](https://docs.microsoft.com/Office365/Enterprise/remove-or-disable-hybrid-modern-authentication-from-skype-for-business-and-excha).

### <a name="azure-ad-conditional-access"></a>Azure AD-bedingter Zugriff

Sie können ein Ressourcenkonto konfigurieren, das in Microsoft Teams-Räumen für IP/Location-basierter Zugriff verwendet wird. Weitere Informationen finden Sie unter [bedingter Zugriff: Blockieren des Zugriffs nach Standort](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-location).

Es werden keine weiteren Richtlinien für den bedingten Zugriff unterstützt. Weitere Informationen zur Gerätekompatibilität finden Sie unter [Verwalten von Teams-Besprechungsräumen mit InTune](https://techcommunity.microsoft.com/t5/intune-customer-success/managing-teams-meeting-rooms-with-intune/ba-p/1069230).  
