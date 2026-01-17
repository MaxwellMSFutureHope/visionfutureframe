# 🚀 IONOS Deployment-Anleitung

## 📋 Übersicht

Diese Anleitung zeigt, wie Sie die aktualisierte Website auf IONOS hochladen.

**Wichtig:** Die Website wird auf IONOS gehostet, nicht auf GitHub Pages. Alle Änderungen müssen manuell per FTP/SFTP oder über den IONOS File Manager hochgeladen werden.

---

## 🔐 Zugangsdaten vorbereiten

Sie benötigen:
- **IONOS Benutzername** (oder E-Mail)
- **IONOS Passwort** (oder FTP-Passwort)
- **FTP-Host** (z.B. `ftp.visionfutureframe.de` oder IP-Adresse)
- **FTP-Port** (meist 21 für FTP, 22 für SFTP)

Diese finden Sie in Ihrem IONOS Kundencenter unter:
- **Hosting & Domains** → **FTP-Zugänge** → **Zugangsdaten anzeigen**

---

## 📤 Option 1: IONOS File Manager (Einfachste Methode)

### Schritt 1: IONOS Kundencenter öffnen
1. Gehen Sie zu: https://www.ionos.de/
2. Loggen Sie sich ein
3. Wählen Sie **Hosting & Domains**

### Schritt 2: File Manager öffnen
1. Klicken Sie auf **File Manager** (oder **Datei-Manager**)
2. Navigieren Sie zum **Root-Verzeichnis** Ihrer Domain (meist `/` oder `/public_html/` oder `/htdocs/`)

### Schritt 3: Dateien hochladen
1. **Alte Dateien sichern** (optional, aber empfohlen):
   - Erstellen Sie einen Ordner `backup_2025-01-27/`
   - Verschieben Sie alle alten HTML-Dateien dorthin

2. **Neue Dateien hochladen:**
   - Klicken Sie auf **Upload** oder **Hochladen**
   - Laden Sie die folgenden Dateien hoch (siehe Liste unten)

3. **Ordnerstruktur erstellen:**
   - Erstellen Sie Ordner `systems/` und `landing/` falls nicht vorhanden
   - Laden Sie die entsprechenden Dateien hoch

---

## 📤 Option 2: FTP/SFTP Client (Für größere Dateimengen)

### Empfohlene FTP-Clients:
- **FileZilla** (kostenlos, Windows/Mac/Linux) - https://filezilla-project.org/
- **WinSCP** (Windows) - https://winscp.net/
- **Cyberduck** (Mac/Windows) - https://cyberduck.io/

### FileZilla Setup:
1. **FileZilla installieren** und öffnen
2. **Datei** → **Verbindung zu Server herstellen**
3. Eingeben:
   - **Host:** `ftp.visionfutureframe.de` (oder IONOS FTP-Host)
   - **Benutzername:** Ihr IONOS FTP-Benutzername
   - **Passwort:** Ihr IONOS FTP-Passwort
   - **Port:** `21` (FTP) oder `22` (SFTP)
4. Klicken Sie auf **Verbinden**

### Dateien hochladen:
1. **Links (lokale Dateien):** Navigieren Sie zu Ihrem Projektordner:
   ```
   C:\Users\Media\Desktop\VIsion Future Frame\VFF internetseite
   ```

2. **Rechts (Remote-Server):** Navigieren Sie zum Root-Verzeichnis:
   - `/` oder `/public_html/` oder `/htdocs/`

3. **Alte Dateien sichern** (empfohlen):
   - Erstellen Sie auf dem Server einen Ordner `backup_2025-01-27/`
   - Verschieben Sie alte Dateien dorthin

4. **Dateien hochladen:**
   - Markieren Sie die Dateien links (lokal)
   - Ziehen Sie sie rechts (Server) in das richtige Verzeichnis
   - Warten Sie, bis der Upload abgeschlossen ist

---

## 📋 Upload-Liste: Alle Dateien für IONOS

### 🔴 WICHTIG - Muss hochgeladen werden:

#### Hauptseiten:
1. ✅ `index.html` - **Hauptseite** (korrigiert, ohne Jobcenter)
2. ✅ `about.html` - Über uns
3. ✅ `contact.html` - Kontakt
4. ✅ `portfolio.html` - Portfolio
5. ✅ `updates.html` - Updates
6. ✅ `proof.html` - Proof
7. ✅ `impressum.html` - Impressum (DSGVO)
8. ✅ `datenschutz.html` - Datenschutz (DSGVO)
9. ✅ `404.html` - 404 Fehlerseite

#### Assets:
10. ✅ `logo.svg` - Logo
11. ✅ `favicon-16x16.png` - Favicon (falls vorhanden)
12. ✅ `favicon-32x32.png` - Favicon (falls vorhanden)
13. ✅ `favicon-192x192.png` - Favicon (falls vorhanden)
14. ✅ `favicon-512x512.png` - Favicon (falls vorhanden)
15. ✅ `og-image.png` - Social Media Bild (falls vorhanden)

#### Technische Dateien:
16. ✅ `manifest.json` - PWA Manifest
17. ✅ `sw.js` - Service Worker
18. ✅ `.htaccess` - **WICHTIG für IONOS!** (Apache-Konfiguration)
19. ✅ `robots.txt` - SEO für Suchmaschinen
20. ✅ `sitemap.xml` - SEO Sitemap

