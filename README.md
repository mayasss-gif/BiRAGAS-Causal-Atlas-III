# BiRAGAS · Causal Atlas · Vol. III — A Kinetic Field Guide

A third, more **artistic and animated** redesign of the BiRAGAS Investors Technical Playbook. Same 25 modules, same Causion agent, same three tiers — rendered this time as an **animated typographic poster series**.

## Concept

**"The Kinetic Field Guide"**

Where the *Investor Pitch Guide v2* is refined dark editorial and the *Systems Manual № 007* is a printed engineering manual, this is **editorial-as-kinetic-poster-series**. Genealogy: Wolfgang Weingart's Swiss-punk experiments, Neville Brody's *The Face*, contemporary risograph zines, the kinetic-typography poster work of M/M Paris and Mirko Borsche. Every section is a fully composed *poster* with art-school energy. The centerpiece is a **spinning typographic mandala** of all 25 module names arranged in three concentric rings.

## The art moves

- **Spinning mandala** — three concentric SVG `textPath` rings carrying all 25 module names. Outer ring (T2 · 10 modules) spins one way at 90s/rev, middle ring (T1 · 8 engines, hot pink) spins the other way at 60s/rev, inner ring (T3 · 7 modules, cyan) spins again. Centre pulses with `causion · agent · 01` in mulberry. Compass marks N/S/E/W in the cardinal directions.
- **Rotating conic gradient backdrop** on the cover — 120s full rotation, cream → chartreuse → cream → cyan → cream → mulberry → cream.
- **Three-lane marquee** scrolling at different speeds, two reversed: Bodoni italic 24pt (60s), Unbounded 13pt all-caps mulberry-bg (80s reverse), Major Mono 14pt (100s).
- **Cursor with shrinking trail** — chartreuse blob plus three lag-following copies at decreasing opacity. `difference` blend mode so it inverts over chartreuse panels.
- **Variable font weight tied to scroll velocity** — Bodoni headlines breathe heavier as you scroll faster, lighter when you stop. Capped 400–900.
- **Animated typing bar** in the Causion section — cycles through 6 plausible scientist prompts at 55ms per character.
- **Stat counters** that animate 0 → 25 / 0 → 08 / 0 → 03 / 0 → 01 with ease-out-cubic on first scroll into view.
- **Animated SVG path** in the pipeline section — 2400-unit dashed stroke draws over 6 seconds from FASTQ to Dossier with arrow marker.
- **Module cards** with stagger reveal, 3D-ish tilt rotation `-0.6deg` + 8px hard ink shadow on hover, and a chartreuse radial glow halo behind. Serial-number badge rotates 360° on hover.
- **Tier "T·0X" mega numerals** — outlined-only at 18% opacity, becoming 4px stroke at 40% opacity on section hover.
- **Manifesto blob animation** — mulberry + cyan organic shapes morphing through 4 keyframes over 12–16s, organic-blob border-radius animation.

## Aesthetic system

