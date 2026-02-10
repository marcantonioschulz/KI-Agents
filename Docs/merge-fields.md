# Merge Fields Reference

Diese Datei listet alle relevanten Merge Fields für die OSM Mail-Templates auf, inklusive GoHighLevel-Standardfelder und projektbezogener Custom Fields. Felder werden ohne Leerzeichen in den Klammern dargestellt.

## Was sind Merge Fields?

Merge Fields ermöglichen die dynamische Personalisierung von E-Mails, SMS, Webseiten, Workflows und Dokumenten. Sie werden automatisch mit den jeweiligen Daten aus dem CRM, Kalender, Kampagnen, Rechnungen usw. ersetzt.

## Hinweise zur Nutzung

- Felder immer ohne Leerzeichen in den Klammern verwenden: z.B. `{{contact.first_name}}`
- Für internationale Telefonnummern nutze die Raw-Formate (z.B. `{{contact.phone_raw}}`).
- Für Fallback-Werte nutze GoHighLevel-Workflows (siehe unten).

## Standard GoHighLevel Merge Fields

### CONTACT

- `{{contact.name}}` – Vollständiger Name
- `{{contact.first_name}}` – Vorname
- `{{contact.last_name}}` – Nachname
- `{{contact.email}}` – E-Mail-Adresse
- `{{contact.phone}}` – Telefonnummer
- `{{contact.phone_raw}}` – Telefonnummer (ohne Formatierung)
- `{{contact.company_name}}` – Firmenname
- `{{contact.full_address}}` – Vollständige Adresse
- `{{contact.address1}}` – Adresse Zeile 1
- `{{contact.address_line2}}` – Adresse Zeile 2
- `{{contact.city}}` – Stadt
- `{{contact.state}}` – Bundesland
- `{{contact.country}}` – Land
- `{{contact.postal_code}}` – Postleitzahl
- `{{contact.timezone}}` – Zeitzone
- `{{contact.date_of_birth}}` – Geburtsdatum
- `{{contact.source}}` – Quelle
- `{{contact.website}}` – Webseite
- `{{contact.id}}` – Kontakt-ID
- Attribution: `{{contact.attributionSource.sessionSource}}`, `{{contact.attributionSource.url}}`, ...
- Latest Attribution: `{{contact.lastAttributionSource.sessionSource}}`, ...

### USER

- `{{user.name}}` – Name des Benutzers
- `{{user.first_name}}` – Vorname
- `{{user.last_name}}` – Nachname
- `{{user.email}}` – E-Mail
- `{{user.phone}}` – Telefonnummer
- `{{user.phone_raw}}` – Telefonnummer (roh)
- `{{user.email_signature}}` – E-Mail-Signatur
- `{{user.calendar_link}}` – Kalender-Link
- `{{user.twilio_phone_number}}` – Twilio Nummer
- `{{user.twilio_phone_number_raw}}` – Twilio Nummer (roh)

### APPOINTMENT

**Basis-Informationen:**
- `{{appointment.title}}` – Termin-Titel
- `{{appointment.status}}` – Status
- `{{appointment.notes}}` – Notizen
- `{{appointment.meeting_location}}` – Treffpunkt

**Zeitangaben:**
- `{{appointment.start_time}}` – Startzeit (vollständig)
- `{{appointment.end_time}}` – Endzeit (vollständig)
- `{{appointment.only_start_date}}` – Nur Startdatum
- `{{appointment.only_start_time}}` – Nur Startzeit
- `{{appointment.only_end_date}}` – Nur Enddatum
- `{{appointment.only_end_time}}` – Nur Endzeit

**Datum-Details:**
- `{{appointment.day}}` – Tag
- `{{appointment.day_of_week}}` – Wochentag
- `{{appointment.month}}` – Monat
- `{{appointment.month_name}}` – Monatsname
- `{{appointment.year}}` – Jahr
- `{{appointment.timezone}}` – Zeitzone

