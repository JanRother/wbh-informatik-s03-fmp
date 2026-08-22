---
role: format-reference
language: de
format-version: 1
---

<!-- 
FORMAT REFERENCE

This file defines the note format for all other files in notes/*.md. It is not a content note. 
All note files (01_*.md, 02_*.md, …) follow the structure demonstrated below.
-->

# Notes for Paper | Section 00: Beispiel

> Wilhelm Büchner Hochschule  
> Computer Science  
> Assignment: Forschungsmethoden und Projektmanagement  
> 
> Notes  
> for Paper: "Generierung von Quellcode durch Large Language Models – Stand der Technik"  
> Section 0: Beispiel
> 
> 2026-08
  
> Datei: `n/a`

<!-- 
Datei: `n/a` is used only in this example file. 
In all real note files this field holds the path to the corresponding LaTeX source, e.g. `paper/chapters/01/_introduction.tex`.
-->

**Format Legend**

| Element                           | Rule                                                                                                                                                                   |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `# …`                             | Exactly one H1 per file: `Notes for Paper \                                                                                                                            |
| Blockquote Block                  | Metadata header directly below H1; fixed field order: Institution / Degree / Course / blank / "Notes" label / Paper title / Section / blank / Date / blank / File path |
| `Datei: ...`                      | Path to the corresponding LaTeX file (`paper/chapters/NN/_name.tex`); `n/a` only in this example                                                                       |
| `-----`                           | Fixed separator (exactly five dashes) between metadata and content                                                                                                     |
| `## ...`                          | One per `\subsection{}` in the `.tex` file; German title identical to LaTeX                                                                                            |
| `### ...`                         | One per `\subsubsection{}` in the `.tex` file; German title identical to LaTeX                                                                                         |
| `[NN, S. X...]`                   | Citation block on its own line, placed directly before the bullet group it sources                                                                                     |
| `**GRAFIK:** [G-NN]`              | Figure reference placeholder on its own line; NN = figure ID                                                                                                           |
| Bullet after a Citation Block     | Content sourced from that reference                                                                                                                                    |
| Bullet with no preceding Citation | Own synthesis or transitional thought; no external source                                                                                                              |
| `- Inhalt des ...`                | Blank placeholder bullet in template/blank note files awaiting real content                                                                                            |

**Citation format:** `[<bib-key>, S. <page><variant>]`

| Variant  | Meaning                                     | Example           |
|----------|---------------------------------------------|-------------------|
| *(none)* | Single page only                            | `[100, S. 5]`     |
| `f.`     | Given page + the immediately following page | `[100, S. 5 f.]`  |
| `ff.`    | Given page + multiple following pages       | `[100, S. 5 ff.]` |

-----

## Erster Unterabschnitt

[100, S. 1 f.]
- wissenschaftliche Arbeit ist besondere Form der schriftlichen Arbeit
- gekennzeichnet durch systematische, methodische und nachvollziehbare Vorgehensweise
- ausgerichtet auf Erkenntnisgewinnung, Beantwortung von Forschungsfragen und Beitrag zum wissenschaftlichen Diskurs

[100, S. 8 f.]
- Merkmale sind
  - klare Zielsetzung und Forschungsfragen
  - strukturierte Methodik und Vorgehensweise
  - kritische Auseinandersetzung mit bestehender Literatur und Forschungsergebnissen
  - transparente Darstellung von Ergebnissen, Analysen und Schlussfolgerungen
  - Einhaltung wissenschaftlicher Standards, wie Zitation, Quellenangaben und Plagiatsvermeidung

<!-- own synthesis, no citation: bullet group without a preceding [bib-key, S. X] block -->
- deshalb ist Ausgestaltung des Themas vor Beginn der Arbeit von Bedeutung

[101, S. 50 ff.]
- verschiedene Möglichkeiten zur Vorbereitung:
  - Literaturrecherche und -analyse
  - Entwicklung von Forschungsfragen und Hypothesen
  - Auswahl geeigneter Forschungsmethoden und -designs
  - Erstellung eines Arbeitsplans und Zeitplans
  - Identifikation relevanter Ressourcen und Materialien

<!-- own synthesis, no citation: -->
- nach Vorbereitung folgt Durchführung
- folgende Abschnitte gehen ins Detail

## Zweiter Unterabschnitt

<!-- own synthesis, no citation: -->
- Durchführung nach verschiedenen Methoden
- Methode entscheidet über Vorgehensweise, Datenerhebung und -analyse

**GRAFIK:** [G-00]

<!-- own synthesis, no citation: -->
- Abbildung zeigt Forschungsprozess

[200, S. 100]
- Forschungsprozess ist iterativ und zyklisch
- Ergebnisse und Erkenntnisse führen zu neuen Forschungsfragen und Hypothesen

## Dritter Unterabschnitt

- Inhalt des Unterabschnitts

### Erster Unterunterabschnitt

- Inhalt des Unterunterabschnitts

### Zweiter Unterunterabschnitt

- Inhalt des Unterunterabschnitts

## Letzter Unterabschnitt

- zusammenfassend ist wissenschaftliche Arbeit systematisch, methodisch und nachvollziehbar
- Vorgehensweisen sind variabel und abhängig von Forschungsfragen, Methoden und Zielen

<!-- PROMPT USE:
When asked to create or fill a note file in this format, follow these rules exactly:

1.  H1 heading:      "Notes for Paper | Section NN: <German section title>"
2.  Metadata block:  Blockquote directly below H1 with fields in this order:
                     Institution / Degree / Course / blank line / "Notes" label /
                     Paper title / Section / blank line / Date / blank line / File path
3.  Separator:       Five dashes (-----) on its own line
4.  Sections:        H2 (##) for each \subsection, H3 (###) for each \subsubsection;
                     use the exact German titles from the .tex file
5.  Content:         All content as bullet points — no prose paragraphs
6.  Citations:       [bib-key, S. page f./ff.] as a standalone line before the related bullet group
7.  Figures:         **GRAFIK:** [G-NN] as a standalone line
8.  Own synthesis:   Bullets with no preceding citation block = own thought, no source needed
9.  Blank templates: Use "- Inhalt des Unterabschnitts" as the placeholder bullet
-->
