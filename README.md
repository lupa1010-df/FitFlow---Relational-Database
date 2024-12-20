# FitFlow---Relational-Database
# 🏋️‍♂️ FitFlow - Deine persönliche Fitness Journey

FitFlow ist ein Datenbankkonzept für eine moderne Fitness-Tracking-App. Das Konzept zeigt die grundlegende Struktur einer relationalen Datenbank, die als Basis für eine vollwertige Fitness-App dienen könnte. Der Fokus liegt auf der durchdachten Datenbankarchitektur, die eine effiziente Verwaltung von Benutzerdaten, Trainingsplänen und Trainingsprotokollen ermöglicht.

## 📝 Konzeptübersicht

Dieses Repository enthält das Datenbankkonzept für eine potenzielle Fitness-App mit folgenden konzeptionellen Komponenten:

- **Benutzerverwaltung**: Strukturierte Speicherung von Benutzerdaten
- **Trainingsplandatenbank**: Framework für individuelle Trainingsprogramme
- **Übungskatalog**: Systematische Erfassung von Übungen
- **Protokollierung**: Struktur für detailliertes Training-Tracking

## 💾 Datenbankstruktur

Das Kernstück des Konzepts ist die relationale Datenbankstruktur:

### Haupttabellen:

1. **Benutzer**
   - ID (Primary Key)
   - Vorname (Not Null)
   - Nachname (Not Null)
   - Geburtstag (Not Null)
   - Email (Unique)(Not Null)
   - Benutzername (Unique)
   - Passwort (Not Null)
   - Erstellungsdatum (Not Null)

2. **Trainingspläne**
   - ID (Primary Key)
   - Name (Not Null)
   - Beschreibung (Not Null)
   - Dauer (Not Null)
   - Intensität (Not Null)

3. **Übungen**
   - ID (Primary Key)
   - Name (Not Null)
   - Beschreibung

4. **Protokoll**
   - ID (Primary Key)
   - Trainingspläne_ID (Foreign Key)
   - Übung_ID (Foreign Key)
   - Benutzer_ID (Foreign Key)
   - Gewicht
   - Datum
   - Dauer
   - Bemerkungen

### Verknüpfungstabellen:

1. **Benutzer_Trainingspläne**
   - Benutzer_ID (Foreign Key)
   - Trainingspläne_ID (Foreign Key)
   - PRIMARY KEY (Benutzer_ID, Trainingspläne_ID)

2. **Trainingsplan_Übungen**
   - Trainingspläne_ID (Foreign Key)
   - Übung_ID (Foreign Key)
   - Anzahl_Wiederholungen (Not Null)
   - Anzahl_Sätze (Not Null)
   - PRIMARY KEY (Trainingspläne_ID, Übung_ID)

## 🔄 Beziehungen

Das Datenbankkonzept ermöglicht folgende Beziehungen:

- **N:M Benutzer-Trainingspläne**: Benutzer können mehrere Trainingspläne haben und Trainingspläne können mehreren Benutzern zugeordnet sein
- **N:M Trainingsplan-Übungen**: Trainingspläne bestehen aus mehreren Übungen mit spezifischen Wiederholungen und Sätzen
- **1:N Protokollierung**: Jede Trainingseinheit wird einem Benutzer, einem Trainingsplan und einer Übung zugeordnet

## 💡 Potenzielle Implementierungsmöglichkeiten

Das Konzept könnte als Grundlage für verschiedene Anwendungen dienen:

- Web-basierte Fitness-Tracking-Plattform
- Mobile Fitness-App
- Gym-Management-System
- Personal Trainer Verwaltungssoftware

## 📈 Erweiterungsmöglichkeiten

Das Datenbankkonzept könnte erweitert werden um:

- Ernährungstracking
- Körpermaße und Gewichtsverlauf
- Workout-Kategorien
- Soziale Funktionen
- Leistungsstatistiken

## 🤝 Feedback und Beiträge

Da dies ein Konzept ist, sind Feedback und Verbesserungsvorschläge zur Datenbankstruktur besonders willkommen. Erstelle gerne ein Issue für:
- Vorschläge zur Optimierung der Tabellenstruktur
- Ideen für zusätzliche Attribute
- Verbesserungen der Beziehungen zwischen den Tabellen

## 📞 Kontakt

Bei Fragen zum Datenbankkonzept oder Vorschlägen zur Verbesserung:

**Paul Bacher**
- Email: paulbacher@hotmail.com
- GitHub: lupa1010-df

---

Entwickelt als Datenbankkonzept für moderne Fitness-Anwendungen