**Kalender-Links:**
- `{{appointment.add_to_google_calendar}}` – Google Kalender Link
- `{{appointment.add_to_ical_outlook}}` – iCal/Outlook Link

**Termin-Management:**
- `{{appointment.cancellation_link}}` – Link zur Terminabsage
- `{{appointment.reschedule_link}}` – Link zur Terminverschiebung

**Wiederholende Termine:**
- `{{appointment.recurring.repeats}}` – Wiederholungstyp
- `{{appointment.recurring.frequency}}` – Frequenz
- `{{appointment.recurring.interval}}` – Intervall

**Zugewiesener Benutzer:**
- `{{appointment.user.name}}` – Name
- `{{appointment.user.first_name}}` – Vorname
- `{{appointment.user.last_name}}` – Nachname
- `{{appointment.user.email}}` – E-Mail
- `{{appointment.user.phone}}` – Telefon

### CALENDAR

- `{{calendar.name}}` – Kalendername

### CAMPAIGN

- `{{campaign.event_date_time}}` – Event, Datum, Uhrzeit
- `{{campaign.event_date}}` – Event Datum
- `{{campaign.event_time}}` – Event Uhrzeit

### MESSAGE

- `{{message.body}}` – Nachrichteninhalt
- `{{message.subject}}` – Betreff

### ACCOUNT/LOCATION

**Basis-Informationen:**
- `{{location.name}}` – Standortname
- `{{location.id}}` – Standort-ID
- `{{location.email}}` – E-Mail
- `{{location.phone}}` – Telefonnummer
- `{{location.phone_raw}}` – Telefonnummer (roh)
- `{{location.website}}` – Webseite
- `{{location.logo_url}}` – Logo URL

**Adresse:**
- `{{location.full_address}}` – Vollständige Adresse
- `{{location.address}}` – Adresse Zeile 1
- `{{location.address_line2}}` – Adresse Zeile 2
- `{{location.city}}` – Stadt
- `{{location.state}}` – Bundesland
- `{{location.country}}` – Land
- `{{location.postal_code}}` – PLZ

**Owner/Inhaber:**
- `{{location_owner.name}}` – Vollständiger Name
- `{{location_owner.first_name}}` – Vorname
- `{{location_owner.last_name}}` – Nachname
- `{{location_owner.email}}` – E-Mail
- `{{location_owner.phone}}` – Telefon

### RIGHT NOW

**Zeit:**
- `{{right_now.second}}` – Sekunde (0-59)
- `{{right_now.minute}}` – Minute (0-59)
- `{{right_now.hour}}` – Stunde (0-23, 24h-Format)
- `{{right_now.hour_ampm}}` – Stunde (1-12, AM/PM-Format)
- `{{right_now.ampm}}` – AM oder PM

**Datum:**
- `{{right_now.day}}` – Tag (1-31)
- `{{right_now.day_of_month}}` – Tag im Monat (1-31)
- `{{right_now.day_of_week}}` – Wochentag (z.B. "Montag", "Dienstag")
- `{{right_now.day_of_week_abbr}}` – Wochentag abgekürzt (z.B. "Mo", "Di")
- `{{right_now.month}}` – Monat (1-12)
- `{{right_now.month_name}}` – Monatsname (z.B. "Januar", "Februar")
- `{{right_now.month_abbr}}` – Monat abgekürzt (z.B. "Jan", "Feb")
- `{{right_now.year}}` – Jahr (z.B. "2025")
- `{{right_now.year_short}}` – Jahr zweistellig (z.B. "25")

**Weitere:**
- `{{right_now.timezone}}` – Zeitzone (z.B. "Europe/Berlin")
- `{{right_now.unix_timestamp}}` – Unix-Timestamp

### ATTRIBUTION

