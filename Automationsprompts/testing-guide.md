# Automation Testing & Validation Guide

## Übersicht
Dieser Guide definiert standardisierte Testing-Verfahren für Automation Prompts, um Konsistenz, Zuverlässigkeit und Production-Readiness sicherzustellen.

## Test-Driven Development für Automationen

### Phase 1: Sample Data Creation
#### Realistische Test-Inputs erstellen
```yaml
test_data_categories:
  perfect_case:
    description: "Idealer Input mit allen erforderlichen Daten"
    example_count: 3
    
  partial_data:
    description: "Input mit fehlenden oder unvollständigen Informationen"
    example_count: 3
    
  edge_cases:
    description: "Grenzfälle, ungewöhnliche Werte, extreme Szenarien"
    example_count: 4
    
  invalid_input:
    description: "Fehlerhafte oder unleserliche Eingaben"
    example_count: 2
    
  multilingual:
    description: "Inputs in verschiedenen Sprachen oder mit Sonderzeichen"
    example_count: 2
```

#### Beispiel Test-Dataset für Lead Classification:
```json
{
  "perfect_cases": [
    {
      "input": "Suche Finanzierung in 3 Monaten, 500k Euro, 100k Eigenkapital, Angestellter mit 5k netto",
      "expected_output": "A-LEAD",
      "description": "Kurzes Zeitfenster, ausreichend EK, gutes Einkommen"
    },
    {
      "input": "Kaufe Haus in 2 Monaten, 400k Finanzierung, 80k EK, stabiles Einkommen 4.5k",
      "expected_output": "A-LEAD", 
      "description": "Alle A-Kriterien erfüllt"
    }
  ],
  
  "partial_data": [
    {
      "input": "Möchte in 8 Monaten kaufen, 400k Euro, unsicheres Einkommen",
      "expected_output": "B-LEAD",
      "description": "EK fehlt, Einkommen unsicher = B-Lead"
    }
  ],
  
  "edge_cases": [
    {
      "input": "Student, kein Einkommen, erbe aber 300k in 6 Monaten",
      "expected_output": "C-LEAD",
      "description": "Ungewöhnliche Finanzlage - konservativ bewerten"
    }
  ]
}
```

### Phase 2: Expected Output Definition

#### Output-Spezifikation
```yaml
classification_outputs:
  format: "exact_string_match"
  valid_values: ["A-LEAD", "B-LEAD", "C-LEAD"]
  case_sensitivity: false
  additional_text: forbidden
  fallback_default: "B-LEAD"
  
content_generation_outputs:
  format: "structured_text"
  personalization_fields: ["{{contact.first_name}}", "{{contact.last_name}}"]
  length_limits:
    email: "50-300 words"
    sms: "max 160 characters"
  language: "German (formal Sie)"
  compliance: ["datenschutz", "impressum", "opt_out"]
```

### Phase 3: Edge Case Testing

#### Systematische Edge Case Kategorien
1. **Daten-Qualität**
   - Leere Felder
   - Null-Werte 
   - Extrem lange/kurze Eingaben
   - Sonderzeichen und Umlaute

2. **Business-Logik**
   - Grenzwerte (genau an Schwellen)
   - Widersprüchliche Informationen
   - Unlogische Kombinationen

3. **Sprach-Variation**
   - Dialekte und regionale Ausdrücke
   - Englische Begriffe in deutschen Texten
   - Fachbegriffe vs. Laien-Sprache

4. **Timing und Kontext**
   - Veraltete Informationen
   - Saisonale Besonderheiten
   - Feiertage und Wochenenden

### Phase 4: Performance Validation

#### Konsistenz-Tests
```python
# Pseudo-Code für Konsistenz-Testing
for test_case in test_dataset:
    results = []
    for iteration in range(10):  # 10x gleichen Input testen
        output = automation_prompt(test_case.input)
        results.append(output)
    
    consistency_rate = len(set(results)) == 1  # Alle Outputs identisch?
    assert consistency_rate, f"Inkonsistente Outputs für: {test_case.input}"
```

#### Performance Metriken
- **Accuracy**: Prozent korrekter Klassifikationen
- **Consistency**: Identische Outputs bei wiederholten Tests
- **Coverage**: Alle Edge Cases abgedeckt
- **Response Time**: Durchschnittliche Verarbeitungszeit

## Validation Checklist

### Pre-Deployment Checklist
```markdown
- [ ] Mindestens 15 Test-Cases definiert (3 perfect, 3 partial, 4 edge, 2 invalid, 2 multilingual)
- [ ] Output format exakt spezifiziert und validiert
- [ ] Alle Edge Cases identifiziert und getestet
- [ ] Fallback-Verhalten für jede Fehlerklasse definiert
- [ ] Consistency bei 10x Wiederholung ≥95%
- [ ] German language processing korrekt
- [ ] CRM integration variables funktionsfähig
- [ ] Business stakeholder approval erhalten
- [ ] Documentation vollständig und aktuell
- [ ] Rollback-Plan für Production-Issues definiert
```

