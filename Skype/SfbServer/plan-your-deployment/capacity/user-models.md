---
title: Benutzermodelle in Skype for Business Server
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
manager: serdars
audience: ITPro
ms.topic: conceptual
ms.prod: skype-for-business-itpro
f1.keywords:
- NOCSH
localization_priority: Normal
ms.collection: IT_Skype16
ms.assetid: c551371c-d740-4372-bada-f0d713ec0d33
description: Die hier beschriebenen Benutzermodelle bilden die Grundlage für die Kapazitäts Planungs Maße und-Empfehlungen, die unter Kapazitätsplanung Benutzermodell Verwendung für Skype for Business Server beschrieben werden.
ms.openlocfilehash: f1bf079fa425d98b3619eb4ccd975253784f4fbe
ms.sourcegitcommit: e64c50818cac37f3d6f0f96d0d4ff0f4bba24aef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "41816034"
---
# <a name="user-models-in-skype-for-business-server"></a>Benutzermodelle in Skype for Business Server
 
Die hier beschriebenen Benutzermodelle bilden die Grundlage für die Kapazitäts Planungs Maße und-Empfehlungen, die unter [Kapazitätsplanung Benutzermodell Verwendung für Skype for Business Server](user-model.md)beschrieben werden.
  
## <a name="skype-for-business-server-user-models"></a>Skype for Business Server-Benutzermodelle

In der folgenden Tabelle wird das Benutzermodell für Registrierung, Kontakte, Sofortnachrichten (im) und Anwesenheitsinformationen für Skype for Business Server beschrieben.
  
**Benutzermodell für Umgebung und Registrierung**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Bereitstellungsgröße und Verteilung  <br/> |Es wird eine große Bereitstellung mit drei zentralen Standorten und einem Front-End-Pool pro Standort modelliert.  <br/> |
|Prozentsatz der Active Directory-Benutzer  <br/> |Wir gehen davon aus, dass 70% aller Active Directory-Benutzer in der Organisation für Skype for Business Server aktiviert sind. 80% der aktivierten Benutzer sind täglich bei Skype for Business Server angemeldet (80% Parallelität). Die gleichzeitigen Benutzer sind die Grundlage für die weiteren Zahlenangaben in diesem Abschnitt.  <br/> |
|Active Directory-Änderungen  <br/> |Wir gehen davon aus, dass pro Woche 0,5% der Gesamt Nutzer für Skype for Business in Active Directory erstellt und aktiviert werden und dass 0,5% der Gesamt Nutzer in Active Directory und von Skype for Business jede Woche deaktiviert sind. 5% der Benutzer haben mindestens ein Active Directory-Attribut, das jede Woche geändert wurde.  <br/> |
|Active Directory-Verteilergruppen  <br/> |Wir gehen davon aus, dass die Anzahl der Active Directory-Verteilergruppen in der Organisation dreimal so hoch ist wie die Anzahl aller Benutzer in Active Directory. Die Verteilergruppen haben folgende Größen:  <br/> • 64% haben 2-30-Nutzer  <br/> • 13% haben 31-50-Nutzer  <br/> • 10% haben 51-100-Nutzer  <br/> • 13% haben 101-500-Nutzer  <br/> |
|VoIP-Benutzer (Voice over IP)  <br/> |60% der Skype for Business Server-Benutzer sind für Unified Communications (UC) aktiviert (das heißt, ihre Telefonnummern sind Eigentum von Skype for Business Server).  <br/> |
|Verteilung registrierter Clients  <br/> |65% der Clients führen eine Skype for Business-Software, einschließlich Skype for Business und lync Phone Edition.  <br/> 30% der Clients, die Client Software aus einer früheren lync-Version ausführen.  <br/> 5% der Kunden, die Skype for Business Web App verwenden.  <br/> Wenn die Mobilität aktiviert ist, wird davon ausgegangen, dass 40 % der Benutzer die Mobilität gleichzeitig mit anderen zuvor genannten registrierten Clientoptionen verwenden. In diesem Fall beträgt das MPOP-Verhältnis (Multiple Point Of Presence) für Clients 1:1,9. Wenn die Mobilität deaktiviert ist, beträgt das MPOP-Verhältnis 1:1,5.  <br/> |
|Verteilung von Remotebenutzern  <br/> |70 % der Benutzer verbinden sich intern.  <br/> 30% der Benutzer, die eine Verbindung über einen Edge-Server herstellen (optional können Sie auch einen Director hier haben, aber nicht erforderlich).  <br/> |
|Verteilung von Kontakten  <br/> |Die maximale Anzahl von Kontakten eines Benutzers beträgt 1.000. Weniger als 1 % der Benutzer verfügen über 1.000 Kontakte. Weniger als 25 % der Benutzer verfügen über 100 Kontakte oder mehr.  <br/> Benutzer, die mit einem öffentlichen Netz verbunden sind, verfügen über durchschnittlich 80 Kontakte. Für diese Benutzer gilt Folgendes:  <br/> • 50% der Kontakte sind innerhalb der Organisation. 10 % dieser Benutzer sind Remotebenutzer, die sich von außerhalb der Firewall verbinden.  <br/> • 40% der Kontakte sind Skype-Nutzer.  <br/> • 10% der Kontakte sind von Federated-Partnern.  <br/> Benutzer ohne Verbindung mit einem öffentlichen Netz verfügen über durchschnittlich 50 Kontakte. Für diese Benutzer gilt Folgendes:  <br/> • 80% der Kontakte sind innerhalb der Organisation. 10 % dieser Benutzer sind Remotebenutzer, die sich von außerhalb der Firewall verbinden.  <br/> • 20% der Kontakte sind von Federated-Partnern.  <br/> Jeder Benutzer weist 1 Verteilergruppe in seiner Kontaktliste auf. Für Leistungstest wird davon ausgegangen, dass Verteilergruppen immer erweitert werden.  <br/> |
|Sitzungszeit  <br/> |Eine durchschnittliche Benutzeranmeldesitzung dauert 12 Stunden. Sämtliche Benutzer melden sich innerhalb von 120 Minuten nach dem Sitzungsstart an.  <br/> |
   
