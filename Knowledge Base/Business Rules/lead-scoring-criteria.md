# Lead Scoring Kriterien - Business Rules

## Übersicht
Definiert die Bewertungskriterien für Lead-Klassifikation A/B/C basierend auf Business-Erfahrung und Conversion-Statistiken.

## Klasse A - Sehr guter Fit (Conversion Rate: ~75-85%)

### Zeitfenster 
- **Optimal**: 0-3 Monate bis Finanzierungsbedarf
- **Akzeptabel**: 3-6 Monate bei konkretem Projekt
- **Indikator**: Kaufvertrag bereits unterschrieben, Notar-Termine geplant

### Eigenkapital-Situation
- **Mindeststandard**: 15-20% der Finanzierungssumme verfügbar
- **Optimal**: 20-30% Eigenkapital
- **Qualität**: Bausparverträge, Sparguthaben, Wertpapiere (liquide Mittel)
- **Ausschlusskriterium**: Geschenktes/geerbtes EK ohne Nachweis

### Einkommenssituation
- **Faustregmel**: Netto-Haushaltseinkommen ≥ 3x gewünschte Monatsrate
- **Unbefristet**: Angestellte mit Arbeitsvertrag >2 Jahre beim aktuellen Arbeitgeber
- **Selbständige**: >3 Jahre Geschäftstätigkeit, BWA der letzten 2 Jahre positiv
- **Beamte/öD**: Besonders positiv bewertet (Jobsicherheit)

### Bonität & Schufa
- **Score**: >95% (sehr gut bis gut)
- **Keine negativen Einträge**: Kredkarten-Rückstände, Mahnverfahren, etc.
- **Bestehende Kredite**: <30% des Nettoeinkommens für laufende Verpflichtungen

### Projekt-Konkretheit
- **Immobilie**: Bereits gefunden und reserviert
- **Finanzierungssumme**: Realistisch kalkuliert (Kaufpreis + Nebenkosten)
- **Region**: Bekannte Lage mit stabilen/steigenden Immobilienpreisen

## Klasse B - Guter Fit (Conversion Rate: ~45-60%)

### Ein Hauptfaktor schwächer als Klasse A:

#### Zeitfenster
- **Mittelfristig**: 6-12 Monate Finanzierungsbedarf
- **Projektphase**: Immobiliensuche läuft aktiv
- **Indikator**: Besichtigungen laufen, aber noch kein Kaufvertrag

#### Eigenkapital 
- **Knapp**: 10-15% verfügbar
- **Alternative Quellen**: Familienunterstützung geplant aber nicht garantiert
- **Aufbau**: Aktiv Eigenkapital ansparen, aber zeitlich knapp

#### Einkommen
- **Grenzwertig**: 2.5-3x Monatsrate als Netto-Haushaltseinkommen  
- **Befristet**: Arbeitsvertrag läuft aus, aber Verlängerung wahrscheinlich
- **Selbständige**: 2-3 Jahre Geschäftstätigkeit, schwankende Ergebnisse

#### Bonität
- **Score**: 90-95% (befriedigend bis gut)
- **Kleinere Einträge**: Alte, erledigte Einträge vorhanden
- **Laufende Kredite**: 30-40% des Nettoeinkommens

#### Projekt
- **Immobilie**: Mehrere Optionen in Prüfung
- **Budget**: Grober Rahmen definiert, Details offen
- **Region**: Mittlere Lage, normale Marktentwicklung

## Klasse C - Schwächerer Lead (Conversion Rate: ~15-25%)

### Mehrere Faktoren problematisch:

#### Zeitfenster
- **Langfristig**: >12 Monate oder "irgendwann"
- **Unkonkret**: "Schaue mich erstmal um"
- **Träumerei**: Unrealistische Vorstellungen ohne konkrete Pläne