### Post-Deployment Monitoring
```markdown
- [ ] Real-world accuracy tracking eingerichtet
- [ ] Fehler-Logging und -Analyse aktiv
- [ ] Performance monitoring (Latenz, Throughput)
- [ ] User feedback collection mechanism
- [ ] Automatic alerts für accuracy drops
- [ ] Regular review cycles geplant (weekly/monthly)
```

## Test Automation Framework

### Automated Test Structure
```yaml
automation_test_suite:
  test_files: 
    - "tests/classification_tests.json"
    - "tests/content_generation_tests.json"
    - "tests/edge_case_scenarios.json"
    
  validation_scripts:
    - "validate_output_format.py"
    - "check_consistency.py" 
    - "measure_performance.py"
    
  reporting:
    format: "markdown_summary"
    metrics: ["accuracy", "consistency", "coverage", "performance"]
    stakeholder_distribution: ["dev_team", "business_owners"]
```

### Continuous Testing Pipeline
1. **Code Change**: Automation prompt wird modifiziert
2. **Automated Testing**: Vollständige Test-Suite läuft automatisch
3. **Validation Report**: Ergebnisse werden zusammengefasst
4. **Approval Gate**: Manual review bei kritischen Änderungen
5. **Staged Rollout**: Schrittweise Einführung mit Monitoring

## Integration Testing

### CRM System Integration
```yaml
integration_test_scenarios:
  gohighlevel_workflow:
    trigger: "form_submission"
    input_mapping: "form_fields -> prompt_variables"
    output_processing: "classification_result -> workflow_branch"
    validation: "correct tag assignment in CRM"
    
  leadconnector_conversation:
    trigger: "chat_message"
    input_mapping: "message_content + contact_data -> prompt"
    output_processing: "generated_response -> chat_interface"
    validation: "proper merge field substitution"
```

### End-to-End Testing
1. **Trigger Event**: Simuliere echten User-Input
2. **Automation Execution**: Prompt wird ausgeführt
3. **CRM Action**: Ergebnis wird in System verarbeitet  
4. **User Experience**: Finale User-Interaction testen
5. **Data Validation**: Korrekte Datenerfassung prüfen

## Troubleshooting Guide

### Häufige Probleme und Lösungen

#### Problem: Inkonsistente Outputs
**Symptome**: Gleicher Input führt zu verschiedenen Ergebnissen
**Debugging**:
```markdown
1. Prompt auf nicht-deterministische Elemente prüfen
2. Temperature/Randomness Settings überprüfen 
3. Input preprocessing auf Variabilität testen
4. Prompt complexity reduzieren wenn nötig
```

#### Problem: Unerwartete Classifications
**Symptome**: Business-logisch falsche Kategorisierungen
**Debugging**:
```markdown
1. Test-Beispiele gegen Business-Regeln validieren
2. Grenzwert-Definitionen schärfen
3. Additional training examples hinzufügen
4. Stakeholder feedback für edge cases einholen
```

#### Problem: Integration-Fehler  
**Symptome**: Automation läuft, aber CRM-Integration fehlschlägt
**Debugging**:
```markdown
1. Output-Format gegen Integration-Spec prüfen
2. Merge field syntax und verfügbarkeit validieren
3. Workflow-Konfiguration in CRM überprüfen
4. API logs und error messages analysieren
```

#### Problem: Performance Issues
**Symptome**: Langsame Response times oder Timeouts
**Debugging**:
```markdown
1. Prompt length und complexity optimieren
2. Input processing efficiency verbessern  
3. Caching für häufige Anfragen implementieren
4. Load balancing und scaling prüfen
```

## Quality Gates

### Minimum Quality Thresholds
```yaml
quality_thresholds:
  accuracy_rate: ">= 95%"
  consistency_rate: ">= 98%" 
  edge_case_coverage: ">= 90%"
  response_time: "< 2 seconds"
  german_language_handling: ">= 99%"
  
deployment_gates:
  development: "basic functionality verified"
  staging: "all quality thresholds met"
  production: "business stakeholder approval + 48h staging validation"
```

### Review and Approval Process
1. **Technical Review**: Code quality, test coverage, documentation
2. **Business Review**: Accuracy, business logic, compliance
3. **Stakeholder Approval**: Final sign-off from business owners
4. **Gradual Rollout**: 10% -> 50% -> 100% with monitoring
5. **Post-Deployment Review**: 7-day performance analysis

---

**Remember**: Automation prompts directly impact customer experience and business outcomes. Rigorous testing isn't optional - it's essential for maintaining trust and operational efficiency.