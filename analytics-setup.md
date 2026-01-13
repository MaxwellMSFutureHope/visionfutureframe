# Analytics Setup für Vision Future Frame

## Empfohlene Lösung: Plausible Analytics

Plausible ist DSGVO-konform, benötigt keine Cookie-Banner und ist datenschutzfreundlich.

### Setup-Schritte:

1. **Account erstellen** auf https://plausible.io
2. **Domain hinzufügen**: visionfutureframe.de
3. **Script in index.html aktivieren**:
   - Entferne die Kommentare um das Plausible-Script
   - Ersetze `data-domain="visionfutureframe.de"` mit deiner Domain

### Code (bereits vorbereitet in index.html):
```html
<script defer data-domain="visionfutureframe.de" src="https://plausible.io/js/script.js"></script>
```

---

## Alternative: Google Analytics 4

Falls du Google Analytics verwenden möchtest (benötigt Cookie-Banner):

1. **GA4 Property erstellen** in Google Analytics
2. **Measurement ID** kopieren (Format: G-XXXXXXXXXX)
3. **Script in index.html aktivieren**:
   - Entferne die Kommentare um das GA4-Script
   - Ersetze `G-XXXXXXXXXX` mit deiner Measurement ID
4. **Cookie-Banner hinzufügen** (z.B. mit Cookiebot oder OneTrust)

### Wichtig für DSGVO:
- IP-Anonymisierung aktiviert (bereits im Code)
- Cookie-Banner für Einwilligung erforderlich
- Datenschutzerklärung aktualisieren

---

## Performance Monitoring

### Optionen:
- **Google PageSpeed Insights**: https://pagespeed.web.dev/
- **WebPageTest**: https://www.webpagetest.org/
- **Lighthouse** (Chrome DevTools)

### Error Tracking:
- **Sentry** (empfohlen für Production)
- **LogRocket** (Session Replay)
- **Rollbar** (Error Tracking)

---

## Empfehlung

Für eine Public-Interest-Organisation wie VFF ist **Plausible Analytics** die beste Wahl:
- ✅ DSGVO-konform ohne Cookie-Banner
- ✅ Datenschutzfreundlich
- ✅ Open Source
- ✅ Transparent
- ✅ Günstig (ab 9€/Monat)