**Benutzermodell für Chat und Anwesenheit**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Peer-zu-Peer-Chatsitzungen  <br/> |Jeder Benutzer verfügt über durchschnittlich sechs Peer-zu-Peer-Chatsitzungen pro Tag.  <br/> 10 Chatnachrichten pro Sitzung.  <br/> Jede Nachricht wird durch zwei SIP-Info-Nachrichten und 2 SIP 200-OK-Nachrichten (für die\<Status\> anzeigen wie "Name wird eingegeben") abgeglichen.  <br/> |
|Gruppenchatsitzungen  <br/> |Die durchschnittliche Anzahl der gesendeten Nachrichten in einer Gruppe, in der nur Sofortnachrichten verschickt werden können, liegt bei fünf Nachrichten pro Benutzer.  <br/> Die durchschnittliche Anzahl der im Chatteil einer AV-Konferenz versendeten Nachrichten liegt bei zwei Nachrichten pro Benutzer.  <br/> |
|Abfrage von Anwesenheitsinformationen  <br/> |Insgesamt wird von durchschnittlich 60 Abfragen von Anwesenheitsinformationen pro Benutzer und Stunde ausgegangen. Für jeden Benutzer wird von folgenden Durchschnittswerten ausgegangen:  <br/> • Eine Umfrage pro Tag für das vorhanden sein von Benutzern auf der Registerkarte "Organisation" des Benutzers (aber nicht in der Kontaktliste). Die durchschnittliche Anzahl der nicht-Kontakte auf der Registerkarte "Organisation" des Benutzers beträgt 15 Benutzer. Zwei Anzeigevorgänge für Visitenkarten pro Tag.  <br/> • Eine Anwesenheits Abfrage, wenn der Benutzer auf einen anderen Benutzer klickt, um eine Unterhaltung zu beginnen, die pro Stunde geschätzt wird.  <br/> • Sechs Nutzer suchen pro Stunde. Jedes Mal, wenn eine Suche durchgeführt wird, wird eine Batchabfrage für alle Personen in der Suchergebnisliste gesendet. Wir gehen davon aus, dass die durchschnittliche Größe der Suchergebnisse 20 beträgt. Wenn die Suchergebnisse auf dem Bildschirm verbleiben, wird die Batchabfrage alle 5 Minuten aktualisiert. Wir gehen davon aus, dass es zwei solcher Aktualisierungen pro Stunde geben wird.  <br/> • Wenn der Benutzer eine e-Mail in Outlook öffnet oder in der Vorschau zeigt, wird eine Umfrage des Vorhandenseins von Benutzern in den Feldern "an:" und "cc:" der e-Mail mit einer Schätzung von fünf e-Mails pro Stunde und vier Benutzern pro e-Mail angezeigt.  <br/> |
|Anwesenheitsabonnements  <br/> |Wenn ein Benutzer einen anderen Benutzer als Kontakt hinzufügt,  abonniert  der erste Benutzer fünf Kategorien von Informationen zum zweiten Benutzer. Aktualisierungen dieser Informationskategorien werden automatisch an den ersten Benutzer gesendet. <br/> Für jeden Client wird eine einzige Stapelabonnementanforderung gesendet, um den Anwesenheitsstatus von durchschnittlich 40 Kontakten abzurufen, mit zusätzlich 40 Dialogen zum Abrufen von Anwesenheitsinformationen für Partnerkontakte.  <br/> Die Anwesenheitsinformationen für Mitglieder einer erweiterten Verteilergruppe werden über beständige Anwesenheitsabonnements ermittelt, nicht über Abrufe, und werden als 1 Erweiterung pro Benutzer für jeweils 2 Stunden modelliert.  <br/> Kurze Abonnements treten auf, wenn sich ein Benutzer anmeldet, es gibt ein Stapelverarbeitungs Abonnement für alle Kontakte des Benutzers, und dann meldet sich der Benutzer bald ab. Es wird von 6 kurzen Abonnements pro Benutzer und Stunde ausgegangen, wobei jedes Abonnement 10 Minuten dauert. <br/> |
|Veröffentlichung der Anwesenheit  <br/> |Der Anwesenheitsstatus wird durchschnittlich viermal pro Benutzer und Stunde veröffentlicht, mit einer maximalen Anzahl von 6 Veröffentlichungen pro Benutzer und Stunde.  <br/> |
|Größe des Anwesenheitsdokuments  <br/> |Bei einem vollständigen Anwesenheitsdokument wird von einer durchschnittlichen Größe von 4 KB ausgegangen, mit einer maximalen Größe von 25 KB.  <br/> |
   
