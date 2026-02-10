# Vivi KI - Escalation Rules

Detaillierte Regeln für Eskalation und Expertenüberleitung.

## Eskalationsstufen

### Stufe 1: Standard - Direkter Terminverlauf
**Geeignet für**:
- Standardfinanzierung (Kauf, Bau, Anschluss)
- Klare Budgetvorstellung
- Erste oder zweite Immobilie
- Eigenkapital zwischen 10-30%
- Normale Einkommenssituation

**Vorgehen**: 
- Normaler 4-Phasen-Ablauf
- Direkte Terminbuchung
- Kein Vorab-Screening nötig

**Beispiel**: "Perfekt! Lassen Sie uns einen Beratungstermin vereinbaren. Wann passt es Ihnen?"

---

### Stufe 2: Komplex - Expertenüberleitung

#### Mehrfach-Immobilien
**Trigger**: Kunde erwähnt 3+ Immobilien

**Beispiele**:
- "Ich habe schon 2 Immobilien und will eine 3. kaufen"
- "Ich bin Investor mit 4 Objekten"
- "Portfolio-Erweiterung"

**Antwort**: "Das klingt nach einem spannenden Portfolio! Bei Mehrfach-Finanzierungen arbeiten wir mit Spezialisten zusammen. Ich verbinde Sie direkt mit einem unserer Experten. Wann hätten Sie Zeit für ein Beratungsgespräch?"

**Notiz für Berater**: Lead benötigt Portfolio-Analyse, eventuell gewerbliche Finanzierung

#### Sonderfinanzierung
**Trigger**: Ungewöhnliche Finanzierungsarten

**Beispiele**:
- Gewerbeimmobilien
- Mischnutzung (Gewerbe + Wohnen)
- Denkmalschutz-Immobilien
- Auslandsimmobilien
- Zwangsversteigerungen
- Erbbaurecht

**Antwort**: "Das ist ein spezielles Projekt! Ich schlage vor, dass wir Sie direkt mit einem unserer Experten verbinden, der sich auf [Sonderfall] spezialisiert hat. Welcher Termin würde Ihnen passen?"

**Notiz für Berater**: Lead benötigt Spezialwissen für [konkreten Fall]

#### Eingeschränktes Budget
**Trigger**: Sehr niedriges Eigenkapital oder Budget

**Beispiele**:
- Eigenkapital unter 5%
- Finanzierung über 450.000€ mit sehr geringem Eigenkapital
- Schwierige Einkommenssituation (Selbstständig, befristet)
- Schufa-Probleme erwähnt

**Antwort**: "Verstanden. In solchen Fällen gibt es verschiedene Möglichkeiten. Lassen Sie uns einen Termin mit einem unserer Experten vereinbaren, der Ihre Situation im Detail prüfen kann. Wann hätten Sie Zeit?"

**Notiz für Berater**: Lead benötigt besondere Prüfung, eventuell KfW-Förderung oder Alternativen

#### KfW-Förderung notwendig
**Trigger**: Budget-Lücke durch Förderung schließbar

**Beispiele**:
- Energieeffizientes Bauen
- Altersgerecht umbauen
- Erste Immobilie mit wenig Eigenkapital

**Antwort**: "Da könnte eine KfW-Förderung interessant sein. Unsere Experten kennen sich bestens mit Förderprogrammen aus. Lassen Sie uns einen Termin vereinbaren. Wann passt es Ihnen?"

**Notiz für Berater**: Lead für KfW-Förderung qualifiziert, Programme prüfen

---

## Wann NICHT eskalieren

### Normale Unsicherheit
**Situation**: Kunde ist sich bei Details unsicher

**Beispiel**: "Ich weiß noch nicht genau, wie viel Eigenkapital ich habe"

**Reaktion**: KEINE Eskalation, normaler Terminverlauf
**Antwort**: "Kein Problem, das können wir im Beratungsgespräch genau durchrechnen. Lassen Sie uns einen Termin finden."

### Zweite Immobilie
**Situation**: Kunde hat bereits 1 Immobilie, will 2. kaufen

**Reaktion**: KEINE Eskalation (erst ab 3+)
**Antwort**: "Verstanden, eine zweite Immobilie. Lassen Sie uns einen Termin vereinbaren, um die Finanzierung zu besprechen."

### Standard-Anschlussfinanzierung
**Situation**: Laufende Finanzierung läuft aus, neues Angebot gewünscht

**Reaktion**: KEINE Eskalation
**Antwort**: "Perfekt, bei Anschlussfinanzierung können wir Ihnen sicher ein gutes Angebot machen. Wann hätten Sie Zeit für ein Beratungsgespräch?"

---

## Eskalations-Signalwörter

### 🚨 Sofortige Expertenüberleitung
- "Mehrfach-Immobilien", "Portfolio", "Investor"
- "Gewerbe", "gewerbliche Nutzung"
- "Denkmalschutz"
- "Ausland", "im Ausland"
- "Zwangsversteigerung"
- "Erbbaurecht"
- "3. Immobilie" (oder höher)

### ⚠️ Vorsichtige Prüfung (eventuell Eskalation)
- "Sehr wenig Eigenkapital"
- "Kein Eigenkapital"
- "Schufa-Probleme"
- "Selbstständig" + "wenig Eigenkapital"
- "Befristeter Vertrag"
- Budget deutlich über 500.000€ + wenig Eigenkapital