#### Eigenkapital
- **Sehr wenig**: <10% der Finanzierungssumme
- **Fehlt komplett**: 100%-Finanzierung gewünscht
- **Unsicher**: "Wir schauen, was möglich ist"

#### Einkommen
- **Zu niedrig**: <2.5x gewünschte Monatsrate
- **Unsicher**: Probezeit, befristete Verträge, Arbeitslosigkeit
- **Selbständige**: <2 Jahre oder negative Entwicklung
- **Studenten/Azubis**: Noch kein stabiles Einkommen

#### Bonität
- **Problematisch**: <90% Schufa-Score
- **Negative Einträge**: Laufende Mahnverfahren, hohe Kreditbelastung
- **Überschuldung**: >50% des Einkommens für bestehende Kredite

#### Projekt
- **Unrealistisch**: Budget und Wünsche passen nicht zusammen
- **Traumschloss**: Luxus-Vorstellungen ohne entsprechendes Budget
- **Problemlagen**: Schwierige Regionen, fallende Immobilienpreise

## Sonderfälle & Ausnahmen

### Upgrade-Möglichkeiten
- **Bürgschaft**: Eltern/Familie übernehmen Bürgschaft → B wird zu A
- **Zusätzliches EK**: Kurzfristig verfügbar → C wird zu B oder A
- **Jobwechsel**: Neuer, besserer Job in Aussicht → Upgrade möglich

### Downgrade-Risiken  
- **Überschätzung**: Unrealistische Selbsteinschätzung → niedriger bewerten
- **Marktveränderung**: Zinsanstieg, Immobilienpreise → Vorsicht bei Grenzfällen
- **Lebensereignisse**: Trennung, Jobverlust, Krankheit → Risikoabschläge

## Regionale Besonderheiten

### Top-Lagen (München, Hamburg, Stuttgart)
- **A-Leads**: Besonders hohe EK-Anforderungen (25-30%)
- **Preisdynamik**: Schnelle Entscheidungen nötig
- **Konkurrenz**: Viele Mitbewerber um Objekte

### Standard-Regionen
- **Normale Kriterien**: Wie oben definiert
- **Mittlere Preise**: Durchschnittliche Finanzierungsvolumina
- **Stabile Märkte**: Planbare Entwicklung

### Strukturschwache Gebiete
- **Vorsicht**: Auch A-Kriterien können riskant sein
- **Wertstabilität**: Immobilie als Sicherheit fraglich
- **Exit-Strategien**: Verkauf schwierig

## Scoring-Algorithmus Empfehlung

```yaml
scoring_weights:
  zeitfenster: 25%
  eigenkapital: 30%  
  einkommen: 25%
  bonität: 15%
  projekt_konkreheit: 5%

classification_logic: |
  IF weighted_score >= 80% AND no_exclusion_criteria THEN A-LEAD
  ELSE IF weighted_score >= 60% THEN B-LEAD  
  ELSE C-LEAD

exclusion_criteria:
  - schufa_score < 85%
  - income_ratio < 2.0
  - eigenkapital_prozent < 5%
  - zeitfenster > 18_months AND projekt_unkonkret
```

## Validierung & Updates

### Monatliche Reviews
- **Conversion-Tracking**: Tatsächliche A/B/C Performance messen
- **Kriterien-Anpassung**: Bei signifikanten Abweichungen
- **Markt-Updates**: Zins- und Marktentwicklungen berücksichtigen

### Saisonale Anpassungen  
- **Q4**: Jahresend-Käufe, steuerliche Optimierung
- **Q1**: Neujahrs-Vorsätze, aber oft wenig konkret
- **Frühjahr**: Hauptsaison für Immobilien-Käufe
- **Sommer**: Familienplanung, Schulwechsel-Termine

---

**Wichtig**: Diese Kriterien sind Richtlinien basierend auf historischen Daten. Jeder Lead sollte individuell betrachtet werden, besonders bei Sonderfällen oder sich ändernden Marktbedingungen.