# LETCOOR 1.0.0 — Vollständige Benutzerdokumentation

> Dokumentation auf Grundlage des tatsächlichen **LETCOOR 1.0.0**-Quellcodes, der am 30. Oktober 2026 bereitgestellt wurde.
> Diese Dokumentation beschreibt die tatsächlich von der Android-/Windows-Anwendung und der aktuellen Benutzeroberfläche bereitgestellten Funktionen.

---

## Inhaltsverzeichnis

1. [Erste Schritte: Geräte verbinden](#1-erste-schritte-geräte-verbinden)
2. [Wichtige Berechtigungen, besonders offline](#2-wichtige-berechtigungen-besonders-offline)
3. [Eine Gruppe erstellen oder ihr beitreten](#3-eine-gruppe-erstellen-oder-ihr-beitreten)
4. [Den Hauptbildschirm verstehen](#4-den-hauptbildschirm-verstehen)
5. [Die taktische Karte](#5-die-taktische-karte)
6. [Eine Meldung erstellen](#6-eine-meldung-erstellen)
7. [Ein Ziel erstellen](#7-ein-ziel-erstellen)
8. [Einen Befehl erstellen](#8-einen-befehl-erstellen)
9. [Einen Sammelpunkt erstellen](#9-einen-sammelpunkt-erstellen)
10. [Eine Sicherheitswarnung senden](#10-eine-sicherheitswarnung-senden)
11. [Mit einem bereits veröffentlichten Objekt interagieren](#11-mit-einem-bereits-veröffentlichten-objekt-interagieren)
12. [Das Panel „Führung und Aktivität“](#12-das-panel-führung-und-aktivität)
13. [Das Gruppen- oder Teammenü](#13-das-gruppen-oder-teammenü)
14. [Teams](#14-teams)
15. [Teilnehmer und Rollen](#15-teilnehmer-und-rollen)
16. [Einen neuen Teilnehmer einladen](#16-einen-neuen-teilnehmer-einladen)
17. [Operationen](#17-operationen)
18. [Rollenkampagnen](#18-rollenkampagnen)
19. [Sitzungen](#19-sitzungen)
20. [Datenaustausch zwischen Teams](#20-datenaustausch-zwischen-teams)
21. [Gruppen- und Teamverwaltung](#21-gruppen--und-teamverwaltung)
22. [Veröffentlichungslimits](#22-veröffentlichungslimits)
23. [Standort](#23-standort)
24. [Benachrichtigungen](#24-benachrichtigungen)
25. [Offline-Karten](#25-offline-karten)
26. [Netzwerkverbindung und Offline-Betrieb](#26-netzwerkverbindung-und-offline-betrieb)
27. [Datenschutz, Sperrung und Wiederherstellung](#27-datenschutz-sperrung-und-wiederherstellung)
28. [Verfügbare Rollen](#28-verfügbare-rollen)
29. [Vorbereitungstipps vor einer Aktivität](#29-vorbereitungstipps-vor-einer-aktivität)
30. [Fehlerbehebung](#30-fehlerbehebung)
31. [Kurzübersicht](#31-kurzübersicht)

---

# 1. Erste Schritte: Geräte verbinden

LETCOOR verwendet ein Einladungssystem zwischen Geräten. Eine Einladung kann je nach Plattform per **QR-Code**, **Link**, Systemfreigabe oder Datei übertragen werden.

Um die Verbindungschancen zu maximieren, insbesondere **ohne Internet**, sollten beide Geräte vor dem Austausch vorbereitet werden.

## 1.1 Vor dem Scannen des QR-Codes oder Öffnen des Links

Auf beiden Geräten:

1. Öffnen Sie LETCOOR und lassen Sie die Anwendung während der ersten Verbindung im Vordergrund.
2. Aktivieren Sie **WLAN**.
3. Aktivieren Sie **Bluetooth**.
4. Akzeptieren Sie Android-/Windows-Anfragen zu **Geräten in der Nähe**, Bluetooth, Wi‑Fi Direct oder dem lokalen Netzwerk.
5. Wenn Android anbietet, das Telefon über Bluetooth sichtbar zu machen, akzeptieren Sie dies während der Verbindungsphase.
6. Wenn Android Sie auffordert, den Standortdienst zu aktivieren, damit die Funkerkennung funktioniert, wird die Aktivierung für die Kompatibilität mit den Näherungs-APIs des Telefons empfohlen.
7. Die **Kamera** ist nur zum Scannen eines QR-Codes erforderlich. Wenn Sie einen Link verwenden, wird sie nicht benötigt.

> **Wichtig:** Das Erlauben oder Aktivieren des Android-Standortdienstes für die Näherungserkennung aktiviert nicht automatisch die Freigabe Ihrer Position in LETCOOR. Die Standortfreigabe ist eine separate Funktion und bleibt deaktiviert, solange Sie sie nicht selbst aktivieren.

## 1.2 Verbindung per QR-Code

### Auf dem einladenden Gerät

1. Öffnen Sie das Gruppen- oder Teammenü, indem Sie oben links auf den Namen tippen.
2. Öffnen Sie den Reiter **Einladen**.
3. Wenn mehrere Ziele verfügbar sind, wählen Sie die **Gruppe** oder das **Team**, dem beigetreten werden soll.
4. Öffnen Sie **Einladung teilen**.
5. Wählen Sie **QR-Code anzeigen**.
6. Lassen Sie den QR-Code auf dem Bildschirm angezeigt.

Ein QR-Code kann aus mehreren Teilen bestehen. LETCOOR wechselt automatisch durch diese Teile. Der Wechsel kann pausiert oder manuell zum vorherigen/nächsten Teil fortgesetzt werden.

### Auf dem eingeladenen Gerät

1. Wählen Sie auf dem Startbildschirm **Mit einer Einladung beitreten**.
2. Drücken Sie die Schaltfläche zum Scannen des QR-Codes.
3. Erlauben Sie den Kamerazugriff, wenn Android/Windows danach fragt.
4. Richten Sie die Kamera auf den QR-Code des anderen Geräts.
5. Wenn der QR-Code mehrere Teile enthält, halten Sie die Kamera auf den Bildschirm gerichtet, bis LETCOOR alle Teile gelesen hat.
6. LETCOOR importiert die Einladung und erstellt eine **Antwort**.
7. Das eingeladene Gerät zeigt anschließend einen **Antwortlink** oder einen **Antwort-QR-Code** an, der an das einladende Gerät zurückgesendet werden muss.

### Antwort an den Einladenden zurücksenden

Auf dem Gerät, das die Einladung erstellt hat:

1. Bleiben Sie unter **Einladen**.
2. Öffnen Sie **Antwort empfangen**.
3. Scannen Sie den Antwort-QR-Code, fügen Sie den Antwortlink ein oder verwenden Sie den verfügbaren Freigabemechanismus.
4. LETCOOR überprüft die Antwort und startet anschließend die direkte Verbindung.

Die Anwendung zeigt danach den Status des Versuchs an: Vorbereitung der Nähe, Internetverbindung, lokale Suche, Verbindung hergestellt oder Zeitüberschreitung.

## 1.3 Verbindung per Link

Der Ablauf ist identisch, jedoch ohne Kamera.

### Einladendes Gerät

Unter **Einladen > Einladung teilen**:

1. Wählen Sie **Einladungslink**.
2. Drücken Sie **Link kopieren** oder die Freigabe-Schaltfläche.
3. Senden Sie den Link an den anderen Teilnehmer.

### Eingeladenes Gerät

1. Öffnen Sie **Mit einer Einladung beitreten**.
2. Fügen Sie den Link in **Anzunehmende Einladung** ein oder verwenden Sie die Zwischenablage-Schaltfläche.
3. LETCOOR verarbeitet einen gültigen Link automatisch.
4. Senden Sie anschließend den **Antwortlink** an das einladende Gerät zurück.

### Einladendes Gerät

Unter **Antwort empfangen**:

1. Fügen Sie den Antwortlink ein oder scannen Sie den Antwort-QR-Code.
2. LETCOOR überprüft die Antwort.
3. Die Verbindung startet automatisch.

## 1.4 Warum muss eine Antwort zurückgesendet werden?

Der bidirektionale Ablauf ermöglicht es beiden Geräten, die für den Verbindungsversuch notwendigen Informationen zu kennen. LETCOOR kann anschließend die verfügbaren Wege ausprobieren und den Peer authentifizieren, bevor er in die Gruppe oder das Team aufgenommen wird.

## 1.5 Aufnahme in Gruppe und Team

Eine gültige Einladung ist signiert und auf ein bei ihrer Erstellung festgelegtes Ziel ausgerichtet.

- Mit einer Gruppeneinladung kann der entsprechenden Gruppe beigetreten werden.
- Eine Einladung aus einem Team kann den Zugang zur **übergeordneten Gruppe und zum Team des Einladenden** umfassen.
- Die privaten Schlüssel der Gruppe oder der vollständige Verlauf werden nicht im QR-Code gespeichert.
- Die Aufnahme wird nach der Authentifizierung durch das LETCOOR-Protokoll bestätigt; bei einer gültigen Einladung gibt es keine zusätzliche manuelle Bestätigung, außer wenn die Aufnahmerichtlinie oder die Berechtigungen des Bereichs dies verhindern.

---

# 2. Wichtige Berechtigungen, besonders offline

LETCOOR verwendet mehrere Systemfunktionen. Für den Betrieb ohne Internet sind die Näherungsberechtigungen besonders wichtig.

## 2.1 Bluetooth und Wi‑Fi Direct

Unter **Einstellungen > Berechtigungen** bietet LETCOOR:

- **Bluetooth und Wi‑Fi Direct — Zulassen**
- **Kamera — Zulassen**
- **Standort — Prüfen**

Auf neueren Android-Versionen kann LETCOOR insbesondere Systemberechtigungen anfordern für:

- Geräte in der Nähe;
- Bluetooth-Scan;
- Bluetooth-Verbindung;
- Bluetooth-Werbung;
- Wi‑Fi Direct / WLAN-Geräte in der Nähe;
- Zugriff auf das lokale Netzwerk auf Android-Versionen, die dies verlangen.

Auf einigen älteren Android-Versionen kann die Bluetooth-/WLAN-Erkennung von der Android-Standortberechtigung abhängen.

## 2.2 Standort: zwei verschiedene Dinge

Es muss unterschieden werden zwischen:

1. **Dem Android-Systemstandort, der von bestimmten APIs zur Näherungserkennung verwendet wird.**
2. **Der freiwilligen Freigabe Ihrer Position in LETCOOR.**

Sie können LETCOOR verwenden, ohne Ihre Position auf der Karte zu veröffentlichen. Die Standortfreigabe wird separat über das Symbol **Standort** eingestellt.

## 2.3 Kamera

Die Kamera wird ausschließlich zum Scannen von QR-Codes verwendet. Für das Scannen ist kein Mikrofon erforderlich.

Wenn der Kamerazugriff verweigert wurde:

- verwenden Sie den Einladungslink;
- oder erlauben Sie die Kamera erneut in den Android-/Windows-Einstellungen.

## 2.4 Systembenachrichtigungen

Systembenachrichtigungen können im LETCOOR-Benachrichtigungscenter aktiviert werden. Damit können native Warnungen für bestimmte Ereignisse empfangen werden, sofern die Plattform dies unterstützt.

---

# 3. Eine Gruppe erstellen oder ihr beitreten

Beim ersten Start zeigt LETCOOR den Startbildschirm an, wenn das Gerät noch keiner Gruppe angehört.

Sie haben zwei Möglichkeiten:

- **Gruppe erstellen**
- **Mit einer Einladung beitreten**

## 3.1 Eine Gruppe erstellen

1. Drücken Sie **Gruppe erstellen**.
2. Geben Sie den **Gruppennamen** ein.
3. Der Name muss mindestens 2 Zeichen enthalten.
4. Drücken Sie **Erstellen**.

Der Ersteller erhält die Verwaltungsrolle der Gruppe und kann anschließend Teams erstellen, Teilnehmer einladen und den Bereich gemäß den vom Core gewährten Möglichkeiten verwalten.

## 3.2 Einer Gruppe beitreten

1. Drücken Sie **Mit einer Einladung beitreten**.
2. Importieren Sie den Link oder den QR-Code.
3. Folgen Sie dem am Anfang dieser Dokumentation beschriebenen Einladungs-/Antwortaustausch.

## 3.3 Persönliche Nr.

Jedes Gerät besitzt eine **Persönliche Nr.**, die beim Onboarding und im Reiter **Kontext** angezeigt wird.

Diese Nummer dient in der Benutzeroberfläche als für den Benutzer lesbare Kennung. Die tatsächliche kryptografische Identität basiert auf der LETCOOR-Geräteidentität und nicht auf diesem angezeigten Code.

---

# 4. Den Hauptbildschirm verstehen

LETCOOR verwendet eine **kartenbasierte Benutzeroberfläche** anstelle einer Abfolge klassischer Seiten.

## 4.1 Kopfbereich

Oben auf dem Bildschirm:

- links: der **Name der aktuell ausgewählten Gruppe oder des Teams**;
- der Untertitel zeigt **Gruppe** oder **Team** an;
- **Nicht synchronisiert** kann erscheinen, wenn der Kontext ohne Synchronisierung arbeitet;
- eine Glocke öffnet die **Benachrichtigungen**;
- die Schaltfläche **Führung** öffnet das Panel für Führung und Aktivität;
- ein Indikator zeigt den Netzwerkstatus: direktes Internet, Relay, Wi‑Fi Direct, lokales WLAN, Bluetooth, LAN, Synchronisierung oder Verbindungssuche.

## 4.2 Zentrale Karte

Die Karte zeigt die im aktuellen Kontext erlaubten Objekte:

- Befehle;
- Meldungen;
- Ziele;
- Treffpunkte / Sammelpunkte;
- Sicherheitswarnungen;
- Teampräsenz;
- genaue Präsenz, wenn sie erlaubt ist;
- Bewegungen / Routen abhängig von Rechten und aktiven Freigaben.

## 4.3 Legende

Die Schaltfläche `?` zeigt die Legende an, darunter:

- Gefahr;
- Ziel;
- Sammelpunkt;
- Team.

## 4.4 Fußbereich

Am unteren Bildschirmrand werden angezeigt:

- die Anzahl der aktiven Mitglieder im Kontext;
- die Anzahl der aktiven Objekte;
- eine eventuell laufende Sitzung, andernfalls Ihre Persönliche Nr.

## 4.5 Gruppen- oder Teammenü öffnen

Tippen Sie oben links auf den Kontextnamen.

Das Panel enthält die Reiter:

- **Kontext**
- **Teams**
- **Teilnehmer**
- **Einladen**
- **Operationen**
- **Verwaltung**
- **Einstellungen**

Einige Funktionen werden nur angezeigt, wenn Ihre Rolle die entsprechende Berechtigung besitzt.

---

# 5. Die taktische Karte

## 5.1 Bewegen

Die Karte wird wie eine klassische Touch-Karte bedient: verschieben und zoomen.

## 5.2 Ein Objekt hinzufügen

Um ein räumliches Objekt zu veröffentlichen:

1. Drücken Sie **lange** auf die gewünschte Stelle.
2. LETCOOR öffnet **Hier hinzufügen**.
3. Die für Ihre Rolle erlaubten Aktionen werden angeboten.

Mögliche Aktionen:

- **Meldung**
- **Ziel**
- **Befehl**
- **Sammelpunkt**
- **Sicherheitswarnung**

Aktionen, die in Ihrem Kontext nicht erlaubt sind, werden nicht angezeigt.

## 5.3 Geografische Formen

Je nach Objekttyp ermöglicht LETCOOR:

- **Punkt**;
- **Kreisförmiger Bereich**;
- **Polygon**;
- **Route**.

Für einen kreisförmigen Bereich kann der Radius von **10 bis 500 m** eingestellt werden.

Für ein Polygon oder eine Route:

1. wählen Sie die Geometrie;
2. drücken Sie **Auf der Karte zeichnen**;
3. fügen Sie die Punkte auf der Karte hinzu;
4. verwenden Sie **Letzten rückgängig**, **Beenden** oder **Abbrechen**.

Die Anzahl der Punkte ist durch die Benutzeroberfläche begrenzt.

## 5.4 Dauer / Frist

Räumliche Objekte, die keine Sicherheitsobjekte sind, können eine Dauer zwischen **5 und 360 Minuten** in 5-Minuten-Schritten erhalten.

---

# 6. Eine Meldung erstellen

1. Drücken Sie lange auf die Karte.
2. Wählen Sie **Meldung**.
3. Wählen Sie den Typ.
4. Geben Sie optional einen Namen und eine Beschreibung ein.
5. Wählen Sie Geometrie und Dauer.
6. Drücken Sie **Veröffentlichen**.

## Verfügbare Meldungstypen

- Gefahr
- Hindernis
- Gesperrte Route
- Unpassierbarer Weg
- Offener Durchgang
- Gegner beobachtet
- Gruppe beobachtet
- Bewegung beobachtet
- Ausrüstungsproblem
- Benutzerdefiniert

Je nach Rolle kann eine Meldung innerhalb des Teams oder auf Gruppenebene veröffentlicht werden.

Scouts und Verantwortliche mit den erforderlichen Berechtigungen können insbesondere bestimmte Meldungen bestätigen, bestreiten, auflösen oder auf Gruppenebene hochstufen.

---

# 7. Ein Ziel erstellen

1. Drücken Sie lange auf die Karte.
2. Wählen Sie **Ziel**.
3. Geben Sie **Zu erreichendes Ziel** ein.
4. Wählen Sie den Typ.
5. Wählen Sie die Priorität.
6. Wählen Sie die Geometrie.
7. Stellen Sie die Frist ein.
8. Drücken Sie **Veröffentlichen**.

## Zieltypen

- Einen Punkt erreichen
- Einen Bereich halten
- Einen Bereich einnehmen
- Einen Gegenstand bergen
- Einen Treffpunkt erreichen
- Einen Bereich beobachten
- Benutzerdefiniert

## Teamziel oder endgültiges Gruppenziel

Wenn Rolle und Kontext dies erlauben, kann im Formular gewählt werden:

- **Gesamte Gruppe — endgültiges Ziel**;
- **Dieses Team — Teamziel**.

Das endgültige Ziel ist für Gruppenmitglieder und Teams gemäß den Autorisierungsregeln des Core sichtbar.

## Prioritäten

Die Benutzeroberfläche bietet:

- P0 — Dringend
- P1 — Hoch
- P2 — Normal
- P3 — Niedrig

---

# 8. Einen Befehl erstellen

1. Drücken Sie lange auf die Karte.
2. Wählen Sie **Befehl**.
3. Geben Sie bei Bedarf eine benutzerdefinierte Anweisung ein.
4. Wählen Sie den Befehlstyp.
5. Wählen Sie die Priorität.
6. Sie können den Befehl mit einem bestehenden **Ziel** verknüpfen.
7. Sie können den Befehl mit einem bestehenden **Treffpunkt** verknüpfen.
8. Falls erforderlich, kann LETCOOR direkt am selben Ort ein Ziel oder einen Treffpunkt erstellen und anschließend zum Befehl zurückkehren.
9. Wählen Sie Geometrie und Dauer.
10. Drücken Sie **Veröffentlichen**.

## Befehlstypen

- Bewegen
- Sammeln
- Position halten
- Vorrücken
- Zurückziehen
- Verteidigen
- Beobachten
- Ein Ziel sichern
- Benutzerdefiniert

## Befehl des Gruppenleiters

Wenn die Veröffentlichung ein Gruppenführungsbefehl ist, wählt der Gruppenleiter die **Empfängerteams** aus. Der operative Code sieht vor, dass diese Art von Befehl an die Leiter der ausgewählten Teams gerichtet ist.

## Teambefehl

Ein Teamleiter kann innerhalb seines Teams Befehle erstellen. Ein Teambefehl kann außerdem mit einem übergeordneten Führungsbefehl verknüpft werden, wenn diese Beziehung verfügbar ist.

---

# 9. Einen Sammelpunkt erstellen

1. Drücken Sie lange auf die Karte.
2. Wählen Sie **Sammelpunkt**.
3. Geben Sie einen kurzen Namen ein.
4. Wählen Sie einen **Punkt** oder einen **Kreisförmigen Bereich**.
5. Stellen Sie Dauer / Frist ein.
6. Veröffentlichen Sie.

Der Sammelpunkt erstellt einen Treffpunkt, der auch als Referenz für einen Befehl verwendet werden kann.

---

# 10. Eine Sicherheitswarnung senden

Die Sicherheitswarnung ist eine priorisierte Veröffentlichung.

1. Drücken Sie lange auf die Karte.
2. Wählen Sie **Sicherheitswarnung**.
3. Geben Sie bei Bedarf eine Nachricht ein.
4. Wählen Sie den Typ.
5. Drücken Sie **Warnung senden**.

## Verfügbare Typen

- Verletzung
- Aktivität stoppen
- Gefahr
- Vermisste Person
- Anderer Notfall

Eine benutzerdefinierte Warnung erfordert eine Nachricht.

LETCOOR weist in der Benutzeroberfläche darauf hin, dass die P0-Warnung bei Gefahr oder Hilfebedarf verwendet werden soll.

Je nach Berechtigungen kann ein Verantwortlicher anschließend **Als gelöst markieren** wählen.

---

# 11. Mit einem bereits veröffentlichten Objekt interagieren

Tippen Sie auf ein Objekt auf der Karte, um dessen Detailansicht zu öffnen.

Die angebotenen Aktionen hängen vom Objekttyp und Ihren Berechtigungen ab.

## Meldung

Mögliche Aktionen:

- Bestätigen
- Bestreiten
- Lösen
- Um 15 Min verlängern
- Meldung abbrechen
- Zur Gruppe hochstufen, wenn die Meldung aus einem Team stammt und die Rolle dies erlaubt

Für bestimmte operative Objekte kann LETCOOR außerdem anbieten:

- **Vor Ort bestätigen**;
- **Für Lösung abstimmen**;
- **Offenen Durchgang melden**;
- **Information entfernen**.

## Ziel

Ein Benutzer mit der entsprechenden Berechtigung kann den Status ändern:

- In Bearbeitung
- Abgeschlossen
- Fehlgeschlagen
- Abgebrochen

## Befehl

Je nach Befehlstyp können Antworten angeboten werden:

- Empfangen
- Akzeptiert
- Abgeschlossen
- Unmöglich

Das vereinfachte Panel **Operationen > Befehle** verwendet mindestens die Bestätigung **Empfangen**, wenn der Befehl eine Antwort erfordert.

## Sicherheitswarnung

Der autorisierte Verantwortliche kann **Als gelöst markieren** wählen.

---

# 12. Das Panel „Führung und Aktivität“

Die Schaltfläche **Führung** oben auf dem Bildschirm öffnet ein separates Panel für Operationen, die nicht zwingend mit einem Punkt auf der Karte verbunden sind.

Es enthält bis zu drei Reiter:

- **Benachrichtigungen**
- **Veröffentlichen**
- **Verlauf**

Die Reiter erscheinen nur, wenn sie Inhalte enthalten oder eine Aktion erlaubt ist.

## 12.1 Benachrichtigungen

Zeigt zugängliche operative Objekte:

- Führungsbefehl;
- Teambefehl;
- Ziel;
- endgültiges Gruppenziel;
- Ankündigung;
- zu prüfender Bericht;
- verifizierte Meldung.

Jede Karte kann anzeigen:

- Text;
- Typ;
- Status;
- Team/Gruppe;
- verknüpftes Ziel oder Treffpunkt;
- adressierte Teams;
- Empfangsbestätigungen;
- Abstimmungen;
- Fortschritt pro Team.

Je nach Rolle können die Schaltflächen anbieten:

- Empfangen;
- Vor Ort prüfen;
- Entfernen;
- Als gelesen markieren;
- Als abgeschlossen melden;
- Für abgeschlossen stimmen;
- Für unmöglich stimmen;
- Für gelöst stimmen;
- Lösen.

## 12.2 Veröffentlichen

LETCOOR zeigt nur Veröffentlichungen an, die für Ihre Rolle und Ihren Kontext erlaubt sind.

Zu den derzeit von der Oberfläche verwalteten internen Typen gehören:

- Führungsbefehl
- Teambefehl
- Teamziel
- Endgültiges Gruppenziel
- Ankündigung
- Zu prüfender Bericht
- Verifizierte Meldung

Wählen Sie bei einem Führungsbefehl die Empfängerteams.

Bei einem Teambefehl können Sie einen übergeordneten Führungsbefehl auswählen.

Geben Sie anschließend die Beschreibung ein und drücken Sie **Veröffentlichen**.

Veröffentlichungen aus diesem Panel verwenden im aktuellen Oberflächencode standardmäßig eine operative Dauer von ungefähr 30 Minuten.

## 12.3 Verlauf

Zeigt aufgezeichnete Ereignisse mit Datum, Zusammenfassung und Objektkennung an.

---

# 13. Das Gruppen- oder Teammenü

Tippen Sie oben links auf den Kontextnamen.

## Reiter Kontext

Zeigt an:

- die Auswahl **Gruppe oder Team**;
- die Anzahl der Mitglieder;
- die Anzahl der verbundenen Geräte;
- den Sitzungsstatus;
- Ihre Rollen;
- das Theme System / Hell / Dunkel;
- die Sprache;
- Ihre kopierbare **Persönliche Nr.**

Die aktuell von der Benutzeroberfläche angebotenen Sprachen sind: **System, Français, English, العربية, Deutsch und Русский**. Für Arabisch wechselt die Oberfläche automatisch zur Schreibrichtung von rechts nach links.

## Reiter Teams

Siehe [Teams](#14-teams).

## Reiter Teilnehmer

Siehe [Teilnehmer und Rollen](#15-teilnehmer-und-rollen).

## Reiter Einladen

Siehe [Einen neuen Teilnehmer einladen](#16-einen-neuen-teilnehmer-einladen).

## Reiter Operationen

Siehe [Operationen](#17-operationen).

## Reiter Verwaltung

Siehe [Gruppen- und Teamverwaltung](#21-gruppen--und-teamverwaltung).

## Reiter Einstellungen

Enthält derzeit:

- Offline-Karten;
- Verwaltung der Bluetooth-/Wi‑Fi-Direct-Berechtigungen;
- Kameraberechtigung;
- Standortprüfung.

---

# 14. Teams

Der Reiter **Teams** zeigt die Teams der Gruppe an.

Für jedes Team zeigt LETCOOR unter anderem:

- Name;
- Anzahl der Mitglieder;
- Teamleiter;
- Teilnehmerliste;
- Ihren Zugriffsstatus für das Team.

## Zugriffsstatus

- **Sie sind Mitglied · Zugriff bereit**
- **Mitgliedschaft registriert · Schlüssel werden empfangen**
- **Sie gehören diesem Team nicht an**

Wenn Sie Mitglied sind und der Zugriff bereit ist, drücken Sie **Mein Team öffnen**.

## 14.1 Ein Team erstellen

Diese Funktion erscheint für den Gruppenleiter mit der entsprechenden Berechtigung.

1. Geben Sie den **Teamnamen** ein.
2. Wählen Sie den **Teamleiter** aus den Gruppenmitgliedern.
3. Wählen Sie optional die anfänglichen Mitglieder aus.
4. Sie können verwenden:
   - Alle auswählen;
   - 10 Personen;
   - 15 Personen;
   - Alle abwählen.
5. Drücken Sie **Team erstellen und Leiter ernennen**.

Ein Team akzeptiert im Formular höchstens 200 anfängliche Mitglieder einschließlich des Leiters.

Ausgewählte Mitglieder verlassen gegebenenfalls ihr bisheriges Team derselben Gruppe, um dem neuen beizutreten.

Wenn die Gruppe bereits zehn oder mehr Teams besitzt, erzwingt der Code zusätzliche Mindestgrößen: Aktive Teams müssen mindestens vier Mitglieder haben, damit die Erweiterung fortgesetzt werden kann.

## 14.2 Teamleiter ersetzen

Wenn die Aktion erlaubt ist:

1. öffnen Sie das Team;
2. verwenden Sie **Teamleiter ersetzen**;
3. wählen Sie ein Gruppenmitglied.

## 14.3 Validierungsschwellen

Autorisierte Verantwortliche können einstellen:

- erforderliche Scout-Stimmen zum Abschließen;
- erforderliche Scout-Stimmen zur Erklärung „unmöglich“;
- erforderliche Stimmen zum Lösen einer Meldung.

---

# 15. Teilnehmer und Rollen

Der Reiter **Teilnehmer** zeigt die Mitglieder des ausgewählten Kontexts.

Sie können einen Teilnehmer anhand seiner Persönlichen Nr. oder Kennung suchen.

Tippen Sie auf einen Teilnehmer, um die verfügbaren Aktionen zu öffnen.

## 15.1 Dauerhafte Rollen und Sitzungsrollen

Wenn eine Sitzung verfügbar ist, kann der Verwalter wählen:

- **Dauerhaft**;
- **Sitzung**.

Eine dauerhafte Rolle bleibt gemäß den Gruppen-/Teamregeln mit dem Mitglied verbunden.

Eine Sitzungsrolle gilt für die ausgewählte Sitzung.

## 15.2 Eine Rolle zuweisen oder entfernen

Rollen, die Sie zuweisen können, erscheinen als Schaltflächen.

Eine aktive Schaltfläche zeigt an, dass die Rolle bereits vorhanden ist. Durch Drücken kann die Rolle entfernt werden, wenn Sie dazu berechtigt sind.

Es gibt außerdem den Abschnitt **Eine Rolle in einem Team verwalten**, in dem gewählt werden kann:

1. das Zielteam;
2. die Rolle;
3. **Teamrolle zuweisen** oder **Teamrolle entfernen**.

## 15.3 Sitzungszuweisung

Ein Sitzungsadministrator kann den Teilnehmer festlegen als:

- Aktiv;
- Pausiert;
- Gegangen;
- Entfernt.

Er kann außerdem das Sitzungsteam oder **Kein Team** wählen.

Drücken Sie **Zuweisung anwenden**.

## 15.4 Ein Mitglied entfernen

Wenn die Berechtigung verfügbar ist, erscheint die Schaltfläche **Aus dieser Gruppe oder diesem Team entfernen**.

## 15.5 Gruppenverwaltung übertragen

Der autorisierte Verantwortliche kann einen anderen Teilnehmer auswählen und anschließend **Verwaltung übertragen** verwenden.

Der Empfänger muss die Übertragung anschließend im Abschnitt **Verwaltung** annehmen.

## 15.6 Ein Gerät sperren

Der Abschnitt **Moderation** ermöglicht, sofern Ihre Rolle dies erlaubt:

- **Dieses Gerät sperren**;
- gesperrte Geräte anzeigen;
- **Sperre aufheben**.

Ein gesperrtes Gerät wird bei neuen Einladungen weiterhin abgelehnt, bis die Sperre aufgehoben wird.

---

# 16. Einen neuen Teilnehmer einladen

Öffnen Sie **Einladen**.

## 16.1 Ziel auswählen

Je nach Rolle können Sie im Menü **Ziel** wählen:

- die Gruppe;
- ein Team.

Ein Gruppenadministrator kann mehrere Ziele im Menü haben.

## 16.2 Aufnahme offen / geschlossen

Die Benutzeroberfläche kann anzeigen:

- **Aufnahme offen**;
- **Aufnahme geschlossen**.

Wenn Ihre Rolle dies erlaubt:

- **Zugang öffnen**;
- **Zugang schließen**.

Ein Team kann außerdem die allgemeine Schließung der Gruppe übernehmen.

## 16.3 Einladung teilen

LETCOOR ermöglicht:

- Link;
- QR;
- Kopie;
- Systemfreigabe;
- `.letcoor`-Datei auf Plattformen, auf denen die Schaltfläche angeboten wird.

## 16.4 Antwort empfangen

Nachdem das andere Gerät die Einladung importiert hat:

1. öffnen Sie **Antwort empfangen**;
2. scannen Sie den Antwortlink oder fügen Sie ihn ein;
3. LETCOOR startet die Verbindung.

Wenn Internet- und Näherungsversuche ablaufen, können Sie mit **Erneut versuchen** neu beginnen.

## 16.5 Eine Einladung zurücksetzen

Die Zurücksetzen-Schaltfläche kann den aktuellen Austausch ungültig machen/neu erzeugen, wenn Ihre Rolle dies erlaubt.

---

# 17. Operationen

Im Reiter **Operationen** kann eine Gruppe oder ein Team gewählt werden; anschließend werden abhängig von Rechten und Inhalt verschiedene Unterreiter angezeigt:

- **Befehle**
- **Ankündigungen**
- **Rollen**
- **Austausch zwischen Teams**
- **Sitzungen**
- **Verlauf**

## 17.1 Befehle

Zeigt aktive Befehle mit:

- Typ;
- Priorität;
- Text;
- Antwortstatus.

Wenn eine Bestätigung erforderlich ist, kann mit **Empfangen** der Empfang in dieser Ansicht bestätigt werden.

## 17.2 Ankündigungen

Zeigt aktive Ankündigungen.

Jede Ankündigung kann enthalten:

- Typ;
- Text;
- angehefteter Status;
- Schaltfläche **Empfang bestätigen**.

Ein autorisiertes Mitglied kann eine Ankündigung erstellen und wählen:

### Typen

- Information
- Wichtig
- Gruppeninformation
- Sitzungsinformation
- Aktivitätsregel
- Koordination

### Ablauf

- 15 Min
- 1 Std
- 4 Std
- 24 Std
- Kein Ablauf

Ein Kontrollkästchen erlaubt **Ankündigung anheften**.

---

# 18. Rollenkampagnen

Rollenkampagnen ermöglichen es, vorübergehend Plätze für eine bestimmte Rolle zu öffnen.

Sie befinden sich unter:

**Gruppen-/Teammenü > Operationen > Rollen**

## 18.1 Einer Kampagne beitreten

Eine offene Kampagne zeigt:

- die Rolle;
- ihren Status;
- den Modus;
- die Anzahl bereits vergebener Plätze / Kapazität.

Drücken Sie **Beitreten**, um die Rolle anzufordern.

## 18.2 Kampagnenmodi

### Erste gültige Anfragen — `FIRST_VALID`

Die ersten berechtigten Anfragen werden automatisch vergeben, bis die verfügbare Kapazität erreicht ist.

Der Code erlaubt diesen Modus nur für Rollen, die als nicht privilegiert gelten.

### Freigabe durch einen Verantwortlichen — `ADMIN_APPROVAL`

Anfragen bleiben ausstehend, bis sie von einem Verantwortlichen bestätigt werden.

Der Verwalter sieht **Ausstehende Anfragen** und kann für jeden Teilnehmer **Genehmigen** drücken.

## 18.3 Eine Kampagne erstellen

Wenn Ihre Rolle die Kampagnenverwaltung erlaubt:

1. wählen Sie die **Rolle**;
2. wählen Sie den für diese Rolle angebotenen **Modus**;
3. wählen Sie die Anzahl der **Plätze** von 1 bis 64;
4. wählen Sie die **Dauer**:
   - 15 Min;
   - 1 Std;
   - 4 Std;
   - 24 Std;
5. drücken Sie **Kampagne öffnen**.

## 18.4 Eine Kampagne schließen

Ein autorisierter Verwalter kann **Schließen** drücken.

## 18.5 Eigene Anfrage zurückziehen

Im **Verlauf** kann bei einer noch ausstehenden Anfrage **Meine Anfrage zurückziehen** angezeigt werden.

## 18.6 Für Kampagnen verfügbare Rollen

Abhängig von Kontext und Rechten stellt der Code für Kampagnen bereit:

- Gruppen-Scout;
- Team-Scout;
- Relay;
- Deckung;
- Angriff.

Die Rolle Gruppenleiter wird niemals über eine Kampagne vergeben.

---

# 19. Sitzungen

Eine Sitzung stellt einen zeitlich begrenzten operativen Zeitraum innerhalb der Gruppe dar.

## 19.1 Eine Sitzung erstellen

Unter **Verwaltung**, sofern Sie die Berechtigung besitzen:

1. öffnen Sie den Abschnitt **Sitzung**;
2. geben Sie die Dauer in Minuten ein;
3. die maximal angezeigte Dauer beträgt **56 Tage**;
4. drücken Sie **Sitzung erstellen**.

## 19.2 Sitzungen anzeigen

Unter **Operationen > Sitzungen** zeigt LETCOOR:

- Erstellungsdatum;
- Status: offen/beendet oder Zuweisungsstatus;
- Ihr eventuelles Team;
- geplantes Ende.

## 19.3 Eine Sitzung verwalten

Der autorisierte Verantwortliche kann:

- **+ 1 Std** hinzufügen;
- die Sitzung **Beenden**.

## 19.4 Rollen und Zuweisungen während einer Sitzung

Unter **Teilnehmer** können Sie eine verwaltete Sitzung auswählen, auf diese Sitzung begrenzte Rollen zuweisen und Teilnehmer einem Team/Status zuordnen.

---

# 20. Datenaustausch zwischen Teams

Diese Funktion ist aus einem **Team** heraus verfügbar unter:

**Operationen > Austausch zwischen Teams**

Sie gewährt nicht automatisch Zugriff auf private Inhalte eines anderen Teams. Sie verwendet ein ausdrücklich erstelltes und angenommenes Freigabeangebot.

## 20.1 Freigabe anbieten

1. Wählen Sie das **Zielteam**.
2. Wählen Sie die **Freigegebenen Daten**.
3. Wählen Sie die Genauigkeit.
4. Stellen Sie das Intervall ein.
5. Stellen Sie den Ablauf ein.
6. Drücken Sie **Freigabe anbieten**.

## 20.2 Verfügbare Datenklassen

- Allgemeine Teampräsenz
- Signal
- Teamstatus
- Genaue Position
- Bewegungsverlauf

## 20.3 Genauigkeit

- Übersicht / aggregiert
- Ungefähr
- Genau

Wenn **Genaue Position** ausgewählt wird, wird die Genauigkeit in der Benutzeroberfläche zwingend auf genau gesetzt.

## 20.4 Intervall

Einstellbar zwischen **5 und 300 Sekunden** in 5-Sekunden-Schritten.

## 20.5 Ablauf

- 15 Min
- 1 Std
- 4 Std
- 24 Std

## 20.6 Annehmen oder widerrufen

Das autorisierte Empfängerteam kann **Annehmen** drücken.

Ein Angebot oder eine Freigabe kann von der Seite mit der entsprechenden Berechtigung **Widerrufen** werden.

---

# 21. Gruppen- und Teamverwaltung

Der Reiter **Verwaltung** bündelt die administrativen Funktionen.

## 21.1 Einen Bereich auswählen

Mit der Auswahl **Gruppe oder Team** kann der zu verwaltende Bereich gewählt werden.

## 21.2 Einem bestehenden Team beitreten

Wenn die Aktion erlaubt ist, kann ein Team anbieten:

- **Beitreten**;
- **Zugriff wiederherstellen**, wenn die Mitgliedschaft besteht, die Schlüssel jedoch erneut abgerufen werden müssen.

## 21.3 Ein Team verlassen

Drücken Sie **Team verlassen** und prüfen Sie die Zusammenfassung, bevor Sie bestätigen.

## 21.4 Ein Team auflösen

Ein autorisierter Verantwortlicher sieht **Team auflösen**.

Die Bestätigung weist darauf hin, dass:

- das Team für seine Mitglieder aufgelöst wird;
- die Mitglieder in der Gruppe bleiben;
- andere Geräte die Auflösung anwenden, sobald sie sie empfangen.

## 21.5 Eine Gruppe verlassen

Ein normales Mitglied kann einen Austrittsplan vorbereiten und anschließend bestätigen.

Wenn der Teilnehmer Teams leitet, muss LETCOOR diese Teams gemäß dem vom Core berechneten Plan möglicherweise vor dem Austritt auflösen.

## 21.6 Eine Gruppe auflösen

Der autorisierte Gruppenleiter kann **Gruppe auflösen** verwenden.

Die Bestätigung warnt davor, dass die Gruppe und ihre Teams aufgelöst werden. Offline-Geräte müssen sich erneut verbinden, um die Auflösung zu erhalten.

## 21.7 Einer neuen Gruppe oder einem neuen Team beitreten

Die Seite **Verwaltung** enthält außerdem einen Bereich **Einer Gruppe oder einem Team beitreten** mit demselben Einladungssystem wie beim Onboarding.

## 21.8 Ausstehende Einladungen

Wenn der Core anzunehmende Einladungen bereitstellt, erscheinen sie bis zum Ablauf mit einer Schaltfläche **Annehmen**.

## 21.9 Teamstatus

Der autorisierte Verantwortliche kann veröffentlichen:

- Bereit
- In Bewegung
- In Position
- Beim Sammeln
- Hilfe benötigt
- Getrennt

## 21.10 Richtlinie für genaue Position

In einem Team kann ein autorisierter Verantwortlicher für die Richtlinie zur genauen Position des Teams wählen:

- **Zulassen**;
- **Verweigern**.

## 21.11 Verwaltungsübertragung

Wenn für Sie eine Verwaltungsübertragung aussteht, zeigt der Abschnitt **Verwaltungsübertragung annehmen**.

---

# 22. Veröffentlichungslimits

Unter **Verwaltung** können autorisierte Verantwortliche die Veröffentlichungslimits der Gruppe oder des Teams einstellen.

Limits können festgelegt werden:

- standardmäßig;
- für ein bestimmtes Mitglied.

Derzeit verfügbare Parameter:

- Anzahl aktiver Sicherheitswarnungen;
- Meldungen pro Minute;
- Meldungen pro 4 Minuten.

Die Formularwerte reichen von 1 bis 1000.

---

# 23. Standort

Das Symbol **Standort** erscheint auf der Karte, wenn die Plattform native Standortdienste bereitstellt.

## 23.1 Freigabe aktivieren

1. Öffnen Sie **Standort**.
2. Wählen Sie **Meinen Standort teilen**.
3. Stellen Sie die Genauigkeit ein.

LETCOOR veröffentlicht die Präsenz regelmäßig erneut, solange die Freigabe aktiv ist und die Anwendung die Position abrufen kann.

## 23.2 Genauigkeit

Der Schieberegler reicht von **0 m bis 1 km**.

- **0 m**: auf dem Gerät verfügbare Genauigkeit, ohne von LETCOOR hinzugefügte Verschiebung.
- höherer Wert: die geteilte Position wird zufällig innerhalb des gewählten Radius verschoben.

## 23.3 Freigabe beenden

Wählen Sie **Meinen Standort nicht teilen**.

Die Freigabe wird außerdem beendet, wenn der Kontext wechselt oder die Anwendung die Präsenz entsprechend ihrem Lebenszyklus unterbricht.

## 23.4 Angezeigte Status

- Standort wird ermittelt…
- Freigabe mit Ihrer Gruppe aktiv
- Freigabe wartet auf Fortsetzung
- Standort nicht geteilt

> Die Standortfreigabe ist nicht erforderlich, um einer Gruppe beizutreten, die Karte zu verwenden, Befehle zu senden oder das Mesh zu nutzen.

---

# 24. Benachrichtigungen

Tippen Sie oben auf dem Bildschirm auf die **Glocke**.

Das Benachrichtigungscenter bündelt:

- Gruppenereignisse;
- Änderungen von Verbindung/Transport;
- LETCOOR-Systemhinweise.

Der Zähler zeigt die Anzahl ungelesener Benachrichtigungen.

## 24.1 Lesen

Benachrichtigungen werden als gelesen markiert, wenn sie in der Liste ausreichend sichtbar werden oder der entsprechende Abschnitt geöffnet wird.

## 24.2 Navigation

Durch Tippen auf eine Benachrichtigung kann geöffnet werden:

- der Abschnitt Teilnehmer;
- Teams;
- Operationen;
- ein Kartenobjekt;
- das Führungspanel.

## 24.3 Systembenachrichtigungen

In den Glockeneinstellungen können native Systembenachrichtigungen aktiviert/deaktiviert werden, sofern die Plattform dies erlaubt.

---

# 25. Offline-Karten

Öffnen Sie:

**Gruppen-/Teammenü > Einstellungen > Offline-Karten**

## 25.1 Einen Bereich auswählen

1. Drücken Sie **Kacheln auf der Karte auswählen**.
2. LETCOOR schließt das Panel und zeigt ein Raster auf der Karte an.
3. Tippen Sie auf die Zellen, die gespeichert werden sollen.
4. Der Zähler zeigt die Anzahl ausgewählter Zellen von maximal 20 an.
5. Drücken Sie **Bestätigen**, um zu den Einstellungen zurückzukehren, oder **Abbrechen**.

## 25.2 Detailstufe

Im Menü **Detail** kann eine Zoomstufe von 3 bis 14 gewählt werden.

Ein zu großer Bereich bei hoher Detailstufe kann abgelehnt werden. Die Oberfläche fordert dann dazu auf, die Detailstufe zu verringern oder kleinere Zellen zu wählen.

## 25.3 Installieren

Nachdem die Zellen ausgewählt wurden:

1. drücken Sie **Ausgewählte Zellen installieren**;
2. verfolgen Sie den Fortschritt;
3. Sie können den **Download abbrechen**.

## 25.4 Eine Karte löschen

Installierte Karten werden mit Zoomstufe und Größe aufgelistet. Drücken Sie **Löschen**, um Speicherplatz freizugeben.

---

# 26. Netzwerkverbindung und Offline-Betrieb

LETCOOR kann mehrere Transportwege für dasselbe logische Netzwerk verwenden.

Die Benutzeroberfläche kennt insbesondere:

- **Direktes Internet**;
- **Internet über Relay**;
- **Lokales Netzwerk (LAN)**;
- **Lokales WLAN**;
- **Wi‑Fi Direct**;
- **Bluetooth**.

## 26.1 Logisches Mesh

LETCOOR verlangt nicht, dass jedes Mitglied direkt mit allen anderen verbunden ist.

Beispiel:

```text
Telefon A ↔ Telefon B ↔ Telefon C ↔ Telefon D
```

Ein autorisiertes Ereignis kann abhängig von Topologie und Geltungsbereichsregeln der Gruppe/des Teams zwischen Peers weitergeleitet werden.

Der physische Transportweg und die LETCOOR-Identität sind getrennt: Ein Peer bleibt über seine LETCOOR-Identität identifiziert, auch wenn sich der Netzwerkweg ändert.

## 26.2 Ohne Internet

Um die Chancen auf einen Betrieb ohne Internet zu maximieren:

- WLAN aktivieren;
- Bluetooth aktivieren;
- Geräte in der Nähe zulassen;
- lokales Netzwerk zulassen, wenn Android danach fragt;
- Systemsichtbarkeit/-kopplung akzeptieren, wenn LETCOOR danach fragt;
- LETCOOR während der ersten Verbindung im Vordergrund lassen;
- Geräte während des anfänglichen Bootstraps näher zusammenbringen;
- Systemdialoge, die für Nahbereichsfunk erforderlich sind, nicht ablehnen.

## 26.3 Status der Näherungstransporte

LETCOOR kann separat anzeigen:

- Lokales WLAN;
- Wi‑Fi Direct;
- Bluetooth;

mit Zuständen wie:

- Berechtigung erforderlich;
- Aktivierung erforderlich;
- Initialisierung;
- bereit;
- Suche;
- Peer gefunden;
- Verbindung;
- Gruppe gebildet;
- LETCOOR-Authentifizierung;
- verbunden;
- Wiederherstellung;
- nicht verfügbar.

## 26.4 Wi‑Fi Direct belegt

Wenn Android meldet, dass Wi‑Fi Direct belegt ist, kann LETCOOR eine Wiederherstellung versuchen. Der Wi‑Fi-Direct-Informationsbildschirm empfiehlt insbesondere zu prüfen:

- ob WLAN aktiv ist;
- ob Tethering/Hotspot mit Wi‑Fi Direct in Konflikt steht;
- ob bereits eine andere Wi‑Fi-Direct-Suche/-Verbindung läuft.

## 26.5 Das Netzwerk kann den Transportweg wechseln

Der Status oben auf dem Bildschirm kann während der Sitzung verschiedene Transportwege anzeigen. LETCOOR kann alternative Routen zu einem Peer besitzen und je nach Netzwerkzustand die verfügbare Route verwenden.

---

# 27. Datenschutz, Sperrung und Wiederherstellung

LETCOOR wendet mehrere Schutzmechanismen an, wenn private Daten einer Gruppe nicht mehr mit anderen Mitgliedern verifiziert werden können.

## 27.1 Sperrung nach Abwesenheit

Der Oberflächencode sieht einen Bildschirm vor:

**Sitzung nach einer Minute Abwesenheit gesperrt.**

Drücken Sie **Neu verbinden**, um wieder Zugriff zu erhalten.

## 27.2 Verbindung zu Mitgliedern prüfen

Wenn eine Datenschutzwiederherstellung erforderlich ist, zeigt LETCOOR:

**Verbindung zu Mitgliedern wird geprüft…**

Es versucht, ein erreichbares Mitglied zu finden, und kann Details zu Näherungstransporten anzeigen.

## 27.3 Automatische lokale Löschung

Bei bestimmten Gruppen, die für automatische Wiederherstellung konfiguriert sind, können die lokalen Gruppendaten **nach einer Prüfung** gelöscht werden, wenn innerhalb des vorgesehenen Zeitraums keine erneute Verbindung möglich ist.

Die aktuelle Benutzeroberfläche nennt für betroffene Gruppen eine Frist von zwanzig Minuten.

Wenn angeboten, können Sie:

- lokale Daten löschen/zurücksetzen;
- oder **Daten auf eigenes Risiko behalten** wählen, wodurch die automatische Löschung für diesen Kontext deaktiviert wird.

LETCOOR warnt davor, dass das Behalten dieser Daten das Risiko bei einer physischen Kompromittierung des Geräts erhöhen kann.

## 27.4 Desktop-Schutz

Auf dem Desktop kann die private Ansicht ausgeblendet/unscharf dargestellt werden, wenn das Fenster den Fokus verliert, und vor der erneuten Anzeige aktualisiert werden.

---

# 28. Verfügbare Rollen

Das LETCOOR-Domänenmodell definiert neun Rollen.

| Rolle | Allgemeine Funktion im aktuellen Code |
|---|---|
| **Gruppenadministrator** (`GROUP_ADMIN`) | Gruppenverwaltung, Erstellung von Teams und Sitzungen, Verwaltung von Mitgliedern/Rollen, Kampagnen, Auflösung, Übertragung der Verwaltung, Ankündigungen. |
| **Gruppenkoordinator** (`GROUP_LEADER`) | Koordination auf Gruppenebene, Gruppenbefehle/-ziele/-meldungen, Kampagnen und Ankündigungen gemäß Berechtigungen. |
| **Teamleiter** (`TEAM_LEADER`) | Befehle/Ziele/Treffpunkte/Status seines Teams, Austausch zwischen Teams, Ankündigungen, Teamkampagnen. |
| **Gruppen-Scout** (`GROUP_SCOUT`) | Meldungen sowie Bestätigung/Hochstufung auf Gruppenebene gemäß Berechtigungen. |
| **Team-Scout** (`TEAM_SCOUT`) | Teambericht/-meldung, Bestätigung und Hochstufung gemäß Berechtigungen. |
| **Relay** (`TRANSMITTER`) | Vom Domänenmodell vorgesehene Relay-Fähigkeit und Veröffentlichung bestimmter zusammengefasster Präsenzdaten gemäß Richtlinie; diese Rolle gewährt keinen Zugriff auf private Daten anderer Teams. |
| **Deckung** (`COVER`) | Operative Kennzeichnung mit den grundlegenden Fähigkeiten eines Mitglieds. |
| **Angriff** (`ATTACKER`) | Operative Kennzeichnung mit den grundlegenden Fähigkeiten eines Mitglieds. |
| **Mitglied** (`MEMBER`) | Grundlegende Fähigkeiten: normale Meldung im eigenen Team, wenn erlaubt, Sicherheitswarnung, Antwort auf Befehle, erlaubte Präsenz und Teilnahme an Kampagnen. |

> Berechtigungen werden vom Core berechnet und sind additiv. Die Oberfläche zeigt nur tatsächlich erlaubte Aktionen an. Die Zugehörigkeit zu einer Gruppe gewährt nicht automatisch Zugriff auf die privaten Daten aller ihrer Teams.

---

# 29. Vorbereitungstipps vor einer Aktivität

Für den realen Einsatz, insbesondere in einem Gebiet mit möglicherweise schlechter Internetverbindung:

1. Installieren Sie dieselbe LETCOOR-Version auf allen Geräten.
2. Erstellen Sie die Gruppe vor Beginn der Aktivität.
3. Lassen Sie die Teilnehmer beitreten, solange sie sich noch physisch nahe beieinander befinden.
4. Akzeptieren Sie auf jedem Android-Gerät die Näherungsberechtigungen.
5. Aktivieren Sie Bluetooth und WLAN.
6. Testen Sie mindestens eine Verbindung ohne mobile Daten, wenn der Offline-Betrieb wichtig ist.
7. Erstellen Sie die Teams und bestimmen Sie die Leiter, bevor sich die Teilnehmer verteilen.
8. Öffnen Sie eine Sitzung, wenn Sie sitzungsbezogene Rollen/Zuweisungen und den entsprechenden Verlauf wünschen.
9. Laden Sie die erforderlichen Offline-Karten herunter, bevor die Internetverbindung verloren geht.
10. Stellen Sie sicher, dass die Teilnehmer wissen, wie sie Folgendes öffnen:
    - Benachrichtigungen;
    - Führung;
    - ihr Team;
    - die Funktion Sicherheitswarnung.
11. Aktivieren Sie die Standortfreigabe nur, wenn Sie die Position tatsächlich veröffentlichen möchten.

---

# 30. Fehlerbehebung

## Die beiden Geräte sehen sich offline nicht

Prüfen Sie auf beiden Geräten:

- WLAN aktiviert;
- Bluetooth aktiviert;
- Berechtigungen für **Geräte in der Nähe** erteilt;
- Berechtigung für lokales Netzwerk erteilt, wenn Android danach fragt;
- App sichtbar/erkennbar, wenn das System eine Bestätigung verlangt;
- LETCOOR während der anfänglichen Suche im Vordergrund.

Wenn Android die Standorteinstellungen öffnet, aktivieren Sie den Standortdienst, um die Kompatibilität der Erkennung zu maximieren. Dadurch wird die LETCOOR-Standortfreigabe nicht aktiviert.

## „Wi‑Fi Direct nicht verfügbar“ oder „belegt“

- deaktivieren Sie vorübergehend ein manuelles Tethering/Hotspot;
- warten Sie einige Sekunden;
- starten Sie den Versuch erneut;
- prüfen Sie, ob eine andere Anwendung oder Wi‑Fi-Direct-Verbindung aktiv ist.

## Der QR-Code funktioniert nicht

- warten Sie, bis alle Teile des QR-Codes gelesen wurden;
- bringen Sie die Bildschirme näher zusammen;
- erhöhen Sie die Helligkeit des Bildschirms, auf dem der QR-Code angezeigt wird;
- verwenden Sie den Zoom-Regler der Kamera;
- verwenden Sie bei Bedarf den Link anstelle des QR-Codes.

## Kamerazugriff verweigert

- verwenden Sie den Link;
- oder öffnen Sie die Kameraeinstellungen von Windows/Android aus LETCOOR heraus, wenn die Schaltfläche angeboten wird.

## Der Link wird akzeptiert, aber die Verbindung läuft ab

- prüfen Sie Internet oder Nähe;
- bringen Sie die Geräte näher zusammen;
- aktivieren Sie WLAN und Bluetooth;
- akzeptieren Sie Systemdialoge;
- drücken Sie **Erneut versuchen**, wenn die Schaltfläche erscheint.

## Ich bin in der Gruppe, aber nicht in einem Team

Öffnen Sie:

**Kontext > Teams** oder **Verwaltung**.

Wenn das Team den Beitritt erlaubt, verwenden Sie **Beitreten**. Eine Teameinladung kann den Teilnehmer abhängig vom erhaltenen Ticket auch direkt in die übergeordnete Gruppe und das Zielteam aufnehmen.

## „Mitgliedschaft registriert · Schlüssel werden empfangen“

Die Mitgliedschaft ist bekannt, aber der kryptografische Zugriff auf das Team ist noch nicht bereit. Lassen Sie die Geräte verbunden, damit die Schlüssel abgerufen/synchronisiert werden können. Wenn in Verwaltung die Schaltfläche **Zugriff wiederherstellen** erscheint, verwenden Sie sie.

## Ein Objekt ist nicht sichtbar

Prüfen Sie:

- die ausgewählte Gruppe/das ausgewählte Team;
- Ihre Berechtigungen;
- den Ablauf des Objekts;
- die Netzwerksynchronisierung;
- dass ein privates Teamobjekt nicht automatisch für andere Teams sichtbar ist.

## Der Standort wird nicht angezeigt

- prüfen Sie die Standortberechtigung;
- prüfen Sie, ob **Meinen Standort teilen** ausgewählt ist;
- prüfen Sie die aktuelle Gruppe;
- warten Sie auf die nächste regelmäßige Veröffentlichung;
- prüfen Sie, ob die Teamrichtlinie die erforderliche Genauigkeit erlaubt.

---

# 31. Kurzübersicht

## LETCOOR beitreten

```text
Einladender
  ↓
Einladen
  ↓
QR oder Link
  ↓
Eingeladenes Gerät importiert
  ↓
Eingeladenes Gerät erzeugt eine Antwort
  ↓
Einladender scannt/fügt die Antwort ein
  ↓
Verbindung + Authentifizierung + Aufnahme
```

## Etwas auf der Karte erstellen

```text
Lange auf die Karte drücken
  ↓
Meldung / Ziel / Befehl / Sammelpunkt / Sicherheitswarnung
  ↓
Formular ausfüllen
  ↓
Bereich / Dauer wählen, falls verfügbar
  ↓
Veröffentlichen
```

## Eine Gruppe verwalten

```text
Gruppenname oben links
  ↓
Kontext | Teams | Teilnehmer | Einladen | Operationen | Verwaltung | Einstellungen
```

## Für eine Rollenkampagne

```text
Operationen
  ↓
Rollen
  ↓
Rolle + Modus + Plätze + Dauer wählen
  ↓
Kampagne öffnen
  ↓
Mitglieder treten bei
  ↓
Automatische Zuweisung oder Bestätigung durch Verantwortlichen je nach Modus
```

## Ohne Internet arbeiten

```text
WLAN EIN
Bluetooth EIN
Näherungsberechtigungen erlaubt
Lokales Netzwerk erlaubt, falls angefordert
Kopplung/Sichtbarkeit akzeptiert, falls angefordert
Geräte beim ersten Kontakt nahe beieinander
LETCOOR im Vordergrund geöffnet
```

LETCOOR kann anschließend die verfügbaren Transportwege verwenden und autorisierte Informationen entsprechend der Mesh-Topologie zwischen Peers weiterleiten.

---

**LETCOOR 1.0.0 — Benutzerdokumentation**