| | |
|---|---|
| **Cream paper** | `#F5EFE0` (slight yellow shift) |
| **Mulberry** | `#3D0E40` (primary tier 1 + signage) |
| **Electric chartreuse** | `#D9F25C` (signature accent, T2) |
| **Hot cyan** | `#00D4E1` (T3) |
| **Hot pink** | `#FF3D7F` (callouts, dossier highlight) |
| **Ink** | `#0A0A0A` |
| **Display** | [Bodoni Moda](https://fonts.google.com/specimen/Bodoni+Moda) — variable italic, opsz 6–96, weight axis tied to scroll velocity |
| **Chunk display** | [Unbounded](https://fonts.google.com/specimen/Unbounded) — for tier labels, marquee |
| **Body** | [Lora](https://fonts.google.com/specimen/Lora) — characterful serif with italic |
| **Mono** | [Major Mono Display](https://fonts.google.com/specimen/Major+Mono+Display) — ornaments, compass, mandala inner ring |

## How this differs from the other two maximalist treatments

| | **Editorial Issue 01** | **Systems Manual № 007** | **Causal Atlas Vol. III** *(this)* |
|---|---|---|---|
| Voice | Printed magazine | Engineering manual | Kinetic poster series |
| Paper | Cool cream | Warm ochre | Cream with green/cyan washes |
| Type system | Fraunces italic + Newsreader + DM Mono | Big Shoulders Display + Stencil + IBM Plex | **Bodoni Moda + Unbounded + Lora + Major Mono** |
| Accent | Hot red on cream | Oxblood + mustard + cyan on ochre | **Mulberry + chartreuse + cyan + hot pink** |
| Animation density | Reveal-on-scroll | Reveal + grain | **Heavy** — mandala spinning, conic gradient rotating, variable-font scroll, typer animation, count-ups, SVG path draw, blob morphs |
| Cursor | Red dot + ring | Crosshair + coords | Chartreuse blob + 3-stage trail |
| Layout signature | 460px italic numerals in red blocks | 25 stamped catalog cards | **Spinning 600×600 typographic mandala** |
| Cover | Stacked H1 + red splash | Mission patch SVG + schematic grid | Variable-axis kinetic headline + mandala |

Three committed, fundamentally different aesthetic vocabularies pointed at the same content. Pick the one that matches the room you're walking into.

## Audio

Every section headline and every module card (both **name** and **subtitle**) is a clickable audio trigger. Voices: Ava Multilingual Neural (edge-tts).

- **▷** marker appears before each clickable title
- **▶** pulses on the currently-playing title
- A **"now playing" chip** slides in from the bottom-left with the current label + animated EQ bars; `×` button stops playback
- An **audio · on/off toggle** lives in the top strip — pulses chartreuse when active. First click on any title auto-enables audio.
- Clicking the active title again pauses it.

### Audio map

| Section / module | File | Trigger |
|---|---|---|
| Cover headline `Causal Atlas of 25 Modules` | `audio/overview.mp3` | h1 |
| `Ask Causion.` | `audio/causion.mp3` | h2 |
| Tier 1 `Beyond correlation.` | `audio/t1.mp3` | h2 |
| Tier 2 `Ten production workflows.` | `audio/t2.mp3` | h2 |
| Tier 3 `Where the data enters.` | `audio/t3.mp3` | h2 |
| Pipeline `FASTQ → FDA-ready dossier.` | `audio/workflow.mp3` | h2 |
| Manifesto (3 lines) | `audio/thesis.mp3` | h2 ×3 |
| 25 module cards | `audio/modules/{slug}.mp3` | `.name` + `.name-sub` each |

Slug mapping notes: card text is shortened for the kinetic layout (`DAG Builder`, `GWAS · MR`, `Centrality`, `SIGNOR`, `CRISPR · Amplicon` etc.), but each `data-audio` attribute points to the full-name slug that matches the existing module narrations (`causal_dag_builder`, `gwas_mendelian_randomization`, `centrality_calculator`, `signor_causality`, `crispr_targeted_amplicon`).

## Contents

| File | |
|---|---|
| `index.html` | Self-contained single page — open in any browser |
| `audio/` | 7 section MP3s + `modules/` 25 module MP3s (Ava Neural · edge-tts) |
| `README.md` | This file |

## Preview

```bash
open "/Users/mohamadammarayass/Desktop/Ayass _ Strategic Planning/BiRAGAS Causal Atlas/index.html"
```

Or serve locally:

```bash
cd "/Users/mohamadammarayass/Desktop/Ayass _ Strategic Planning/BiRAGAS Causal Atlas"
python3 -m http.server 8000
# → http://localhost:8000/
```

## Live URL

**https://mayasss-gif.github.io/BiRAGAS-Causal-Atlas-III/**

## Deployment commands used (for reference)

```bash
cd "/Users/mohamadammarayass/Desktop/Ayass _ Strategic Planning/BiRAGAS Causal Atlas"
git init && git add . && git commit -m "Initial: BiRAGAS Causal Atlas Vol. III"
gh repo create mayasss-gif/BiRAGAS-Causal-Atlas-III --public --source=. --push
gh api repos/mayasss-gif/BiRAGAS-Causal-Atlas-III/pages --method POST \
  -f source[branch]=main -f source[path]=/
```

Suggested URL: `https://mayasss-gif.github.io/BiRAGAS-Causal-Atlas-III/`

## Performance notes

- All animations use `transform` / `opacity` (GPU-accelerated). No layout-thrashing properties animated.
- `requestAnimationFrame` for cursor + scroll-velocity loop.
- IntersectionObserver for reveals + counters.
- Mandala uses pure SVG `textPath` — no canvas, no JS animation library.
- Conic-gradient is CSS-only at 120s rotation — negligible CPU.
- Variable font axis change is debounced through the velocity smoothing.

## Notes

- Content derived from the live Technical Playbook + `modules.json`.
- 25 modules preserved verbatim with their assay / method / function.
- No audio. The motion is the performance.