In der folgenden Tabelle wird das Benutzermodell für die Adressbuchverwendung beschrieben.
  
**Benutzermodell für die Adressbuchverwendung**

|**Adressbuchsuchmodus**|**Verwendung**|
|:-----|:-----|
|Nur Adressbuchwebabfrage (alle Abfragen werden vom Adressbuch-Webabfragedienst ausgeführt)  <br/> |Vier Präfixabfragen pro Benutzer und Tag.  <br/> 60 exakte Suchabfragen pro Benutzer und Tag. 40 % dieser Abfragen werden als Batchabfragen ausgeführt, mit durchschnittlich 20 Kontakten pro Abfrage. Die übrigen 60 % der Abfragen werden für einen einzelnen Kontakt ausgeführt.  <br/> 25 Fotoabfragen pro Benutzer und Tag. 24 Abfragen für ein einzelnes Foto, die verbleibende Abfrage wird als Batchabfrage mit durchschnittlich 20 Kontakten ausgeführt.  <br/> Eine Suchabfrage für die gesamte Organisation pro Benutzer und Tag.  <br/> |
|Im gemischten Modus werden sowohl die Adressbuchdatei als auch Webabfragen verwendet. Dies ist der Standardmodus.  <br/> |Nur zwei Abfragetypen werden über das Netzwerk ausgeführt, die Suchabfragen für Fotos und für die gesamte Organisation.  <br/> 25 Fotoabfragen pro Benutzer und Tag. 24 Abfragen für ein einzelnes Foto, die verbleibende Abfrage wird als Batchabfrage mit durchschnittlich 20 Kontakten ausgeführt.  <br/> Eine Suchabfrage für die gesamte Organisation pro Benutzer und Tag.  <br/> |
   
