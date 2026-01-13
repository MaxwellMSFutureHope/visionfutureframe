# Deployment-Anleitung für GitHub Pages

## 📤 Dateien hochladen

### Option 1: GitHub Web Interface

1. Gehe zu https://github.com/MaxwellMSFutureHope/visionfutureframe
2. Klicke auf "Add file" → "Upload files"
3. Ziehe alle folgenden Dateien in den Browser:

**Wichtige Dateien (müssen hochgeladen werden):**
- ✅ `index.html` (aktualisiert)
- ✅ `impressum.html` (neu)
- ✅ `datenschutz.html` (neu)
- ✅ `logo.svg` (neu)
- ✅ `manifest.json` (neu)
- ✅ `sw.js` (neu)
- ✅ `robots.txt` (neu)
- ✅ `sitemap.xml` (neu)
- ✅ `CNAME` (bereits vorhanden, prüfen ob aktualisiert)
- ✅ `README.md` (aktualisiert)
- ✅ `.htaccess` (neu - funktioniert nur auf Apache-Servern)
- ✅ `analytics-setup.md` (neu)
- ✅ `SETUP.md` (neu)
- ✅ `favicon-generator.html` (neu)
- ✅ `og-image-generator.html` (neu)

**Hinweis:** `.htaccess` funktioniert nicht auf GitHub Pages (nur Apache). Für GitHub Pages ist das nicht nötig.

### Option 2: Git Command Line

```bash
# Repository klonen (falls noch nicht geschehen)
git clone https://github.com/MaxwellMSFutureHope/visionfutureframe.git
cd visionfutureframe

# Alle Dateien hinzufügen
git add .

# Commit erstellen
git commit -m "Update: Vollständige Website mit allen Features"

# Hochladen
git push origin main
```

## 🔧 GitHub Pages aktivieren

1. Gehe zu Repository → **Settings**
2. Scrolle zu **Pages**
3. Unter **Source** wähle: **Deploy from a branch**
4. Branch: **main**
5. Folder: **/ (root)**
6. Klicke **Save**

## 🌐 Custom Domain einrichten

1. Die `CNAME` Datei ist bereits vorhanden mit `visionfutureframe.de`
2. In GitHub Repository Settings → Pages:
   - Trage `visionfutureframe.de` in das Custom Domain Feld ein
3. DNS-Einstellungen bei deinem Domain-Provider:
   - **Typ:** CNAME
   - **Name:** @ (oder www)
   - **Wert:** `maxwellmsfuturehope.github.io`

## ⚠️ Wichtige Hinweise

### GitHub Pages Limitations:
- ❌ `.htaccess` wird **nicht** ausgeführt (nur Apache)
- ✅ Service Worker funktioniert
- ✅ PWA funktioniert
- ✅ HTTPS ist automatisch aktiv

### Nach dem Upload:
1. **Favicons generieren:**
   - Öffne `favicon-generator.html` lokal
   - Lade alle 4 Favicons herunter
   - Lade sie auf GitHub hoch

2. **OG-Image generieren:**
   - Öffne `og-image-generator.html` lokal
   - Lade `og-image.png` herunter
   - Lade es auf GitHub hoch

3. **Service Worker testen:**
   - Öffne https://visionfutureframe.de
   - Chrome DevTools → Application → Service Workers
   - Prüfe ob Service Worker registriert ist

4. **Analytics aktivieren:**
   - Siehe `analytics-setup.md`
   - Entferne Kommentare in `index.html`

## ✅ Checkliste nach Deployment

- [ ] Website läuft auf https://visionfutureframe.de
- [ ] Impressum erreichbar: `/impressum.html`
- [ ] Datenschutz erreichbar: `/datenschutz.html`
- [ ] Service Worker registriert
- [ ] PWA installierbar
- [ ] Mobile Responsive getestet
- [ ] Open Graph Image funktioniert (Facebook Debugger)
- [ ] Favicons sichtbar im Browser-Tab
- [ ] Analytics aktiviert (falls gewünscht)

## 🔍 Testing

### Performance:
- https://pagespeed.web.dev/
- https://www.webpagetest.org/

### SEO:
- https://search.google.com/test/rich-results
- https://developers.facebook.com/tools/debug/

### PWA:
- Chrome DevTools → Lighthouse → PWA Audit

---

**Bei Problemen:** Siehe `SETUP.md` oder kontaktiere marcel.smarsch@visionfutureframe.de
