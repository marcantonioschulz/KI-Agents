# Content Generation Automation Template

## Metadata
```yaml
template_type: "content_generation"
version: "1.0"
purpose: "Standardized template for dynamic content generation prompts"
output_format: "Formatted text/HTML with merge field integration"
integration_platforms: ["GoHighLevel", "LeadConnector", "Email Systems"]
```

## Template Structure

### Aufgabe
[Beschreibung der Content-Generation-Aufgabe - welche Art von Inhalten sollen erstellt werden?]

### Content-Typen

#### [CONTENT-TYP-1] - [Beschreibung]
- **Zweck**: [Ziel und Verwendung des Contents]
- **Stil**: [Tonalität und Schreibstil]
- **Länge**: [Wortanzahl oder Zeichenlimit]
- **Personalisierung**: [Welche Merge Fields werden verwendet]

#### [CONTENT-TYP-2] - [Beschreibung]
- **Zweck**: [Ziel und Verwendung des Contents]
- **Stil**: [Tonalität und Schreibstil]  
- **Länge**: [Wortanzahl oder Zeichenlimit]
- **Personalisierung**: [Welche Merge Fields werden verwendet]

### Input-Variablen
```yaml
customer_data:
  - "{{contact.first_name}}"
  - "{{contact.last_name}}"
  - "{{contact.email}}"
  - "{{contact.phone}}"
  - "{{contact.lead_source}}"
  
context_variables:
  - "[context_field_1]": [Beschreibung]
  - "[context_field_2]": [Beschreibung]
  - "[context_field_3]": [Beschreibung]
  
business_logic:
  - "[business_rule_1]": [Details]
  - "[business_rule_2]": [Details]
```

### Output-Format

#### Für E-Mail Content:
```html
Betreff: [Dynamischer Betreff mit Personalisierung]

Sehr geehrte/r {{contact.first_name}} {{contact.last_name}},

[Personalisierte Einleitung basierend auf Context]

[Hauptinhalt mit relevanten Informationen]

[Call-to-Action oder nächste Schritte]

Mit freundlichen Grüßen
[Absender-Information]
```

#### Für SMS Content:
```text
Hallo {{contact.first_name}}, [kurze personalisierte Nachricht basierend auf Context]. [Call-to-Action]. LG Team Endlich zu Hause
```

### Content-Personalisierung

#### Personalisierungsebenen
1. **Basis**: Name und grundlegende Höflichkeit
2. **Kontext**: Bezug auf vorherige Interaktionen oder Lead-Source
3. **Individuell**: Spezifische Bedürfnisse oder Projektdetails
4. **Timing**: Berücksichtigung von Zeitfenstern und Dringlichkeit

#### Merge Field Integration
- **Standard Fields**: `{{contact.first_name}}`, `{{contact.last_name}}`, etc.
- **Custom Fields**: `{{contact.project_type}}`, `{{contact.budget_range}}`, etc.
- **Appointment Fields**: `{{appointment.date}}`, `{{appointment.time}}`, etc.

### Content-Varianten

#### Variante A: [Szenario-Beschreibung]
**Auslöser**: [Trigger-Bedingung]
**Template**: 
```
[Content-Template für Variante A]
```

#### Variante B: [Szenario-Beschreibung]
**Auslöser**: [Trigger-Bedingung]
**Template**:
```
[Content-Template für Variante B]
```

### Qualitätsrichtlinien

#### Sprache & Stil
- **Primärsprache**: Deutsch (formelles "Sie")
- **Tonalität**: Professionell, freundlich, vertrauensvoll
- **Fachsprache**: Verständlich erklären, Jargon vermeiden
- **Länge**: Prägnant aber vollständig

#### Compliance & Rechtliches
- **Datenschutz**: Keine sensiblen Daten in Content einbetten
- **Impressum**: Korrekte Absender-Informationen
- **Opt-out**: Abmelde-Möglichkeiten bei Marketing-Content
- **Finanzberatung**: Disclaimer bei Beratungshinweisen

### Test-Beispiele

#### Beispiel 1: Willkommens-E-Mail
**Input:**
```yaml
contact:
  first_name: "Max"
  last_name: "Mustermann" 
  email: "max.mustermann@example.com"
  lead_source: "Website Formular"
context:
  form_interest: "Baufinanzierung Neubau"
```

**Expected Output:**
```html
Betreff: Willkommen Max - Ihre Anfrage zur Baufinanzierung

Sehr geehrter Max Mustermann,

vielen Dank für Ihr Interesse an einer Baufinanzierung für Ihren Neubau. Wir haben Ihre Anfrage über unser Website-Formular erhalten und freuen uns, Ihnen weiterhelfen zu können.

Ein Experte aus unserem Team wird sich innerhalb der nächsten 24 Stunden bei Ihnen melden, um Ihre individuellen Wünsche zu besprechen.

Mit freundlichen Grüßen
Team Endlich zu Hause Finanzierungen
```

#### Beispiel 2: Termin-Reminder SMS
**Input:**
```yaml
contact:
  first_name: "Anna"
appointment:
  date: "15.10.2025"
  time: "14:00"
```

**Expected Output:**
```text
Hallo Anna, Erinnerung: Ihr Beratungstermin ist morgen um 14:00 Uhr. Bei Fragen: 0123-456789. LG Team Endlich zu Hause
```

### Fallback-Handling

#### Fehlende Personalisierung
```
Wenn {{contact.first_name}} leer: "Sehr geehrte Damen und Herren"
Wenn {{contact.last_name}} leer: Nur Vorname verwenden
Wenn beide Namen leer: Generische Anrede
```

#### Content-Ersatz
```
Wenn spezifischer Content nicht verfügbar: Generischen Ersatz-Content verwenden
Wenn Merge Fields fehlen: Platzhalter durch neutrale Formulierung ersetzen
```

### Integration Instructions

#### E-Mail Marketing System
1. **Setup**: Content-Template in System hinterlegen
2. **Trigger**: Workflow-Bedingung definieren  
3. **Personalization**: Merge Field Mapping konfigurieren
4. **Testing**: A/B-Tests für verschiedene Varianten

#### SMS Automation
1. **Character Limit**: 160 Zeichen beachten
2. **Personalization**: Minimale aber effektive Anrede
3. **Compliance**: Opt-out Mechanismus integrieren
4. **Timing**: Versandzeiten für beste Erreichbarkeit

---

**Usage Instructions**:
1. Template kopieren und anpassen
2. Alle [PLACEHOLDER] mit spezifischen Werten füllen
3. Test-Beispiele mit realen Daten validieren
4. Content-Qualität durch Stakeholder prüfen lassen
5. A/B-Tests für Performance-Optimierung einrichten