In der folgenden Tabelle ist das Konferenzmodell beschrieben.
  
**Konferenzmodell**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Geplante Besprechungen im Vergleich zu Sofortbesprechungen  <br/> |60 % geplant, 40 % ungeplant.  <br/> Bei den geplanten Besprechungen wird von 80 % zugewiesenen Konferenzen ausgegangen, wobei es sich um Instanzen von wiederkehrenden Konferenzen handelt. 10 % sind einmalige offene Besprechungen, 8 % sind einmalige anonyme Besprechungen und 2 % sind einmalige geschlossene Besprechungen.  <br/> |
|Verteilung von Konferenzclients  <br/> |Für geplante Besprechungen:  <br/> • 65% der Konferenz Nutzer nutzen Skype for Business 2016.  <br/> • 5% der Konferenz Nutzer nutzen Skype for Business Web App.  <br/> • 30% der Konferenzbenutzer verwenden frühere Clients, einschließlich lync 2013 und Microsoft lync 2010.  <br/> Für ungeplante Besprechungen:  <br/> • 70% der Konferenz Nutzer nutzen Skype for Business.  <br/> • 30% der Konferenzbenutzer verwenden frühere Clients, einschließlich lync 2013 und Microsoft lync 2010.  <br/> |
|Gleichzeitigkeit von Besprechungen  <br/> |5 % der Benutzer befinden sich während der Arbeitszeiten in Konferenzen. Bei einem Pool mit 80.000 Benutzern können sich daher bis zu 4.000 Benutzer gleichzeitig in Konferenzen befinden.  <br/> |
|Verteilung der Audiofunktion in Besprechungen  <br/> |40 % Kombination aus VoIP-Audio- und Einwahlkonferenzen, mit einem Verhältnis von 3:1 von VoIP-Benutzern zu Einwahlbenutzern.  <br/> 35 % nur VoIP-Audio.  <br/> 15 % nur Audio bei Einwahlkonferenzen.  <br/> 10 % ohne Audio (reine Chatkonferenzen mit durchschnittlich fünf gesendeten Nachrichten pro Benutzer).  <br/> |
|Medienmix für Konferenzen  <br/> |Bei 75 % der Konferenzen handelt es sich um Webkonferenzen mit Audio sowie einigen anderen Methoden für die Zusammenarbeit.  <br/> Für diesen Konferenzen werden die folgenden weiteren Methoden für die Zusammenarbeit genutzt:  <br/> **Hinweis:** Diese Zahlen betragen mehr als 100%, da eine Konferenz mehrere Methoden für die Zusammenarbeit aufweisen kann. <br/> • 50% Add Application Sharing. Es wird davon ausgegangen, dass ein Benutzer Daten mit maximal 1,1 MB pro Sekunde sendet.  <br/> • 50% fügen Chatnachrichten (mit durchschnittlich 2 Nachrichten pro Benutzer) hinzu.  <br/> • 20% fügen Datenzusammenarbeit, einschließlich PowerPoint oder Whiteboard, in diese ein, durchschnittlich 2 PowerPoint-Dateien, die pro Konferenz präsentiert werden, mit einer durchschnittlichen PowerPoint-Dateigröße von 10 MB (ohne eingebettetes Video) oder 30 MB (mit eingebettetem Video). Durchschnitt von 20 Anmerkungen pro Whiteboard.  <br/> • 20% Video hinzufügen. 70 % dieser Benutzer nehmen an Konferenzen teil, für die Mehrfachansicht-Video aktiviert ist, wobei jeder Benutzer 2 bis 3 Videostreams empfängt.  <br/> • 15% fügen Sie freigegebene Notizen hinzu.  <br/> |
|Verteilung der Konferenzteilnehmer  <br/> |50 % interne, authentifizierte Benutzer.  <br/> 25 % authentifizierte Benutzer mit Remotezugriff.  <br/> 15 % anonyme Benutzer.  <br/> 10 % Partnerbenutzer.  <br/> |
|Verteilung für den Besprechungsbeitritt  <br/> |Für die Benutzer wird simuliert, dass sie der Besprechung innerhalb der ersten 5 Minuten beitreten.  <br/> |
   