**Erste Attribution (First Touch):**
- `{{contact.attributionSource.sessionSource}}` – Session-Quelle
- `{{contact.attributionSource.url}}` – URL
- `{{contact.attributionSource.utmSource}}` – UTM Source
- `{{contact.attributionSource.utmMedium}}` – UTM Medium
- `{{contact.attributionSource.utmCampaign}}` – UTM Campaign
- `{{contact.attributionSource.utmTerm}}` – UTM Term
- `{{contact.attributionSource.utmContent}}` – UTM Content
- `{{contact.attributionSource.referrer}}` – Referrer
- `{{contact.attributionSource.fbclid}}` – Facebook Click ID
- `{{contact.attributionSource.gclid}}` – Google Click ID
- `{{contact.attributionSource.msclkid}}` – Microsoft Click ID

**Letzte Attribution (Last Touch):**
- `{{contact.lastAttributionSource.sessionSource}}` – Session-Quelle
- `{{contact.lastAttributionSource.url}}` – URL
- `{{contact.lastAttributionSource.utmSource}}` – UTM Source
- `{{contact.lastAttributionSource.utmMedium}}` – UTM Medium
- `{{contact.lastAttributionSource.utmCampaign}}` – UTM Campaign
- `{{contact.lastAttributionSource.utmTerm}}` – UTM Term
- `{{contact.lastAttributionSource.utmContent}}` – UTM Content
- `{{contact.lastAttributionSource.referrer}}` – Referrer
- `{{contact.lastAttributionSource.fbclid}}` – Facebook Click ID
- `{{contact.lastAttributionSource.gclid}}` – Google Click ID
- `{{contact.lastAttributionSource.msclkid}}` – Microsoft Click ID

### COURSE

**Kurs-Informationen:**
- `{{course.name}}` – Kursname
- `{{course.description}}` – Beschreibung
- `{{course.url}}` – Kurs-URL
- `{{course.image}}` – Kursbild-URL

**Produkt-Details:**
- `{{course.product.name}}` – Produktname
- `{{course.product.description}}` – Produktbeschreibung
- `{{course.product.image}}` – Produktbild

**Fortschritt:**
- `{{course.progress.percentage}}` – Fortschritt in %
- `{{course.progress.completed_lessons}}` – Abgeschlossene Lektionen
- `{{course.progress.total_lessons}}` – Gesamtzahl Lektionen

### INVOICE

**Rechnungs-Informationen:**
- `{{invoice.name}}` – Rechnungsname
- `{{invoice.number}}` – Rechnungsnummer
- `{{invoice.title}}` – Titel
- `{{invoice.issue_date}}` – Ausstellungsdatum
- `{{invoice.due_date}}` – Fälligkeitsdatum
- `{{invoice.status}}` – Status
- `{{invoice.currency}}` – Währung

**Beträge:**
- `{{invoice.total_amount}}` – Gesamtbetrag
- `{{invoice.sub_total}}` – Zwischensumme
- `{{invoice.discount}}` – Rabatt
- `{{invoice.tax}}` – Steuer
- `{{invoice.amount_paid}}` – Bezahlter Betrag
- `{{invoice.amount_due}}` – Offener Betrag

**Unternehmen:**
- `{{invoice.company.name}}` – Firmenname
- `{{invoice.company.address}}` – Adresse
- `{{invoice.company.city}}` – Stadt
- `{{invoice.company.state}}` – Bundesland
- `{{invoice.company.country}}` – Land
- `{{invoice.company.postal_code}}` – PLZ
- `{{invoice.company.phone}}` – Telefon
- `{{invoice.company.email}}` – E-Mail
- `{{invoice.company.website}}` – Webseite

**Kunde:**
- `{{invoice.customer.name}}` – Name
- `{{invoice.customer.email}}` – E-Mail
- `{{invoice.customer.phone}}` – Telefon
- `{{invoice.customer.address}}` – Adresse

**Absender:**
- `{{invoice.sender.name}}` – Name
- `{{invoice.sender.email}}` – E-Mail
- `{{invoice.sender.phone}}` – Telefon

**Zahlungskarte:**
- `{{invoice.card.brand}}` – Kartentyp (Visa, Mastercard, etc.)
- `{{invoice.card.last4}}` – Letzte 4 Ziffern
- `{{invoice.card.exp_month}}` – Ablaufmonat
- `{{invoice.card.exp_year}}` – Ablaufjahr