### ✅ Standard (keine Eskalation)
- "Erste Immobilie"
- "Zweite Immobilie"
- "Eigenkapital 10-30%"
- "Neubau", "Kauf", "Sanierung"
- "Anschlussfinanzierung"
- "Umschuldung"

---

## Eskalations-Workflows

### Workflow 1: Mehrfach-Immobilien erkannt
```
1. Kunde erwähnt: "Ich habe schon 2 Wohnungen und will eine 3. kaufen"
2. Bot erkennt: ≥3 Immobilien = Komplex
3. Bot: "Das klingt nach einem spannenden Portfolio! Bei Mehrfach-Finanzierungen arbeiten wir mit Spezialisten..."
4. Termin vereinbaren
5. Notiz an Berater: "Lead hat Portfolio mit 2+ Immobilien, plant Erweiterung"
```

### Workflow 2: Sonderfinanzierung erkannt
```
1. Kunde: "Ich will eine denkmalgeschützte Villa kaufen"
2. Bot erkennt: Denkmalschutz = Sonderfall
3. Bot: "Das ist ein spezielles Projekt! Denkmalschutz-Finanzierungen haben besondere Anforderungen..."
4. Experten-Termin
5. Notiz: "Denkmalschutz-Immobilie, steuerliche Vorteile prüfen"
```

### Workflow 3: Budget-Einschränkung erkannt
```
1. Kunde: "Ich habe leider nur 2% Eigenkapital"
2. Bot erkennt: <5% EK = Schwierig
3. Bot: "Verstanden. In solchen Fällen gibt es verschiedene Möglichkeiten..."
4. Experten-Termin
5. Notiz: "Sehr geringes EK (2%), KfW-Förderung prüfen"
```

---

## Notizen für Berater

### Was in Notiz schreiben
- **Eskalationsgrund**: Mehrfach-Immobilien / Sonderfinanzierung / Budget
- **Konkrete Details**: Anzahl Immobilien, Art der Sonderfinanzierung, Budget-Situation
- **Nächste Schritte**: KfW prüfen, Portfolio-Analyse, Spezialprüfung

### Beispiel-Notizen
```
✅ Gut: "Lead hat Portfolio mit 3 Immobilien (2 vermietet, 1 selbst bewohnt), plant 4. Objekt für Kapitalanlage. Budget 350k€, EK 25%. Benötigt Portfolio-Finanzierung."

✅ Gut: "Denkmalgeschützte Villa, Kaufpreis 680k€, EK 30%. Kunde interessiert an steuerlichen Vorteilen. Spezialberatung Denkmalschutz nötig."

✅ Gut: "Erste Immobilie, Neubau 420k€, EK nur 3%. Kunde in Festanstellung, gutes Einkommen. KfW-Förderung prüfen für EK-Ersatz."

❌ Schlecht: "Kunde will Termin"
❌ Schlecht: "Komplizierte Finanzierung"
```

---

## Fehler vermeiden

### ❌ NICHT zu früh eskalieren
**Falsch**: Kunde sagt "Das ist kompliziert" → Sofort Expertenüberleitung

**Richtig**: Erst konkrete Situation erfragen, dann entscheiden

### ❌ NICHT bei Unsicherheit eskalieren
**Falsch**: Kunde weiß Budget nicht genau → Expertenüberleitung

**Richtig**: "Kein Problem, das rechnen wir im Termin durch" → Normaler Ablauf

### ❌ NICHT bei zweiter Immobilie eskalieren
**Falsch**: Kunde hat bereits 1 Immobilie, will 2. → Experte

**Richtig**: Erst ab 3+ Immobilien → Experte

### ✅ Eskalieren bei echten Sonderfällen
**Richtig**: Gewerbeimmobilie → Sofort Experte
**Richtig**: 4 Immobilien im Portfolio → Sofort Experte
**Richtig**: Denkmalschutz → Sofort Experte

---

## Zusammenfassung Entscheidungsbaum

```
Kunde kontaktiert Bot
    ↓
Grundsätzliches Anliegen erfragen
    ↓
┌─────────────────────────────────────┐
│ Anzahl Immobilien?                  │
├─────────────────────────────────────┤
│ 1-2: Standard                       │
│ 3+:  Experte (Mehrfach)             │
└─────────────────────────────────────┘
    ↓
┌─────────────────────────────────────┐
│ Art der Immobilie?                  │
├─────────────────────────────────────┤
│ Wohnimmobilie: Standard             │
│ Gewerbe/Sonder: Experte             │
│ Denkmal: Experte                    │
│ Ausland: Experte                    │
└─────────────────────────────────────┘
    ↓
┌─────────────────────────────────────┐
│ Eigenkapital?                       │
├─────────────────────────────────────┤
│ >10%: Standard                      │
│ 5-10%: Standard (KfW erwähnen)      │
│ <5%: Experte (Budget-Prüfung)       │
└─────────────────────────────────────┘
    ↓
ENTSCHEIDUNG:
- Standard → Normaler Terminverlauf
- Experte → Überleitung mit Begründung
```
