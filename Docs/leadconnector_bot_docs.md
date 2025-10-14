# LeadConnector Documentation (Add Contact Info + Merge Fields)

## 📋 Add Contact Info for your Bot
*Stand: 20. Dezember 2024*

### Inhaltsverzeichnis
- Einführung
- Schritt 1: Zugriff auf die Funktion
- Schritt 2: Kontaktinformationen hinzufügen
- Felder einrichten
- Zusätzliche Hinweise

---

### Einführung
Die **Add Contact Info**-Funktion ermöglicht es, Kontaktdaten wie **Name, Telefonnummer, E-Mail** und mehr direkt über die KI zu erfassen oder zu aktualisieren.  
Ziel: Einfachere und präzisere Pflege aktueller Lead-Daten.

**Wichtige Hinweise:**
- Nur **leere Felder** werden aktualisiert.  
- E-Mail und Telefonnummer werden **automatisch** aktualisiert.  
- Wenn du möchtest, dass der Bot aktiv Daten abfragt, **muss** dies im Prompt explizit stehen.  
  > Wenn der Prompt keine Anweisung enthält, fragt der Bot nicht nach den Informationen.

---

### Schritt 1: Zugriff auf die Funktion
1. Öffne den Tab **Bot Goals**.  
2. Klicke auf **Add Contact Info**.  
3. Falls du einen neuen Bot erstellst, vergebe zuerst einen **Namen**, bevor du fortfährst.

---

### Schritt 2: Kontaktinformationen hinzufügen
Nach Klick auf **Add Contact Info** kannst du definieren, welche Felder du aktualisieren möchtest.

#### Felder einrichten:
- **Action Name:** Bezeichnung der Aktion (z. B. „Update Contact’s Date of Birth“).  
- **Select Field:** Wähle das Feld, das aktualisiert werden soll (Name, Firma, Geburtsdatum etc.).  
- **What to Update:** Kurze Beschreibung des Inhalts.  
  - Beispiel:  
    - `Date of Birth → This is the birth date of the contact`  
    - `Business Name → This is the business name of the contact`
- **Output Example (optional):**  
  Beispielwert, z. B. „5th Jan 1990“.  
- Danach auf **Save** klicken.

> 💡 Tipp: Stelle sicher, dass dein Prompt eine passende Frage enthält, sonst kann die Information nicht abgefragt werden.

---

### Zusätzliche Hinweise
Nach dem Speichern sollte der Prompt klare Anweisungen enthalten, z. B.:

```text
### mandatory instruction:
Before booking an appointment, always ask these questions one after another:
1. Ask the customer for their name
2. Ask the customer for their email
3. Ask the customer for their phone
4. Ask the customer for their date of birth
5. Ask the customer for their business name
```

Diese Struktur stellt sicher, dass der Bot alle wichtigen Daten abfragt, bevor z. B. ein Termin gebucht wird.

---

## 💡 Merge Fields for Emails, SMS, and Funnels (LeadConnector)
*Stand: 2. September 2025*

### Zweck
Merge Fields erlauben es, Nachrichten **automatisch zu personalisieren**, indem sie Kontakt-, Benutzer-, Termin- und Kontodaten einfügen.

Anwendungsbeispiele:
- E-Mails & SMS
- Funnels & Webseiten
- Rechnungen & Workflows
- Kampagnen und Automationen

---

### 📇 CONTACT Merge Fields
| Feld | Merge Code |
|------|-------------|
| Full name | `{{contact.name}}` |
| First name | `{{contact.first_name}}` |
| Last name | `{{contact.last_name}}` |
| Email | `{{contact.email}}` |
| Phone | `{{contact.phone}}` |
| Phone (Raw) | `{{contact.phone_raw}}` |
| Company name | `{{contact.company_name}}` |
| Full address | `{{contact.full_address}}` |
| City | `{{contact.city}}` |
| State | `{{contact.state}}` |
| Postal Code | `{{contact.postal_code}}` |
| Time Zone | `{{contact.timezone}}` |
| Date of Birth | `{{contact.date_of_birth}}` |
| Source | `{{contact.source}}` |
| Website | `{{contact.website}}` |

---

