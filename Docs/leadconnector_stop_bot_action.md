# Stop Bot Action — LeadConnector Documentation

*Stand: 13. Februar 2025*

## 📖 Inhaltsverzeichnis
- Einführung  
- Schritt-für-Schritt Anleitung zur Einrichtung  
  - Schritt 1: Bot Goals Tab öffnen  
  - Schritt 2: Stop Bot Button auswählen  
  - Schritt 3: Einstellungen konfigurieren  
- Wichtige Hinweise zu Stop-Bot-Bedingungen  

---

## Einführung
Die **Stop Bot Action**-Funktion ermöglicht es, den KI-Bot automatisch zu stoppen, wenn bestimmte **Trigger-Bedingungen** während einer Unterhaltung erfüllt werden.  
Das verhindert unnötige Nachrichten zwischen Bot und Kontakt und verbessert die Nutzererfahrung.

**Beispiele:**
- Wenn ein Nutzer „Goodbye“ schreibt, hört der Bot automatisch auf zu antworten.  
- Wenn ein Kunde kein Interesse zeigt, kann die Konversation gestoppt werden, um Spam oder Überkommunikation zu vermeiden.

---

## Schritt-für-Schritt Anleitung

### 🧭 Schritt 1: Bot Goals Tab öffnen
Wenn du einen neuen Bot erstellst, vergib oder bearbeite zuerst seinen **Namen**, bevor du fortfährst.

### ⚙️ Schritt 2: Stop Bot Button auswählen
Navigiere in den **Bot Goals**-Bereich und klicke auf den Button **Stop Bot**, um die Funktion zu öffnen.

### 🔧 Schritt 3: Einstellungen konfigurieren

#### 1. Szenarioname
Gib dem Szenario einen Namen, um die Bedingung leichter zu identifizieren.  
➡️ Beispiel: `Customer Not Interested Scenario`

#### 2. Szenario aktivieren
Schalte den Toggle **Enable Scenario** auf **On**, damit die Funktion aktiv wird.

#### 3. Trigger-Bedingung festlegen
Beschreibe die Bedingung, bei der der Bot stoppen soll.  
Beispiele:
- „Customer not interested in the product.“  
- „User says goodbye.“

#### 4. Beispielphrasen hinzufügen
Ergänze Beispielphrasen, die den Stopp auslösen sollen, um das Erkennungsverhalten des Bots zu trainieren.

**Beispiel:**
```text
Not Interested
I don’t like the product
Goodbye
Thank you, have a nice day
```

#### 5. Final Message
Definiere die **Abschlussnachricht**, die der Bot senden soll, bevor er inaktiv wird.  
Beispiel:  
> „Thank you for your time. If you have any other questions, feel free to ask.“

#### 6. Reaktivierungs-Timer
Lege fest, wann der Bot für denselben Kontakt wieder aktiviert werden darf.

- Standardwert: **24 Stunden**  
- Empfehlung: **5–10 Minuten**, wenn der Bot zeitnah wieder ansprechbar sein soll.

#### 7. Custom Tag (optional)
Füge einen **benutzerdefinierten Tag** hinzu, wenn der Stop-Bot-Trigger aktiviert wird.  
Dieser Tag kann in Workflows für **Nachfassaktionen** verwendet werden.

Beispiel:  
- Standard-Tag: `stop bot`  
- Eigene Option: `customer_not_interested`

---

## 🧠 Wichtige Hinweise zu Stop-Bot-Bedingungen

Wenn die Bedingungen korrekt definiert sind, **stoppt der Bot automatisch**, sobald sie eintreten.  
Das sorgt für präzisere, kontextbezogene Kommunikation.

### 🔍 Best Practices
1. **Eindeutige Trigger formulieren:** Vermeide zu allgemeine Phrasen, damit der Bot nicht zu früh stoppt.  
2. **Szenarien testen:** Prüfe nach der Einrichtung, ob der Bot korrekt reagiert und nicht unerwartet aufhört.

### ⚠️ Beispiel
> Wenn ein Kunde kein Interesse am Produkt zeigt, kann der Bot dennoch Leads pflegen, sofern dies im Prompt vorgesehen ist.  
Ein zu früher Stopp könnte hier eine Chance auf Engagement verhindern.

---

© LeadConnector 2025 — Stop Bot Action Guide