**Links:**
- `{{invoice.live_payment_link}}` – Zahlungslink
- `{{invoice.alt_payment_link}}` – Alternativer Zahlungslink

## Custom Fields (Projektbezogen)

### Formular Felder

- `{{contact.kaufpreis}}` – Kaufpreis
- `{{contact.haushaltsnetto_in_zahlen}}` – Haushaltsnetto in Zahlen
- `{{contact.eigenkapital}}` – Eigenkapital
- `{{contact.zeitraum}}` – Zeitraum
- `{{contact.schufa}}` – Schufa
- `{{contact.your_message}}` – Nachricht
- `{{contact.finanzierungsart}}` – Finanzierungsart
- `{{contact.aktuelle_miete}}` – Aktuelle Miete
- `{{contact.arbeitsverhltnis}}` – Arbeitsverhältnis
- `{{contact.immobilie_im_blick}}` – Immobilie im Blick
- `{{contact.wunschrate}}` – Wunschrate
- `{{contact.was_ist_aktuell_das_grte_hindernis_auf_dem_weg_ins_eigenheim}}` – Aktuelles Hindernis

### EZH Webseite Erstgespräch

- `{{contact.wofr_interessiert_sie_sich}}` – Interessensgebiet
- `{{contact.wo_stehen_sie_aktuell}}` – Aktuelle Situation
- `{{contact.was_bremst_sie}}` – Bremse
- `{{contact.wann_starten_sie}}` – Startzeitpunkt

### Vertriebler

- `{{contact.was_ist_dein_aktueller_berufsstatus}}` – Berufsstatus
- `{{contact.was_wre_dir_in_einer_neuen_stelle_am_wichtigsten}}` – Wichtigstes in neuer Stelle
- `{{contact.welches_adjektiv_beschreibt_dich_am_besten}}` – Adjektiv
- `{{contact.bist_du_oder_warst_du_in_der_finanzbranche_ttig}}` – Finanzbranche-Erfahrung
- `{{contact.beherrschst_du_die_deutsche_sprache_in_wort_und_schrift}}` – Deutschkenntnisse
- `{{contact.warum_sollten_wir_gerade_dir_die_chance_geben_bei_uns_karriere_zu_machen}}` – Warum du?

### EZH Webseite Karriere

- `{{contact.beruflicher_status}}` – Beruflicher Status
- `{{contact.womit_kennst_du_dich_schon_aus}}` – Kenntnisse
- `{{contact.was_motiviert_dich_am_meisten}}` – Motivation
- `{{contact.hast_du_erfahrung_in}}` – Erfahrung
- `{{contact.was_traust_du_dir_aktuell_zu}}` – Selbsteinschätzung
- `{{contact.warum_sollten_wir_dich_kennenlernen}}` – Warum kennenlernen?

## Beispiel-Usage

```html
<p>Hallo {{contact.first_name}}, Ihr Termin ist am {{appointment.start_time}}.</p>
<a href="{{appointment.cancellation_link}}">Termin absagen</a>
```

## Fallback-Werte mit Workflows

Wenn ein Feld leer ist, kann per Workflow ein Fallback-Wert gesetzt werden:

1. Custom Value in den Einstellungen anlegen (z.B. First_Name_Fallback)
2. Im Workflow If/Else-Bedingung für das Feld prüfen
3. Fallback-Wert im Template nutzen, falls das Feld leer ist

Mehr Infos: <https://help.gohighlevel.com/support/solutions/articles/48001180266>

## Links & Referenzen

- GoHighLevel Merge Fields: <https://help.gohighlevel.com/support/solutions/articles/48001078171-list-of-merge-fields>
- Kontakt-Detail-Link: <https://app.osm.marketing/v2/location/{{location.id}}/contacts/detail/{{contact.id}}>

---
Diese Datei ist die zentrale Referenz für alle Merge Fields im Projekt. Ergänze neue Custom Fields hier und nutze die Felder konsistent in allen Templates.
