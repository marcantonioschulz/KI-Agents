# Classification Automation Template

## Metadata
```yaml
template_type: "classification"
version: "1.0"
purpose: "Standardized template for classification automation prompts"
output_format: "Single classification token"
integration_platforms: ["GoHighLevel", "LeadConnector", "Custom Workflows"]
```

## Template Structure

### Aufgabe
[Beschreibung der Klassifikations-Aufgabe - was soll klassifiziert werden?]

### Klassifikationskriterien

#### [KATEGORIE-1] - [Beschreibung]
- **Kriterium 1**: [Details und Schwellenwerte]
- **Kriterium 2**: [Details und Schwellenwerte]
- **Kriterium 3**: [Details und Schwellenwerte]
- **Beispiele**: [Konkrete Beispiele für diese Kategorie]

#### [KATEGORIE-2] - [Beschreibung] 
- **Kriterium 1**: [Details und Schwellenwerte]
- **Kriterium 2**: [Details und Schwellenwerte]
- **Kriterium 3**: [Details und Schwellenwerte]
- **Beispiele**: [Konkrete Beispiele für diese Kategorie]

#### [KATEGORIE-3] - [Beschreibung]
- **Kriterium 1**: [Details und Schwellenwerte]
- **Kriterium 2**: [Details und Schwellenwerte]
- **Kriterium 3**: [Details und Schwellenwerte]
- **Beispiele**: [Konkrete Beispiele für diese Kategorie]

### Input-Format  
```
Erwartete Datenstruktur:
- [Feld 1]: [Beschreibung und Format]
- [Feld 2]: [Beschreibung und Format]
- [Feld 3]: [Beschreibung und Format]
```

### Output-Format
**WICHTIG: Antworte NUR mit einem der folgenden Werte:**

```
[OPTION-1]
[OPTION-2] 
[OPTION-3]
```

**Keine zusätzlichen Erklärungen, Texte oder Formatierungen!**

### Fallback-Handling
```
Bei unvollständigen Daten: [DEFAULT-OPTION]
Bei unklaren Informationen: [DEFAULT-OPTION]  
Bei Parsing-Fehlern: [SAFE-FALLBACK-OPTION]
```

### Entscheidungslogik
1. **Schritt 1**: [Erste Bewertungsebene]
2. **Schritt 2**: [Zweite Bewertungsebene]  
3. **Schritt 3**: [Finale Klassifikation]
4. **Output**: Exakt einen der definierten Werte ausgeben

### Test-Beispiele

#### Beispiel 1: [KATEGORIE-1]
**Input:** 
```
[Beispiel-Input für Kategorie 1]
```
**Expected Output:** `[OPTION-1]`

#### Beispiel 2: [KATEGORIE-2]  
**Input:**
```
[Beispiel-Input für Kategorie 2]
```
**Expected Output:** `[OPTION-2]`

#### Beispiel 3: [KATEGORIE-3]
**Input:**
```
[Beispiel-Input für Kategorie 3]
```
**Expected Output:** `[OPTION-3]`

#### Edge Case: Unvollständige Daten
**Input:**
```
[Beispiel mit fehlenden Informationen]
```
**Expected Output:** `[FALLBACK-OPTION]`

### Validation Schema
```json
{
  "valid_outputs": ["[OPTION-1]", "[OPTION-2]", "[OPTION-3]"],
  "format": "exact_string_match",
  "case_sensitive": false,
  "fallback_default": "[DEFAULT-OPTION]"
}
```

### Integration Instructions

#### GoHighLevel Workflow
1. **Trigger**: [Beschreibung des Auslösers]
2. **Input Mapping**: [Wie Daten an Prompt weitergegeben werden]
3. **Output Processing**: [Wie Classification-Result verwendet wird]
4. **IF-ELSE Logic**: 
   ```
   IF output = "[OPTION-1]" THEN [Aktion 1]
   IF output = "[OPTION-2]" THEN [Aktion 2]  
   IF output = "[OPTION-3]" THEN [Aktion 3]
   ```

#### LeadConnector Integration
- **Conversation AI**: V3-Struktur beachten
- **Merge Fields**: `{{contact.*}}` für Input-Daten nutzen
- **Workflow Actions**: Basierend auf Classification-Output

### Troubleshooting

**Problem**: Inkonsistente Outputs
**Lösung**: Validierung der Input-Daten und Fallback-Logik prüfen

**Problem**: Unerwartete Classifications  
**Lösung**: Test-Beispiele erweitern und Kriterien schärfen

**Problem**: Integration-Fehler
**Lösung**: Output-Format und Validation Schema überprüfen

---

**Usage Instructions**: 
1. Kopiere dieses Template
2. Ersetze alle [PLACEHOLDER] mit spezifischen Werten
3. Füge mindestens 5 Test-Beispiele hinzu
4. Validiere mit realen Daten vor Deployment
5. Dokumentiere alle Änderungen im Changelog