#### Ordnerstruktur:
21. ✅ `systems/` Ordner:
    - `systems/autogovai.html`
    - `systems/dtl.html`
    - `systems/vault.html`

22. ✅ `landing/` Ordner:
    - `landing/auditierbare-ki-behoerden.html`
    - `landing/digitale-verwaltung-prozessautomatisierung.html`
    - `landing/local-first-ki-dokumentenanalyse.html`
    - `landing/policy-as-code-deutschland.html`
    - `landing/verwaltungs-ki-pilotprojekt.html`

### 🟡 OPTIONAL - Dokumentation (nicht für Website nötig):
- `README.md`
- `SETUP.md`
- `DEPLOYMENT.md`
- `IONOS-DEPLOYMENT.md` (diese Datei)
- `analytics-setup.md`
- `favicon-generator.html`
- `og-image-generator.html`

### ❌ NICHT hochladen:
- `.git/` Ordner
- `.github/` Ordner
- `.gitignore`
- `CNAME` (nur für GitHub Pages)

---

## ⚙️ Wichtige Einstellungen nach dem Upload

### 1. Dateiberechtigungen (FTP):
- **HTML-Dateien:** `644` oder `755`
- **Ordner:** `755`
- **JavaScript (.js):** `644` oder `755`
- **.htaccess:** `644` (muss lesbar sein!)

### 2. .htaccess aktivieren (IONOS Apache):
- Die `.htaccess` Datei sollte automatisch funktionieren
- Falls nicht: Prüfen Sie die Dateiberechtigungen
- IONOS unterstützt standardmäßig `.htaccess` auf Apache-Servern

### 3. Cache leeren:
Nach dem Upload sollten Sie:
- **Browser-Cache leeren** (Strg+F5)
- **IONOS Cache prüfen** (falls aktiviert in IONOS Kundencenter)

---

## ✅ Checkliste nach Upload

### Funktionstest:
- [ ] Website läuft: https://visionfutureframe.de
- [ ] Hauptseite zeigt neuen Text (ohne Jobcenter)
- [ ] Impressum erreichbar: `/impressum.html`
- [ ] Datenschutz erreichbar: `/datenschutz.html`
- [ ] Portfolio erreichbar: `/portfolio.html`
- [ ] System-Seiten erreichbar: `/systems/autogovai.html`
- [ ] Landing-Pages erreichbar: `/landing/verwaltungs-ki-pilotprojekt.html`
- [ ] 404-Seite funktioniert (testen mit falscher URL)

### SEO & Performance:
- [ ] `robots.txt` erreichbar: `/robots.txt`
- [ ] `sitemap.xml` erreichbar: `/sitemap.xml`
- [ ] Service Worker funktioniert (DevTools → Application → Service Workers)
- [ ] PWA installierbar (Chrome: Menü → "App installieren")
- [ ] Favicons sichtbar im Browser-Tab
- [ ] Open Graph Image funktioniert (Facebook Debugger)

### Technische Checks:
- [ ] `.htaccess` wird ausgeführt (Performance-Optimierungen aktiv)
- [ ] HTTPS funktioniert
- [ ] Mobile Responsive Design getestet
- [ ] Alle Bilder laden korrekt

---

## 🔍 Fehlerbehebung

### Problem: Website zeigt noch alte Version
**Lösung:**
1. Browser-Cache leeren (Strg+F5 / Cmd+Shift+R)
2. Inkognito-Modus testen
3. IONOS Cache leeren (falls aktiviert)
4. Prüfen, ob Dateien wirklich hochgeladen wurden (FTP-Client: Dateigröße prüfen)

### Problem: 404 Fehler auf Unterseiten
**Lösung:**
1. Prüfen, ob Ordner `systems/` und `landing/` existieren
2. Prüfen, ob Dateien im richtigen Ordner sind
3. Prüfen, ob Dateiberechtigungen korrekt sind (755 für Ordner)

### Problem: .htaccess wird ignoriert
**Lösung:**
1. Dateiberechtigungen prüfen (644)
2. In IONOS Kundencenter prüfen, ob `.htaccess` aktiviert ist
3. Apache-Server muss laufen (IONOS Standard)

### Problem: Service Worker funktioniert nicht
**Lösung:**
1. Prüfen, ob `sw.js` hochgeladen wurde
2. Prüfen, ob `sw.js` im Root-Verzeichnis ist (gleicher Ordner wie `index.html`)
3. DevTools → Application → Service Workers → Prüfen auf Fehler

---

## 📞 Support

Bei Problemen:
- **IONOS Support:** https://www.ionos.de/help/
- **E-Mail:** marcel.smarsch@visionfutureframe.de

---

## 🎯 Schnellstart-Zusammenfassung

1. ✅ IONOS File Manager öffnen oder FTP-Client verbinden
2. ✅ Backup der alten Dateien erstellen (optional)
3. ✅ Alle Dateien aus der Liste hochladen
4. ✅ Ordnerstruktur `systems/` und `landing/` erstellen
5. ✅ `.htaccess` Dateiberechtigungen prüfen (644)
6. ✅ Browser-Cache leeren (Strg+F5)
7. ✅ Website testen

---

**Stand:** Januar 2025  
**Letzte Aktualisierung:** 27. Januar 2025