### 👤 USER Merge Fields
| Feld | Merge Code |
|------|-------------|
| Full Name | `{{user.name}}` |
| Email | `{{user.email}}` |
| Phone | `{{user.phone}}` |
| Signature | `{{user.email_signature}}` |
| Calendar Link | `{{user.calendar_link}}` |
| Twilio Phone | `{{user.twilio_phone_number}}` |

---

### 📅 APPOINTMENT Merge Fields
| Feld | Merge Code |
|------|-------------|
| Title | `{{appointment.title}}` |
| Start Date/Time | `{{appointment.start_time}}` |
| End Date/Time | `{{appointment.end_time}}` |
| Cancellation Link | `{{appointment.cancellation_link}}` |
| Reschedule Link | `{{appointment.reschedule_link}}` |
| Meeting Location | `{{appointment.meeting_location}}` |
| Assigned User | `{{appointment.user.name}}` |

---

### 🗓️ CALENDAR Merge Fields
| Feld | Merge Code |
|------|-------------|
| Calendar Name | `{{calendar.name}}` |

---

### 📢 CAMPAIGN Merge Fields
| Feld | Merge Code |
|------|-------------|
| Event Date | `{{campaign.event_date}}` |
| Event Time | `{{campaign.event_time}}` |

---

### 💬 MESSAGE Merge Fields
| Feld | Merge Code |
|------|-------------|
| Body | `{{message.body}}` |
| Subject | `{{message.subject}}` |

---

### 🏢 ACCOUNT Merge Fields
| Feld | Merge Code |
|------|-------------|
| Company Name | `{{location.name}}` |
| Email | `{{location.email}}` |
| Phone | `{{location.phone}}` |
| Address | `{{location.address}}` |
| Website | `{{location.website}}` |
| Logo URL | `{{location.logo_url}}` |

---

### 🕒 RIGHT NOW Merge Fields
| Feld | Merge Code |
|------|-------------|
| Time (24h) | `{{right_now.hour}}` |
| Time (AM/PM) | `{{right_now.hour_ampm}}` |
| Day | `{{right_now.day}}` |
| Month | `{{right_now.month}}` |
| Year | `{{right_now.year}}` |

---

### 📈 ATTRIBUTION Merge Fields
| Art | Beispiel |
|------|----------|
| Session Source | `{{contact.attributionSource.sessionSource}}` |
| UTM Source | `{{contact.attributionSource.utmSource}}` |
| UTM Campaign | `{{contact.lastAttributionSource.utmCampaign}}` |
| FB ClickId | `{{contact.attributionSource.fbclid}}` |
| Google ClickId | `{{contact.attributionSource.gclid}}` |

---

### 💳 INVOICE Merge Fields
| Kategorie | Feld | Merge Code |
|------------|-------|------------|
| **Invoice Info** | Name | `{{invoice.name}}` |
|  | Number | `{{invoice.number}}` |
|  | Issue Date | `{{invoice.issue_date}}` |
|  | Due Date | `{{invoice.due_date}}` |
|  | Total | `{{invoice.total_amount}}` |
| **Company** | Name | `{{invoice.company.name}}` |
|  | Address | `{{invoice.company.address}}` |
| **Customer** | Name | `{{invoice.customer.name}}` |
|  | Email | `{{invoice.customer.email}}` |
| **Payment Card** | Brand | `{{invoice.card.brand}}` |
|  | Last 4 Digits | `{{invoice.card.last4}}` |

---

### 🧠 Workflows: Fallback Values
Wenn ein Feld (z. B. `{{contact.first_name}}`) leer ist:
1. Erstelle unter **Settings → Custom Values** einen Platzhalter (z. B. `First_Name_Fallback`).  
2. Füge in deinem Workflow eine **If/Else**-Bedingung hinzu:
   - Wenn leer → nutze `{{custom_values.First_Name_Fallback}}`
   - Wenn gefüllt → nutze das Originalfeld.

Dadurch bleibt Personalisierung konsistent.

---

### 🔗 Weitere Ressourcen
- [Custom Values Settings](https://help.gohighlevel.com/en/support/solutions/articles/155000004705)
- [Merge Fields Overview](https://help.gohighlevel.com/en/support/solutions/articles/155000004390)
- [If/Else Workflows Guide](https://help.gohighlevel.com/en/support/solutions/articles/48001180266)

---

© LeadConnector 2025 — HighLevel Merge Fields & AI Bot Setup Documentation
