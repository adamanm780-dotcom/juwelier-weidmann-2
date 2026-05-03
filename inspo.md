# Inspo — Juwelier Achim Weidmann (Branche: Juwelier / Trauringe)

> Quelle: https://dribbble.com/search/luxury-jewelry-website (grid-screenshot inspo/grid.png).
> Modus: **Limited inspo** — Patterns aus dem Such-Grid abstrahiert (kein Login auf Dribbble, Shot-Pages teils blockiert). Reicht für Stil-Steuerung, da das Genre auf Dribbble dicht besetzt ist und sich klare Wiederholungs-Patterns zeigen.

## Übergeordnete Richtung
Hell, editorial, ruhig — anders als die meisten klassischen Juwelier-Sites die low-key dark-luxury fahren. Großzügige Weißräume, dunkelbraune Walnuss-Akzente als Erdung (Header, Footer, Type-Akzente), Jade-Grün als feiner Color-Accent statt Gold. Magazine-Spread-Anmutung, Cormorant-Serif für Editorial-Headlines, viel Negativraum, ruhige Bildkompositionen mit Hand-/Atelier-Studien. Keine glitzer-marketing-Ästhetik, sondern Galerie-/Boutique-Charakter.

## Referenzen (aus inspo/grid.png)

### 1. „Pearl 'n Craft" Editorial Hero
- Stil: editorial-light cream serif
- Übernehmen:
  - Serifen-Headline groß linksbündig, viel Whitespace darunter
  - Zarter Frame um Hero-Bild, leichte Off-White Grundfläche
  - Overline-Mini-Label oben links („A Heritage Brand")
- Screenshot: inspo/grid.png

### 2. „Crafting Forever" Trauring-Editorial
- Stil: bright editorial split-hero
- Übernehmen:
  - 50/50 Split: Headline links / Produktbild rechts
  - Sehr feiner Hairline-Border um das Hero-Bild (1px)
  - „One Vow at a Time"-Tonalität: poetische, kurze Headline
- Screenshot: inspo/grid.png

### 3. „Symbol of Beauty" Editorial Layout
- Stil: bold-serif magazine
- Übernehmen:
  - Display-Serif als Hero-Wort über Vollbild-Bild gelegt
  - Seitenzahl- / Issue-Number-Style oben rechts (Mini-Detail das Editorial-Charakter pumpt)
- Screenshot: inspo/grid.png

### 4. Light Bento-Categories
- Stil: weiß bento grid, asymmetrisch
- Übernehmen:
  - 4 Kategorien (Trauringe / Verlobungsringe / Uhren / Atelier) als Bento-Cards mit unterschiedlichen Heights
  - Caption unten links pro Card („I · Trauringe", „II · Verlobungsringe" etc.)
- Screenshot: inspo/grid.png

### 5. Atelier-Shot mit großer Caption
- Stil: editorial split, Hände + Werkzeuge close-up
- Übernehmen:
  - „Atelier"-Section: Image links groß, Text-Block rechts mit Overline + Serif-Headline + 2 Absätze
  - Sticky-Caption-Effekt beim Scrollen (Caption bleibt während Bilderwechsel sichtbar — kann Phase 6 ggf. via reveal/IntersectionObserver simuliert werden)
- Screenshot: inspo/grid.png

### 6. Detail-Grid 6er Asymmetrie
- Stil: ungleiche bento, Bilder in Walnuss-Schatten gerahmt
- Übernehmen:
  - 6 Detail-Bilder als 3-Spalten-Grid mit unterschiedlichen Höhen (asymmetrisch)
  - Hover: subtle scale + duotone fade in Jade-Tone
- Screenshot: inspo/grid.png

### 7. Type-Pair Editorial
- Stil: Cormorant Garamond + Inter
- Übernehmen:
  - Cormorant für H1–H4 (italic-Variante für Akzent-Hervorhebungen wie „forever")
  - Inter für Body + Overlines (uppercase tracking 0.32em)
- Screenshot: inspo/grid.png

## Konkrete Anpassungen für Phase 6

- **Font-Pair**: **Cormorant Garamond** (Serif, Headlines) + **Inter** (Sans, Body/Overlines). Cormorant trägt das editorial-luxury-Mood ohne in Standard-Trauring-Kitsch zu kippen; Inter hält es modern.
- **Hero-Treatment**: 50/50 Split (Headline links / Hero-Bild rechts mit Hairline-Border) — Variante aus Ref 2. Statt Vollbild-Hero, weil das den Weiß-Charakter pumpt. Overline „A Heritage Atelier" oben, große Cormorant-Italic-Headline. Unten Tag-Bar (Trauringe · Verlobungsringe · Uhren) + CTA „Termin vereinbaren →".
- **Section-Flourishes**:
  - Kategorien als **Bento-Grid** mit Roman-Numeral-Captions (I/II/III/IV) — Ref 4
  - Featured-Items mit großem **Issue-Number-Style** oben rechts pro Card (Ref 3)
  - Atelier-Section als **Image-Text-Split** mit Hand-/Werkzeug-Close-Up (Ref 5)
  - Detail-Grid **asymmetrisch 3-spaltig** mit Hover-Scale + leichtem **Jade-Duotone** (Ref 6)
- **Mikro-Interaktionen-Highlights**:
  - Underline-Reveal auf Nav (Standard FlowState)
  - Ken-Burns auf Hero (auch wenn 50/50, das Bild bewegt sich subtil)
  - Reveal-on-scroll für alle Section-Headlines
  - Hover-Scale + Duotone-Filter (Jade) auf Gallery-Bilder
  - Magnetic-Effekt nur auf Haupt-CTA (subtil, optional)
- **Farb-Mood-Hinweis**: Body-Hintergrund **weiß** (Hauptfläche) — anders als Default-FlowState-Dark. Topbar + Footer in **dunkelbraun (Walnuss)**. Akzentfarbe **jade-grün** für Overlines, Borders, Hover-States. Text-Standard auf Weiß = dunkelbraun (nicht reines Schwarz). Tokens werden in Phase 4 invertiert: `--bg` = weiß, `--ivory` als Hauptfläche-Token bleibt hell, `--bg-deep` = dunkelbraun für Topbar/Footer, `--accent` = jade.
