# Englisch-Abi
<!DOCTYPE html>

<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Englisch Abi 2026 – Textformen Lernblatt</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@400;500&family=DM+Sans:wght@300;400;500&display=swap');

:root {
–bg: #0e0e12;
–surface: #16161d;
–surface2: #1e1e28;
–border: #2a2a38;
–accent1: #7c6aff;
–accent2: #ff6a6a;
–accent3: #6affb8;
–accent4: #ffb86a;
–text: #e8e8f0;
–muted: #7a7a9a;
}

- { margin: 0; padding: 0; box-sizing: border-box; }

body {
background: var(–bg);
color: var(–text);
font-family: ‘DM Sans’, sans-serif;
min-height: 100vh;
padding: 2rem 1rem 4rem;
}

/* Background texture */
body::before {
content: ‘’;
position: fixed;
inset: 0;
background:
radial-gradient(ellipse 80% 50% at 20% 10%, rgba(124,106,255,0.08) 0%, transparent 60%),
radial-gradient(ellipse 60% 40% at 80% 80%, rgba(106,255,184,0.05) 0%, transparent 50%);
pointer-events: none;
z-index: 0;
}

.container {
max-width: 900px;
margin: 0 auto;
position: relative;
z-index: 1;
}

/* Header */
.header {
text-align: center;
margin-bottom: 3rem;
padding: 2.5rem 2rem;
border: 1px solid var(–border);
border-radius: 16px;
background: var(–surface);
position: relative;
overflow: hidden;
}

.header::before {
content: ‘’;
position: absolute;
top: 0; left: 0; right: 0;
height: 3px;
background: linear-gradient(90deg, var(–accent1), var(–accent3), var(–accent2));
}

.header-tag {
font-family: ‘DM Mono’, monospace;
font-size: 0.72rem;
color: var(–accent1);
letter-spacing: 0.15em;
text-transform: uppercase;
margin-bottom: 0.75rem;
}

.header h1 {
font-family: ‘Syne’, sans-serif;
font-size: clamp(1.8rem, 5vw, 2.8rem);
font-weight: 800;
line-height: 1.1;
margin-bottom: 0.5rem;
}