In normalen Front-End-Pools verfügt Skype for Business Server über eine maximal unterstützte Besprechungsgröße von 250-Benutzern. Jeder Pool kann zu einem bestimmten Zeitpunkt eine Besprechung mit 250 Benutzern hosten. Während eine Besprechung dieser Größe stattfindet, kann der Pool zusätzlich weitere kleinere Konferenzen hosten. Darüber hinaus können Sie Besprechungen mit bis zu 1.000 Benutzern unterstützen, indem Sie einen Pool speziell zum Hosten dieser Besprechungen einrichten. Ausführliche Informationen finden Sie unter [Planen großer Besprechungen in Skype for Business Server](../../plan-your-deployment/conferencing/large-meetings.md).
  
Konferenzen wurden wie folgt simuliert:
  
- 85 % der Konferenzen wiesen vier Teilnehmer auf.
    
- 10 % der Konferenzen wiesen sechs Teilnehmer auf.
    
- 5 % der Konferenzen wiesen elf Teilnehmer auf.
    
- Eine große Konferenz mit 250 Benutzern.
    
Die folgende Tabelle enthält ausführliche Informationen zum Benutzermodell für Konferenzen mit Einwahlbenutzern.
  
**Benutzermodell für Einwahlkonferenzen**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Authentifiziert/anonym  <br/> |70 % der Anrufer treten anonym bei und werden zur Aufzeichnung ihres Namens aufgefordert. 30 % nehmen als authentifizierte Benutzer teil.  <br/> |
|Anrufdauer und Wartemusik  <br/> |Durchschnittliche Anrufdauer ohne Wartemusik: 50 Sekunden.  <br/> Für 50 % der Einwahlbenutzer wird Wartemusik wiedergegeben (durchschnittlich 5 Minuten).  <br/> |
|DTMF (Dual-Tone Multifrequency, Mehrfrequenzverfahren)  <br/> |15 % der Konferenzen, auf die ausschließlich per Einwahl zugegriffen wird, werden per Telefon geleitet. 10 % der gemischten Konferenzen, an denen Einwahlbenutzer teilnehmen, werden ebenfalls per Telefon geleitet.  <br/> 20 % der Konferenzleiter (per Telefon) nutzen 2 DTMF-Befehle pro Konferenz.  <br/> |
|Sprache von Ansagen  <br/> |Bei Simulationen wird Englisch als Ansagensprache verwendet.  <br/> |
   
Die folgende Tabelle enthält ausführliche Informationen zum Benutzermodell für die Konferenzlobby.
  
**Benutzermodell für die Konferenzlobby**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Anzahl von Benutzern in der Lobby  <br/> |5 % der Einwahlbenutzer betreten zunächst die Lobby, 25 % der anderen Benutzer werden zunächst in die Lobby weitergeleitet.  <br/> |
|Zulassen von Benutzern aus der Lobby  <br/> |Bei Simulationen wurden alle Benutzer vom Referenten zugelassen, bevor ein Clienttimeout auftritt.  <br/> |
   
In der folgenden Tabelle ist das Benutzermodell für andere Peer-zu-Peer-Sitzungen beschrieben.
  
**Benutzermodell für Peer-zu-Peer-Sitzungen**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Anwendungsfreigabe  <br/> |Jeder Benutzer nimmt an fünf Peer-zu-Peer-Anwendungsfreigabesitzungen pro Monat teil (durchschnittlich 0,25 Sitzungen pro Tag).  <br/> |
|Dateiübertragung  <br/> |Jeder Benutzer nimmt (im Rahmen einer Chatsitzung) an einer Peer-zu-Peer-Dateiübertragungssitzung pro Monat teil (durchschnittlich 0,05 Sitzungen pro Tag). Die durchschnittliche Größe der in einer Sitzung übertragenen Dateien beträgt 1 MB.  <br/> |
   
In der folgenden Tabelle wird das Benutzermodell für Richtlinien beschrieben.
  
