# Vision Future Frame - Verbesserungsplan

## Übersicht der geplanten Verbesserungen

Dieses Dokument listet alle geplanten Verbesserungen basierend auf den Anforderungen auf.

### Status: In Planung

## 1. Core UX + Conversion (Priorität: HOCH)

### A) Klare CTA-Architektur
- ✅ Primary CTA: "Pilot anfragen" (bereits vorhanden)
- ✅ Secondary CTA: "Proof ansehen" (bereits vorhanden)
- ⏳ Sticky CTA im Header (Desktop) - hinzufügen
- ⏳ Bottom-Bar CTA (Mobile) - hinzufügen

### B) Contact-Flow
- ⏳ Contact-Formular mit Dropdown (Pilotpartner/Investor/Talent)
- ⏳ Calendly-Link oder Terminvorschlag
- ⏳ Auto-Reply Bestätigung (JavaScript)

### C) Proof als Trust Engine
- ✅ /proof Seite vorhanden
- ⏳ Artefakt-Galerie verbessern
- ⏳ Roadmap-Badge hinzufügen
- ⏳ "Was ist heute real?" Sektion

## 2. Performance & technische Qualität

### A) Lighthouse Targets
- Performance ≥ 95
- Accessibility ≥ 95
- Best Practices ≥ 95
- SEO ≥ 95

### B) Optimierungen
- ⏳ Bilder optimieren (WebP/AVIF)
- ⏳ Fonts self-hosted (optional)
- ⏳ Critical CSS minimieren
- ⏳ Lazy Loading für Bilder

## 3. SEO – technisch + inhaltlich

### A) Technical SEO
- ✅ robots.txt vorhanden
- ✅ sitemap.xml vorhanden
- ✅ Canonical URLs
- ✅ OpenGraph + Twitter Cards
- ⏳ 404 Seite
- ⏳ Internal Linking verbessern

### B) On-Page SEO
- ✅ Genau 1 H1
- ✅ Saubere H2/H3 Hierarchie
- ✅ Title: klar + Keyword + Brand
- ✅ Meta Description

### C) Schema.org
- ✅ Organization Schema
- ⏳ FAQPage Schema hinzufügen
- ⏳ WebSite Schema hinzufügen

### D) Content-Engine
- ⏳ /updates Seite (optional)

## 4. Security & Compliance

### A) Security Headers
- ⏳ .htaccess erweitern (CSP, HSTS, etc.)
- ⚠️ Hinweis: GitHub Pages unterstützt .htaccess nicht direkt

### B) Form-Security
- ⏳ Honeypot für Spam-Schutz
- ⏳ Rate-Limiting (JavaScript)
- ⏳ Server-side validation (benötigt Backend)

### C) DSGVO "safe wording"
- ✅ Privacy-by-design bereits erwähnt
- ⏳ Konkrete Details hinzufügen

### D) Legal Pages
- ✅ Impressum vorhanden
- ✅ Datenschutz vorhanden

## 5. Design-System

### A) Signature-Pattern
- ⏳ Frame-IDs hinzufügen ("FRAME-03 / PROOF")
- ⏳ Evidence-Chips neben Claims
- ⏳ Grid-Lines im Hintergrund (subtil)

### B) Design Tokens
- ✅ Spacing Scale (CSS Variables)
- ✅ Radius Scale
- ✅ Typography Scale
- ✅ Shadow/Glow definiert

### C) Accessibility
- ✅ Farbkontrast prüfen
- ⏳ Focus states verbessern
- ✅ Keyboard navigation
- ⏳ aria-labels erweitern

## 6. Inhalte

### A) "Was ist VisionFutureFrame?" in 2 Sätzen
- ⏳ Hero-Section: Klare 2-Satz-Definition hinzufügen

### B) "Für wen ist das?" Segmentierung
- ⏳ Landing-Blöcke: Public Sector / Enterprise / Partner/Invest

### C) Portfolio als Holding
- ✅ Projekte als Cards vorhanden
- ⏳ Status-Badges (Prototype/Pilot/Verified)
- ⏳ Factsheet-Links

## 7. Analytics

### A) Privacy-friendly Analytics
- ⏳ Plausible oder Umami Setup
- ⏳ Event Tracking (6 Events)

## 8. Wartbarkeit & Skalierung

### A) Content als Daten
- ⏳ content/portfolio.ts (für Next.js Migration)
- ⏳ content/solutions.ts
- ⏳ content/proof.ts

### B) Komponenten modular
- ⏳ components/sections/Hero.tsx (für Next.js Migration)
- ⏳ components/sections/ProofStrip.tsx
- ⏳ components/sections/PortfolioGrid.tsx

## 9. "Ultimate" Features (optional)

- ⏳ Proof Timeline
- ⏳ Downloadable One-Pager (PDF)
- ⏳ Interactive Demo Mock

## Nächste Schritte

1. Sticky CTA im Header + Mobile Bottom-Bar
2. Contact-Formular mit Dropdown
3. Content-Klarheit ("Was ist VFF?")
4. Design-System (Frame-IDs, Evidence-Chips)
5. SEO-Verbesserungen (FAQPage Schema)