.header h1 span {
background: linear-gradient(135deg, var(–accent1), var(–accent3));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.header p {
color: var(–muted);
font-size: 0.95rem;
font-weight: 300;
}

/* Nav tabs */
.nav {
display: flex;
gap: 0.5rem;
flex-wrap: wrap;
margin-bottom: 2rem;
padding: 0.75rem;
background: var(–surface);
border: 1px solid var(–border);
border-radius: 12px;
}

.nav-btn {
padding: 0.5rem 1rem;
border-radius: 8px;
border: 1px solid transparent;
background: transparent;
color: var(–muted);
font-family: ‘DM Sans’, sans-serif;
font-size: 0.82rem;
font-weight: 500;
cursor: pointer;
transition: all 0.2s;
white-space: nowrap;
}

.nav-btn:hover {
color: var(–text);
background: var(–surface2);
}

.nav-btn.active {
color: var(–text);
background: var(–surface2);
border-color: var(–border);
}

.nav-btn.part1 { –dot: var(–accent1); }
.nav-btn.part2 { –dot: var(–accent3); }

.nav-btn::before {
content: ‘●’;
font-size: 0.5rem;
margin-right: 0.4rem;
color: var(–dot, var(–muted));
vertical-align: middle;
}

/* Section label */
.section-label {
font-family: ‘DM Mono’, monospace;
font-size: 0.7rem;
letter-spacing: 0.12em;
text-transform: uppercase;
color: var(–muted);
margin-bottom: 1rem;
padding-left: 0.25rem;
}

/* Cards */
.card {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 16px;
margin-bottom: 1.25rem;
overflow: hidden;
display: none;
animation: fadeIn 0.3s ease;
}

.card.visible { display: block; }
.card.all-visible { display: block; }

@keyframes fadeIn {
from { opacity: 0; transform: translateY(8px); }
to { opacity: 1; transform: translateY(0); }
}

.card-header {
padding: 1.25rem 1.5rem;
display: flex;
align-items: center;
gap: 1rem;
cursor: pointer;
user-select: none;
border-bottom: 1px solid transparent;
transition: border-color 0.2s;
}

.card.open .card-header {
border-bottom-color: var(–border);
}

.card-icon {
width: 42px;
height: 42px;
border-radius: 10px;
display: flex;
align-items: center;
justify-content: center;
font-size: 1.2rem;
flex-shrink: 0;
}

.card-title-wrap { flex: 1; }

.card-title {
font-family: ‘Syne’, sans-serif;
font-size: 1.05rem;
font-weight: 700;
margin-bottom: 0.15rem;
}

.card-subtitle {
font-size: 0.78rem;
color: var(–muted);
font-weight: 300;
}

.card-badge {
font-family: ‘DM Mono’, monospace;
font-size: 0.68rem;
padding: 0.3rem 0.7rem;
border-radius: 20px;
letter-spacing: 0.05em;
flex-shrink: 0;
}

.card-toggle {
width: 28px;
height: 28px;
border-radius: 8px;
background: var(–surface2);
border: 1px solid var(–border);
color: var(–muted);
display: flex;
align-items: center;
justify-content: center;
font-size: 0.9rem;
transition: transform 0.3s, color 0.2s;
flex-shrink: 0;
}

.card.open .card-toggle {
transform: rotate(180deg);
color: var(–text);
}

.card-body {
display: none;
padding: 1.5rem;
gap: 1.25rem;
}

.card.open .card-body {
display: grid;
grid-template-columns: 1fr 1fr;
animation: fadeIn 0.25s ease;
}

@media (max-width: 640px) {
.card.open .card-body {
grid-template-columns: 1fr;
}
}

/* Body sections */
.body-section { }

.body-section.full-width {
grid-column: 1 / -1;
}

.body-section h4 {
font-family: ‘DM Mono’, monospace;
font-size: 0.68rem;
letter-spacing: 0.1em;
text-transform: uppercase;
margin-bottom: 0.75rem;
padding-bottom: 0.4rem;
border-bottom: 1px solid var(–border);
}

.body-section ul {
list-style: none;
display: flex;
flex-direction: column;
gap: 0.4rem;
}

.body-section ul li {
font-size: 0.875rem;
color: var(–muted);
padding-left: 1rem;
position: relative;
line-height: 1.5;
font-weight: 300;
}

.body-section ul li::before {
content: ‘→’;
position: absolute;
left: 0;
color: var(–accent);
font-size: 0.75rem;
}

.body-section ul li strong {
color: var(–text);
font-weight: 500;
}

/* Structure box */
.structure {
background: var(–surface2);
border: 1px solid var(–border);
border-radius: 10px;
padding: 1rem;
font-family: ‘DM Mono’, monospace;
font-size: 0.78rem;
line-height: 1.8;
color: var(–muted);
grid-column: 1 / -1;
}

.structure .step {
display: flex;
align-items: flex-start;
gap: 0.75rem;
padding: 0.35rem 0;
border-bottom: 1px solid rgba(255,255,255,0.04);
}

.structure .step:last-child { border-bottom: none; }

.step-num {
background: var(–accent);
color: var(–bg);
width: 20px;
height: 20px;
border-radius: 5px;
display: flex;
align-items: center;
justify-content: center;
font-size: 0.65rem;
font-weight: 700;
flex-shrink: 0;
margin-top: 1px;
}

.step-text { color: var(–text); }
.step-text span { color: var(–muted); font-size: 0.72rem; }

/* Phrase chips */
.phrases {
grid-column: 1 / -1;
display: flex;
flex-wrap: wrap;
gap: 0.5rem;
}

.phrase {
background: var(–surface2);
border: 1px solid var(–border);
padding: 0.35rem 0.75rem;
border-radius: 6px;
font-size: 0.78rem;
color: var(–text);
font-family: ‘DM Mono’, monospace;
border-left: 2px solid var(–accent);
}

/* Warning box */
.warning-box {
grid-column: 1 / -1;
background: rgba(255,106,106,0.08);
border: 1px solid rgba(255,106,106,0.2);
border-radius: 10px;
padding: 1rem;
font-size: 0.82rem;
color: #ff9a9a;
line-height: 1.6;
}

.warning-box strong { color: var(–accent2); }

/* Tip box */
.tip-box {
grid-column: 1 / -1;
background: rgba(124,106,255,0.08);
border: 1px solid rgba(124,106,255,0.2);
border-radius: 10px;
padding: 1rem;
font-size: 0.82rem;
color: #b0a8ff;
line-height: 1.6;
}

.tip-box strong { color: var(–accent1); }

/* Color themes per card */
.theme-purple { –accent: var(–accent1); }
.theme-red { –accent: var(–accent2); }
.theme-green { –accent: var(–accent3); }
.theme-orange { –accent: var(–accent4); }
.theme-blue { –accent: #6ab8ff; }
.theme-pink { –accent: #ff6ab8; }
.theme-yellow { –accent: #f0ff6a; }
.theme-teal { –accent: #6affee; }

.card-icon { background: rgba(var(–accent-rgb, 124,106,255), 0.12); }
.theme-purple .card-icon { background: rgba(124,106,255,0.12); }
.theme-red .card-icon { background: rgba(255,106,106,0.12); }
.theme-green .card-icon { background: rgba(106,255,184,0.12); }
.theme-orange .card-icon { background: rgba(255,184,106,0.12); }
.theme-blue .card-icon { background: rgba(106,184,255,0.12); }
.theme-pink .card-icon { background: rgba(255,106,184,0.12); }
.theme-yellow .card-icon { background: rgba(240,255,106,0.12); }
.theme-teal .card-icon { background: rgba(106,255,238,0.12); }

.card-badge {
background: rgba(var(–badge-rgb),0.12);
color: var(–accent);
border: 1px solid rgba(var(–badge-rgb),0.2);
}

.theme-purple .card-badge { –badge-rgb: 124,106,255; }
.theme-green .card-badge { –badge-rgb: 106,255,184; }
.theme-orange .card-badge { –badge-rgb: 255,184,106; }

/* Divider */
.divider {
display: flex;
align-items: center;
gap: 1rem;
margin: 2rem 0 1.5rem;
}

.divider-line {
flex: 1;
height: 1px;
background: var(–border);
}

.divider-label {
font-family: ‘DM Mono’, monospace;
font-size: 0.7rem;
letter-spacing: 0.12em;
text-transform: uppercase;
padding: 0.35rem 0.9rem;
border-radius: 20px;
border: 1px solid var(–border);
color: var(–muted);
white-space: nowrap;
}

.divider-label.p1 { color: var(–accent1); border-color: rgba(124,106,255,0.3); background: rgba(124,106,255,0.06); }
.divider-label.p2 { color: var(–accent3); border-color: rgba(106,255,184,0.3); background: rgba(106,255,184,0.06); }

/* Expand all */
.controls {
display: flex;
gap: 0.5rem;
margin-bottom: 1.5rem;
flex-wrap: wrap;
}

.ctrl-btn {
padding: 0.45rem 1rem;
border-radius: 8px;
border: 1px solid var(–border);
background: var(–surface);
color: var(–muted);
font-size: 0.8rem;
font-family: ‘DM Sans’, sans-serif;
cursor: pointer;
transition: all 0.2s;
}

.ctrl-btn:hover { color: var(–text); background: var(–surface2); }
</style>

</head>
<body>
<div class="container">

  <div class="header">
    <div class="header-tag">Englisch Abitur Berlin 2026 · Grundkurs</div>
    <h1>Textformen <span>Lernblatt</span></h1>
    <p>Alle Texttypen · Struktur · Tipps · Phrasen</p>
  </div>

  <!-- Nav -->

  <div class="nav">
    <button class="nav-btn part1 active" onclick="filterCards('all')">Alle</button>
    <button class="nav-btn part1" onclick="filterCards('part1')">● Teil 1</button>
    <button class="nav-btn part2" onclick="filterCards('part2')">● Teil 2 Mediation</button>
    <button class="nav-btn part1" onclick="filterCards('analyse')">Analyse</button>
    <button class="nav-btn part1" onclick="filterCards('argumentativ')">Argumentativ</button>
    <button class="nav-btn part1" onclick="filterCards('kreativ')">Kreativ</button>
  </div>

  <div class="controls">
    <button class="ctrl-btn" onclick="expandAll()">▼ Alle aufklappen</button>
    <button class="ctrl-btn" onclick="collapseAll()">▲ Alle zuklappen</button>
  </div>

  <!-- TEIL 1 -->

  <div class="divider"><div class="divider-line"></div><div class="divider-label p1">Teil 1 — Leseverstehen & Schreiben</div><div class="divider-line"></div></div>

  <!-- SUMMARY -->

  <div class="card theme-purple visible" data-tags="part1 analyse" id="summary">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">📄</div>
      <div class="card-title-wrap">
        <div class="card-title">Summary</div>
        <div class="card-subtitle">Aufgabe 1 · Zusammenfassung eines englischen Texts</div>
      </div>
      <div class="card-badge">Aufgabe 1</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent1)">Was zu tun ist</h4>
        <ul>
          <li>Den Text <strong>sinngemäß</strong> in eigenen Worten zusammenfassen</li>
          <li><strong>Keine eigene Meinung</strong> – rein sachlich bleiben</li>
          <li>Hauptaussagen rausfiltern, Details weglassen</li>
          <li>Reihenfolge des Originals <strong>nicht</strong> zwingend folgen</li>
          <li>Nur Infos aus dem Text – kein Vorwissen einbringen</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent1)">Häufige Fehler</h4>
        <ul>
          <li><strong>Zu lang</strong> – eine Summary ist kurz und kompakt</li>
          <li>Direkte Zitate aus dem Text verwenden</li>
          <li>Eigene Meinung oder Bewertung einfließen lassen</li>
          <li>Zu viele Details, Beispiele aus dem Original übernehmen</li>
          <li>Mit "In this text..." anfangen (zu generisch)</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:var(--accent1)">1</div><div class="step-text">Topic sentence <span>– Worum geht es? Autor, Quelle, Hauptthema in 1 Satz</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent1)">2</div><div class="step-text">Main points <span>– Die wichtigsten Aussagen des Texts in logischer Reihenfolge</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent1)">3</div><div class="step-text">Conclusion <span>– Fazit oder Schlussaussage des Texts (falls vorhanden)</span></div></div>
      </div>
      <div class="body-section full-width">
        <h4 style="color:var(--accent1)">Nützliche Phrasen</h4>
      </div>
      <div class="phrases">
        <span class="phrase">The article/text deals with...</span>
        <span class="phrase">The author argues that...</span>
        <span class="phrase">According to the text...</span>
        <span class="phrase">The main point is that...</span>
        <span class="phrase">Furthermore, the text states...</span>
        <span class="phrase">In conclusion, the author...</span>
        <span class="phrase">The text focuses on...</span>
        <span class="phrase">As a result,...</span>
      </div>
    </div>
  </div>

  <!-- OUTLINE -->

  <div class="card theme-orange visible" data-tags="part1 analyse" id="outline">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">🗂️</div>
      <div class="card-title-wrap">
        <div class="card-title">Outline</div>
        <div class="card-subtitle">Aufgabe 1 · Strukturierte Gliederung</div>
      </div>
      <div class="card-badge">Aufgabe 1</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent4)">Was zu tun ist</h4>
        <ul>
          <li>Strukturierte <strong>Gliederung</strong> eines Arguments oder Texts</li>
          <li><strong>Stichpunkte</strong>, keine ganzen Sätze</li>
          <li>Hierarchisch aufbauen (I. → A. → 1.)</li>
          <li>Logische Argumentation zeigen</li>
          <li>Nur die wichtigsten Punkte – keine Details</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent4)">Häufige Fehler</h4>
        <ul>
          <li>Ganze Sätze schreiben statt <strong>Stichpunkte</strong></li>
          <li>Zu viele Unterpunkte – 2–3 pro Abschnitt reichen</li>
          <li>Keine klare Hierarchie erkennbar</li>
          <li>Eigene Meinung reinbringen (wenn nicht gefragt)</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">I</div><div class="step-text">Introduction <span>– Topic + Thesis statement</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">II</div><div class="step-text">Main Body <span>– A. First argument / B. Second argument / C. Counterargument</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">III</div><div class="step-text">Conclusion <span>– Summary + final statement / recommendation</span></div></div>
      </div>
      <div class="tip-box">
        <strong>💡 Tipp:</strong> Bei einer Outline musst du <em>nicht</em> einen vollständigen Text schreiben. Stichpunkte wie "→ social media increases anxiety in teens" reichen völlig aus. Bewertung geht nach Struktur und Logik, nicht nach Sprache.
      </div>
    </div>
  </div>

  <!-- TEXT ANALYSIS -->

  <div class="card theme-red visible" data-tags="part1 analyse" id="analysis">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">🔍</div>
      <div class="card-title-wrap">
        <div class="card-title">Text Analysis</div>
        <div class="card-subtitle">Aufgabe 2 · Analyse mit Stilmitteln</div>
      </div>
      <div class="card-badge">Aufgabe 2</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent2)">Was zu tun ist</h4>
        <ul>
          <li>Text auf <strong>Inhalt + sprachliche Mittel</strong> analysieren</li>
          <li>Stilmittel nennen, belegen (Zitat), <strong>Wirkung erklären</strong></li>
          <li>Immer: Beleg → Name → Wirkung (P-E-E Methode)</li>
          <li>Auf Struktur, Ton, Perspektive eingehen</li>
          <li>Fiktional: Erzählperspektive, Charaktere, Setting</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent2)">Wichtige Stilmittel</h4>
        <ul>
          <li><strong>Metaphor</strong> – indirekter Vergleich</li>
          <li><strong>Simile</strong> – "like" / "as" Vergleich</li>
          <li><strong>Alliteration</strong> – gleiche Anfangsbuchstaben</li>
          <li><strong>Repetition</strong> – Wiederholung zur Betonung</li>
          <li><strong>Rhetorical question</strong> – Frage ohne Antwort</li>
          <li><strong>Irony/Sarcasm</strong> – Gegenteil gemeint</li>
          <li><strong>Hyperbole</strong> – Übertreibung</li>
          <li><strong>Personification</strong> – Vermenschlichung</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:var(--accent2)">1</div><div class="step-text">Introduction <span>– Titel, Autor, Textsorte, Thema, Intention in 2–3 Sätzen</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent2)">2</div><div class="step-text">Content <span>– Kurze Zusammenfassung der Hauptaussage</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent2)">3</div><div class="step-text">Language Analysis <span>– Stilmittel mit Beleg + Wirkung (P-E-E)</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent2)">4</div><div class="step-text">Conclusion <span>– Gesamtwirkung + Intention des Autors</span></div></div>
      </div>
      <div class="body-section full-width">
        <h4 style="color:var(--accent2)">P-E-E Methode (Point – Evidence – Effect)</h4>
      </div>
      <div class="phrases">
        <span class="phrase">The author uses... to suggest/show/highlight...</span>
        <span class="phrase">The use of [device] creates a feeling of...</span>
        <span class="phrase">This implies that...</span>
        <span class="phrase">The [metaphor] "..." conveys...</span>
        <span class="phrase">By using..., the author emphasises...</span>
        <span class="phrase">This has the effect of...</span>
        <span class="phrase">The repetition of "..." reinforces...</span>
        <span class="phrase">The rhetorical question makes the reader...</span>
      </div>
    </div>
  </div>

  <!-- CARTOON ANALYSIS -->

  <div class="card theme-pink visible" data-tags="part1 analyse" id="cartoon">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">🖼️</div>
      <div class="card-title-wrap">
        <div class="card-title">Cartoon / Image Analysis</div>
        <div class="card-subtitle">Aufgabe 2 · Diskontinuierliche Texte</div>
      </div>
      <div class="card-badge">Aufgabe 2</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:#ff6ab8">Was zu tun ist</h4>
        <ul>
          <li>Bild <strong>beschreiben</strong> (was ist zu sehen?)</li>
          <li>Botschaft / Message <strong>interpretieren</strong></li>
          <li>Symbolik, Ironie, Übertreibung erkennen</li>
          <li>Kontext / aktueller Bezug herstellen</li>
          <li>Stilmittel der Bildsprache benennen</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:#ff6ab8">Bildsprachliche Mittel</h4>
        <ul>
          <li><strong>Symbolism</strong> – Objekte stehen für Ideen</li>
          <li><strong>Exaggeration/Caricature</strong> – übertriebene Darstellung</li>
          <li><strong>Irony</strong> – Gegensatz Bild/Text</li>
          <li><strong>Labeling</strong> – Beschriftungen im Bild</li>
          <li><strong>Juxtaposition</strong> – Gegensätze nebeneinander</li>
          <li><strong>Size/Proportion</strong> – Größenverhältnisse</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:#ff6ab8">1</div><div class="step-text">Description <span>– Was ist zu sehen? (foreground, background, characters)</span></div></div>
        <div class="step"><div class="step-num" style="background:#ff6ab8">2</div><div class="step-text">Interpretation <span>– Was bedeutet es? Symbolik? Botschaft?</span></div></div>
        <div class="step"><div class="step-num" style="background:#ff6ab8">3</div><div class="step-text">Devices <span>– Welche Mittel werden eingesetzt + Wirkung?</span></div></div>
        <div class="step"><div class="step-num" style="background:#ff6ab8">4</div><div class="step-text">Context <span>– Bezug zum Thema / zur Realität herstellen</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">The cartoon shows/depicts...</span>
        <span class="phrase">In the foreground/background...</span>
        <span class="phrase">The cartoonist uses... to symbolise...</span>
        <span class="phrase">This is meant to criticise/highlight...</span>
        <span class="phrase">The exaggeration of... suggests...</span>
        <span class="phrase">The overall message is...</span>
      </div>
    </div>
  </div>

  <!-- ESSAY / COMMENT -->

  <div class="card theme-blue visible" data-tags="part1 argumentativ" id="essay">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">✍️</div>
      <div class="card-title-wrap">
        <div class="card-title">Essay / Comment</div>
        <div class="card-subtitle">Aufgabe 3 · Argumentativer Text</div>
      </div>
      <div class="card-badge">Aufgabe 3</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:#6ab8ff">Was zu tun ist</h4>
        <ul>
          <li>Klare <strong>These</strong> aufstellen und verteidigen</li>
          <li>Pro- und Contra-Argumente abwägen</li>
          <li><strong>Formelle Sprache</strong> – keine Umgangssprache</li>
          <li>Eigene Position klar am Ende vertreten</li>
          <li>Logische Übergänge zwischen Absätzen</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:#6ab8ff">Häufige Fehler</h4>
        <ul>
          <li>Keine klare Position beziehen</li>
          <li>Argumente ohne Belege / Beispiele</li>
          <li>Zu kurze Absätze (mind. 3–4 Sätze pro Punkt)</li>
          <li>Informelle Sprache ("I think it's pretty bad")</li>
          <li>Keine Gegenargumente berücksichtigen</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:#6ab8ff;color:#000">1</div><div class="step-text">Introduction <span>– Hook + Kontext + These (eigene Position)</span></div></div>
        <div class="step"><div class="step-num" style="background:#6ab8ff;color:#000">2</div><div class="step-text">Argument 1 <span>– Hauptargument + Beleg + Erklärung</span></div></div>
        <div class="step"><div class="step-num" style="background:#6ab8ff;color:#000">3</div><div class="step-text">Argument 2 <span>– Weiteres Argument + Beispiel</span></div></div>
        <div class="step"><div class="step-num" style="background:#6ab8ff;color:#000">4</div><div class="step-text">Counterargument <span>– Gegenargument nennen + entkräften</span></div></div>
        <div class="step"><div class="step-num" style="background:#6ab8ff;color:#000">5</div><div class="step-text">Conclusion <span>– These wiederholen, Fazit, Ausblick</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">It is widely argued that...</span>
        <span class="phrase">One could argue that...</span>
        <span class="phrase">However, it must be considered...</span>
        <span class="phrase">Furthermore / Moreover / In addition...</span>
        <span class="phrase">Despite this, ...</span>
        <span class="phrase">In conclusion, it is clear that...</span>
        <span class="phrase">Taking everything into account...</span>
        <span class="phrase">While X, it is important to note...</span>
      </div>
    </div>
  </div>

  <!-- SPEECH / REDE -->

  <div class="card theme-green visible" data-tags="part1 argumentativ kreativ" id="speech">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">🎤</div>
      <div class="card-title-wrap">
        <div class="card-title">Speech / Rede</div>
        <div class="card-subtitle">Aufgabe 3 · Persuasive Rede</div>
      </div>
      <div class="card-badge">Aufgabe 3</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent3)">Was zu tun ist</h4>
        <ul>
          <li>Direkte <strong>Ansprache</strong> des Publikums</li>
          <li>Rhetorische Mittel bewusst einsetzen</li>
          <li>Klar überzeugend / persuasiv argumentieren</li>
          <li>Kontext beachten: Wer spricht? Wo? Zu wem?</li>
          <li>Starke Eröffnung und starkes Ende</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent3)">Rhetorische Mittel für Reden</h4>
        <ul>
          <li><strong>Rhetorical questions</strong> – Publikum einbeziehen</li>
          <li><strong>Repetition / Anaphora</strong> – Wirkung verstärken</li>
          <li><strong>Rule of three</strong> – drei Punkte nacheinander</li>
          <li><strong>Direct address</strong> – "You and I know that..."</li>
          <li><strong>Call to action</strong> – Zum Handeln auffordern</li>
          <li><strong>Inclusive language</strong> – "we", "our", "together"</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:var(--accent3);color:#000">1</div><div class="step-text">Opening <span>– Anrede + starker Einstieg (Frage, Zitat, Statistik)</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent3);color:#000">2</div><div class="step-text">Main body <span>– 2–3 Argumente, klar gegliedert, mit Beispielen</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent3);color:#000">3</div><div class="step-text">Counterargument <span>– kurz ansprechen + widerlegen</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent3);color:#000">4</div><div class="step-text">Closing <span>– Call to action + unvergesslicher letzter Satz</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">Ladies and gentlemen,...</span>
        <span class="phrase">Dear fellow students,...</span>
        <span class="phrase">Ask yourself: ...</span>
        <span class="phrase">We cannot afford to ignore...</span>
        <span class="phrase">The time for action is now.</span>
        <span class="phrase">Together, we can...</span>
        <span class="phrase">I urge you to...</span>
        <span class="phrase">Let me leave you with this thought:</span>
        <span class="phrase">Thank you for your attention.</span>
      </div>
    </div>
  </div>

  <!-- LETTER TO THE EDITOR -->

  <div class="card theme-yellow visible" data-tags="part1 argumentativ" id="letter-editor">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">📰</div>
      <div class="card-title-wrap">
        <div class="card-title">Letter to the Editor</div>
        <div class="card-subtitle">Aufgabe 3 · Formeller Leserbrief</div>
      </div>
      <div class="card-badge">Aufgabe 3</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:#f0ff6a">Was zu tun ist</h4>
        <ul>
          <li>Reaktion auf einen <strong>Artikel / Bericht</strong></li>
          <li>Formelle Sprache und formeller <strong>Briefaufbau</strong></li>
          <li>Bezug auf den Artikel herstellen</li>
          <li>Eigene Position klar argumentieren</li>
          <li>Höflicher aber bestimmter Ton</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:#f0ff6a">Formaler Aufbau</h4>
        <ul>
          <li>Kein Absenderadresse nötig im Abi</li>
          <li>Anrede: <strong>Dear Editor,</strong></li>
          <li>Erster Satz: Bezug auf Artikel</li>
          <li>Abschluss: <strong>Yours faithfully/sincerely,</strong></li>
          <li>Name am Ende nicht vergessen</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:#f0ff6a;color:#000">1</div><div class="step-text">Opening <span>– "I am writing in response to your article about..."</span></div></div>
        <div class="step"><div class="step-num" style="background:#f0ff6a;color:#000">2</div><div class="step-text">Position <span>– Eigene Meinung/These klar formulieren</span></div></div>
        <div class="step"><div class="step-num" style="background:#f0ff6a;color:#000">3</div><div class="step-text">Arguments <span>– 2–3 Argumente mit Belegen</span></div></div>
        <div class="step"><div class="step-num" style="background:#f0ff6a;color:#000">4</div><div class="step-text">Closing <span>– Forderung oder Appell + formeller Abschluss</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">I am writing in response to...</span>
        <span class="phrase">I was [pleased/concerned] to read...</span>
        <span class="phrase">I strongly believe that...</span>
        <span class="phrase">It is deeply concerning that...</span>
        <span class="phrase">I urge your readers to consider...</span>
        <span class="phrase">Yours faithfully, / Yours sincerely,</span>
      </div>
    </div>
  </div>

  <!-- BLOG POST -->

  <div class="card theme-teal visible" data-tags="part1 kreativ" id="blog">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">💻</div>
      <div class="card-title-wrap">
        <div class="card-title">Blog Post</div>
        <div class="card-subtitle">Aufgabe 3 · Semi-formeller Meinungstext</div>
      </div>
      <div class="card-badge">Aufgabe 3</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:#6affee">Was zu tun ist</h4>
        <ul>
          <li>Lockerer, aber <strong>nicht zu informeller</strong> Ton</li>
          <li>Direkte Leseransprache erlaubt</li>
          <li>Persönliche Meinung und Erfahrungen einbringen</li>
          <li>Titel / Überschrift nicht vergessen!</li>
          <li>Einladend und interessant schreiben</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:#6affee">Ton & Stil</h4>
        <ul>
          <li>Contractions erlaubt: <strong>it's, don't, I've</strong></li>
          <li>Leser direkt ansprechen: <strong>"you", "we"</strong></li>
          <li>Rhetorische Fragen einbauen</li>
          <li>Kurze, lebendige Sätze möglich</li>
          <li>Humor / persönliche Anekdoten möglich</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:#6affee;color:#000">1</div><div class="step-text">Headline <span>– Catchy Überschrift (Frage, Provokation, Wortspiel)</span></div></div>
        <div class="step"><div class="step-num" style="background:#6affee;color:#000">2</div><div class="step-text">Hook <span>– Einstieg der Leser fesselt (Frage, Statistik, Story)</span></div></div>
        <div class="step"><div class="step-num" style="background:#6affee;color:#000">3</div><div class="step-text">Main body <span>– Argumente / Punkte mit persönlichem Bezug</span></div></div>
        <div class="step"><div class="step-num" style="background:#6affee;color:#000">4</div><div class="step-text">Closing <span>– Fazit + Aufruf an Leser (Kommentar, Diskussion)</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">Have you ever wondered...?</span>
        <span class="phrase">Let me tell you something...</span>
        <span class="phrase">Personally, I believe...</span>
        <span class="phrase">What do you think? Let me know...</span>
        <span class="phrase">Here's the thing:...</span>
        <span class="phrase">If you ask me,...</span>
        <span class="phrase">The bottom line is...</span>
      </div>
    </div>
  </div>

  <!-- OPEN LETTER -->

  <div class="card theme-purple visible" data-tags="part1 kreativ argumentativ" id="open-letter">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">📬</div>
      <div class="card-title-wrap">
        <div class="card-title">Open Letter</div>
        <div class="card-subtitle">Aufgabe 3 · Offener Brief</div>
      </div>
      <div class="card-badge">Aufgabe 3</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent1)">Was zu tun ist</h4>
        <ul>
          <li>Formeller Brief an eine <strong>öffentliche Person/Institution</strong></li>
          <li>Für ein <strong>breiteres Publikum</strong> geschrieben</li>
          <li>Klare Forderung oder Botschaft</li>
          <li>Ton: respektvoll aber direkt und überzeugend</li>
          <li>Briefformat einhalten</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent1)">Unterschied zum Letter to Editor</h4>
        <ul>
          <li>Adressiert an <strong>Person/Organisation</strong>, nicht Editor</li>
          <li>Wird oft <strong>veröffentlicht</strong> – für alle lesbar</li>
          <li>Tone etwas <strong>persönlicher</strong> möglich</li>
          <li>Klare Forderung/Appell am Ende</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:var(--accent1)">1</div><div class="step-text">Salutation <span>– "Dear Mr President / Dear Mayor of Berlin,..."</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent1)">2</div><div class="step-text">Introduction <span>– Wer schreibt? Warum? Worum geht es?</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent1)">3</div><div class="step-text">Arguments <span>– 2–3 klare Punkte mit Belegen</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent1)">4</div><div class="step-text">Demand/Appeal <span>– Konkrete Forderung oder Bitte</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent1)">5</div><div class="step-text">Closing <span>– "Yours sincerely," + Name</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">I am writing on behalf of...</span>
        <span class="phrase">As a concerned citizen/student...</span>
        <span class="phrase">It is time to take action on...</span>
        <span class="phrase">We call upon you to...</span>
        <span class="phrase">The evidence clearly shows...</span>
        <span class="phrase">Yours sincerely,</span>
      </div>
    </div>
  </div>

  <!-- TEIL 2 DIVIDER -->

  <div class="divider"><div class="divider-line"></div><div class="divider-label p2">Teil 2 — Sprachmittlung / Mediation</div><div class="divider-line"></div></div>

  <!-- MEDIATION ALLGEMEIN -->

  <div class="card theme-green visible" data-tags="part2" id="mediation">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">🔄</div>
      <div class="card-title-wrap">
        <div class="card-title">Sprachmittlung – Grundprinzip</div>
        <div class="card-subtitle">Teil 2 · Deutsch → Englisch sinngemäß übertragen</div>
      </div>
      <div class="card-badge">Teil 2</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent3)">Das Wichtigste</h4>
        <ul>
          <li><strong>Kein wörtliches Übersetzen!</strong> – sinngemäß übertragen</li>
          <li>Nur die für die Aufgabe <strong>relevanten Infos</strong> rausnehmen</li>
          <li>Adressatengerecht schreiben – Ton anpassen</li>
          <li>Eigene Einleitung/Überleitung schreiben</li>
          <li>Deutschen Text im Kopf lassen – auf Englisch neu formulieren</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent3)">Häufige Fehler</h4>
        <ul>
          <li>Wort-für-Wort Übersetzung → klingt unnatürlich</li>
          <li>Zu viele/zu wenige Infos aus dem Text</li>
          <li>Falscher Ton (zu formell/informell)</li>
          <li>Keine Einleitung zum Kontext</li>
          <li>Grammatik-Fehler durch deutschen Satzbau</li>
        </ul>
      </div>
      <div class="warning-box">
        <strong>⚠️ Achtung:</strong> Bei der Sprachmittlung wirst du bewertet auf: Inhaltsvollständigkeit, adressatengerechten Ton UND sprachliche Korrektheit. Alle drei Bereiche zählen!
      </div>
      <div class="phrases">
        <span class="phrase">I came across an article about...</span>
        <span class="phrase">I thought you might be interested in...</span>
        <span class="phrase">According to a German article,...</span>
        <span class="phrase">The text mentions that...</span>
        <span class="phrase">In other words,...</span>
        <span class="phrase">The author points out that...</span>
      </div>
    </div>
  </div>

  <!-- MEDIATION EMAIL -->

  <div class="card theme-orange visible" data-tags="part2" id="med-email">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">📧</div>
      <div class="card-title-wrap">
        <div class="card-title">Mediation – E-Mail</div>
        <div class="card-subtitle">Teil 2 · Häufigste Mediation-Textsorte</div>
      </div>
      <div class="card-badge">Teil 2</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:var(--accent4)">Formales nicht vergessen</h4>
        <ul>
          <li><strong>Subject:</strong> Betreff oben drüber</li>
          <li>Anrede: <strong>Dear Mr/Ms...</strong> (formell) oder <strong>Hi [Name],</strong></li>
          <li>Abschluss: <strong>Best regards / Kind regards / Cheers</strong></li>
          <li>Deinen Namen am Ende</li>
          <li>Ton nach Empfänger: Chef → formell, Freund → informell</li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:var(--accent4)">Inhalt</h4>
        <ul>
          <li>Kurze Einleitung: Warum schreibst du?</li>
          <li>Wichtigste Infos aus dem deutschen Text übertragen</li>
          <li>Eigene Kommentare / Meinung nur wenn gefragt</li>
          <li>Kurz und präzise – keine Roman-Länge</li>
        </ul>
      </div>
      <div class="structure">
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">1</div><div class="step-text">Subject: <span>Kurzer, aussagekräftiger Betreff</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">2</div><div class="step-text">Salutation <span>– Dear.../Hi...</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">3</div><div class="step-text">Opening line <span>– Kontext erklären: "I came across..."</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">4</div><div class="step-text">Main content <span>– Relevante Infos aus deutschem Text auf Englisch</span></div></div>
        <div class="step"><div class="step-num" style="background:var(--accent4);color:#000">5</div><div class="step-text">Closing <span>– "Let me know if..." + Best regards + Name</span></div></div>
      </div>
      <div class="phrases">
        <span class="phrase">Subject: Info about [topic]</span>
        <span class="phrase">I hope this email finds you well.</span>
        <span class="phrase">I recently read an article about... and thought you'd find it interesting.</span>
        <span class="phrase">According to the article,...</span>
        <span class="phrase">The key points are:...</span>
        <span class="phrase">Let me know if you have any questions.</span>
        <span class="phrase">Best regards, / Kind regards,</span>
      </div>
    </div>
  </div>

  <!-- MEDIATION SUMMARY -->

  <div class="card theme-blue visible" data-tags="part2" id="med-summary">
    <div class="card-header" onclick="toggle(this)">
      <div class="card-icon">📋</div>
      <div class="card-title-wrap">
        <div class="card-title">Mediation – Summary / Brief</div>
        <div class="card-subtitle">Teil 2 · Für englischsprachige Person zusammenfassen</div>
      </div>
      <div class="card-badge">Teil 2</div>
      <div class="card-toggle">▼</div>
    </div>
    <div class="card-body">
      <div class="body-section">
        <h4 style="color:#6ab8ff">Was zu tun ist</h4>
        <ul>
          <li>Deutschen Text für <strong>englischsprachige Person</strong> aufbereiten</li>
          <li>Kontext erklären (woher kommt der Text?)</li>
          <li>Ton je nach Aufgabenstellung anpassen</li>
          <li>Nur relevante Infos für den <strong>spezifischen Empfänger</strong></li>
        </ul>
      </div>
      <div class="body-section">
        <h4 style="color:#6ab8ff">Tipps</h4>
        <ul>
          <li>Immer fragen: Was braucht <strong>diese Person</strong> zu wissen?</li>
          <li>Kulturelle Begriffe erklären (z.B. "Gymnasium" = grammar school)</li>
          <li>Zahlen und Fakten präzise übertragen</li>
          <li>Eigene Meinung nur wenn ausdrücklich gefragt</li>
        </ul>
      </div>
      <div class="phrases">
        <span class="phrase">I would like to summarise a German article for you.</span>
        <span class="phrase">The article was published in...</span>
        <span class="phrase">To give you some context,...</span>
        <span class="phrase">In Germany, this means that...</span>
        <span class="phrase">The most important points are...</span>
        <span class="phrase">I hope this gives you a good overview.</span>
      </div>
      <div class="tip-box">
        <strong>💡 Tipp:</strong> Bei kulturspezifischen deutschen Begriffen (Abitur, Gymnasium, Bundesrat etc.) kurz auf Englisch erklären – der englische Empfänger kennt das nicht!
      </div>
    </div>
  </div>

</div>

<script>
  function toggle(header) {
    const card = header.parentElement;
    card.classList.toggle('open');
  }

  function filterCards(tag) {
    const cards = document.querySelectorAll('.card');
    const buttons = document.querySelectorAll('.nav-btn');
    buttons.forEach(b => b.classList.remove('active'));
    event.target.classList.add('active');

    cards.forEach(card => {
      if (tag === 'all') {
        card.classList.add('visible');
      } else {
        const tags = card.dataset.tags || '';
        if (tags.includes(tag)) {
          card.classList.add('visible');
        } else {
          card.classList.remove('visible');
          card.classList.remove('open');
        }
      }
    });
  }

  function expandAll() {
    document.querySelectorAll('.card.visible').forEach(c => c.classList.add('open'));
  }

  function collapseAll() {
    document.querySelectorAll('.card').forEach(c => c.classList.remove('open'));
  }
</script>

</body>
</html>
