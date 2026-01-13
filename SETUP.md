# Vision Future Frame - Setup-Anleitung

## ✅ Abgeschlossene Aufgaben

### Rechtliche Seiten
- ✅ **Impressum** (`impressum.html`) - DSGVO-konform
- ✅ **Datenschutzerklärung** (`datenschutz.html`) - Vollständig DSGVO-konform
- ⏳ AGB (optional, bei Bedarf)

### Visuelle Assets
- ✅ **Logo** (`logo.svg`) - Als separate SVG-Datei
- ✅ **Favicon-Generator** (`favicon-generator.html`) - Generiert alle benötigten Größen
- ✅ **Open Graph Image Generator** (`og-image-generator.html`) - Für Social Media

### Technische Optimierungen
- ✅ **.htaccess** - Performance, Security, Caching
- ✅ **Service Worker** (`sw.js`) - PWA-Funktionalität
- ✅ **Manifest.json** - PWA-Manifest
- ✅ **Analytics-Vorbereitung** - Plausible & GA4 Code vorbereitet

## 📋 Nächste Schritte

### 1. Favicons generieren
1. Öffne `favicon-generator.html` im Browser
2. Lade alle 4 Favicon-Größen herunter:
   - `favicon-16x16.png`
   - `favicon-32x32.png`
   - `favicon-192x192.png`
   - `favicon-512x512.png`
3. Speichere sie im Root-Verzeichnis der Website

### 2. Open Graph Image generieren
1. Öffne `og-image-generator.html` im Browser
2. Klicke auf "Download og-image.png"
3. Speichere als `og-image.png` im Root-Verzeichnis

### 3. Analytics einrichten
1. Lies `analytics-setup.md` für Details
2. **Empfehlung**: Plausible Analytics (DSGVO-konform, kein Cookie-Banner)
3. Entferne die Kommentare um das Analytics-Script in `index.html`

### 4. Deployment-Checkliste

#### Vor dem Upload:
- [ ] Alle Favicon-Dateien hochgeladen
- [ ] `og-image.png` hochgeladen
- [ ] Analytics aktiviert (falls gewünscht)
- [ ] Service Worker getestet
- [ ] SSL-Zertifikat aktiviert (HTTPS)

#### Nach dem Upload:
- [ ] Website funktioniert auf https://visionfutureframe.de
- [ ] Impressum & Datenschutz erreichbar
- [ ] Service Worker registriert (in Browser DevTools prüfen)
- [ ] PWA installierbar (Chrome: Menü → "App installieren")
- [ ] Open Graph Image funktioniert (Facebook Debugger testen)
- [ ] Mobile Responsive Design getestet
- [ ] Performance getestet (PageSpeed Insights)

## 🚀 Deployment

### GitHub Pages
1. Repository erstellen
2. Dateien hochladen
3. GitHub Pages aktivieren
4. Custom Domain einrichten (CNAME-Datei vorhanden)

### Alternative Hosting-Optionen:
- **Netlify** - Automatisches Deployment, kostenlos
- **Vercel** - Schnell, kostenlos
- **Cloudflare Pages** - CDN inklusive
- **Eigener Server** - Apache/Nginx mit .htaccess

## 📁 Dateistruktur

```
VFF internetseite/
├── index.html              # Hauptseite
├── impressum.html          # Impressum
├── datenschutz.html       # Datenschutzerklärung
├── logo.svg               # Logo als SVG
├── favicon-*.png          # Favicons (zu generieren)
├── og-image.png           # Social Media Bild (zu generieren)
├── manifest.json          # PWA Manifest
├── sw.js                  # Service Worker
├── .htaccess              # Apache Konfiguration
├── robots.txt             # SEO
├── sitemap.xml            # SEO
├── CNAME                  # Custom Domain
├── README.md              # Projektbeschreibung
├── SETUP.md               # Diese Datei
├── analytics-setup.md     # Analytics Anleitung
├── favicon-generator.html # Favicon Generator
└── og-image-generator.html # OG Image Generator
```

## 🔧 Wartung

### Regelmäßige Updates:
- Sitemap-Datum aktualisieren (`sitemap.xml`)
- Service Worker Cache-Version erhöhen (`sw.js` - CACHE_NAME)
- Analytics-Daten prüfen
- Performance-Monitoring

### Content-Updates:
- Neue Projekte hinzufügen
- Status-Updates (z.B. "Im Aufbau" entfernen)
- Kontaktdaten aktualisieren

## 📞 Support

Bei Fragen oder Problemen:
- E-Mail: marcel.smarsch@visionfutureframe.de
- Website: https://visionfutureframe.de

---

**Stand:** Januar 2025  
**Version:** 1.0