**Benutzermodell für Richtlinien**

|**Kategorie**|**Beschreibung**|
|:-----|:-----|
|Konferenz-, Anwesenheits- und Archivierungsrichtlinien  <br/> |Es wird von einer globalen Richtlinie, zehn Konferenzrichtlinien, vier Archivierungsrichtlinien und zehn Anwesenheitsrichtlinien ausgegangen.  <br/> |
|VoIP-Richtlinie  <br/> |Es wird von einer globalen Richtlinie und zwei Richtlinien pro Standort ausgegangen. 100 % der Standorte verfügen über eine Standortrichtlinie, und 30 % der Benutzer ist eine benutzerbasierte Richtlinie zugewiesen. Pro Standort wird von einem Wählplan und zwei Routen ausgegangen.  <br/> |
   
## <a name="busy-hour"></a>Spitzenzeiten

Die Spitzenauslastung für Peer-zu-Peer-Sitzungen wird basierend auf der Anzahl von Anrufversuchen (Busy Hour Call Attempts, BHCA) zu Spitzenzeiten berechnet. Für diesen Begriff aus der VoIP-Branche wird davon ausgegangen, dass 50 % aller Anrufe an einem Tag innerhalb von 20 % der Gesamtzeit getätigt werden. Der BHCA-Wert wird mithilfe der folgenden Formel berechnet:
  
 `BHCA=(total calls * 0.5) / 1.6`
  
Zur Simulation von Spitzenzeiten wurden in Leistungstests VoIP- und andere Peer-zu-Peer-Sitzungen bei einer Spitzenauslastung mit einer Dauer von mindestens 1,6 Stunden pro Tag ausgeführt.
  
Für die Spitzenauslastung bei Konferenzen wird davon ausgegangen, dass 75 % aller Konferenzen an einem achtstündigen Arbeitstag innerhalb von vier Stunden zu Spitzenzeiten stattfinden. Für diese Spitzenzeiten wird das 1,5-Fache der durchschnittlichen Konferenzauslastung verzeichnet.
  
## <a name="enterprise-voice-to-pstn-calls"></a>Enterprise-VoIP für PSTN-Anrufe

Die folgenden Annahmen gelten für Enterprise-VoIP-Anrufe:
  
- 60% der Benutzer sind für Enterprise-VoIP aktiviert, und 60% dieser Benutzer sind für PSTN-Anrufe aktiviert.
    
- Jeder dieser Benutzer, für den PSTN-Anrufe aktiviert sind, tätigt 4 PSTN-Anrufe in Spitzenzeiten. Jeder Anruf dauert 3 Minuten.
    
- 65 % dieser PST-VoIP-Anrufe verwenden die Medienumgehung.
    
## <a name="mobility"></a>Mobilität

Es wird davon ausgegangen, dass für 40 % der registrierten Benutzer die Mobilität aktiviert ist. Für jeden Benutzer mit aktivierter Mobilität wird davon ausgegangen, dass sich die Aktivität des mobilen Clients zur Aktivität der anderen MPOP-Instanzen für diesen Benutzer summiert. Mit Ausnahme von Konferenzinteraktionen, für die der Mobilitätsclient einfach ein weiterer Clienttyp ist, der für die Teilnahme an Konferenzen verwendet werden kann.
  
## <a name="persistent-chat"></a>Beständiger Chat

Es wird davon ausgegangen, dass 25 % der registrierten Benutzer an Sitzungen für beständigen Chat beteiligt sind, wobei Folgendes gilt:
  
- Durchschnittlich 1,5 Chatrooms pro Benutzer
    
- Jeder Chatroom führt zu 12 Abrufanforderungen pro Stunde, mit einem Zielwert von durchschnittlich je 10 Benutzern
    
## <a name="response-group-and-call-park"></a>Reaktionsgruppe und Parken von Anrufen

Es wird davon ausgegangen, dass 0,15 % der registrierten Benutzer Reaktionsgruppen angehören. Außerdem wird davon ausgegangen, dass 0,02 % der registrierten Benutzer zu einem bestimmten Zeitpunkt Anrufe parken.
  

