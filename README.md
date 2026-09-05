# aero-learning-bay

Interactive learning websites for aerospace electronics topics at Temasek Polytechnic,
built to be embedded into ThingLink virtual MRO scenarios.

Each topic is a single self-contained HTML page — no external fonts, scripts, styles or
images, and no network calls. All student data (diagnostic tier, practice answers, lab
flags, Feynman explanations, knowledge summary) stays in the student's own browser via
`localStorage`. Nothing is uploaded anywhere.

## Live topics

| Topic | Title | Modules | Embed URL |
|---|---|---|---|
| 1 | Semiconductors, Integrated Circuits & PCB | 7 | https://daniellow1987-ship-it.github.io/aero-learning-bay/topic1/ |
| 3 | Logic Circuits & Data Converters | 6 | https://daniellow1987-ship-it.github.io/aero-learning-bay/topic3/ |
| 5 | Databuses (ARINC 429 & ARINC 629) | 7 | https://daniellow1987-ship-it.github.io/aero-learning-bay/topic5/ |

## How each bay is structured

1. **Pre-flight check** — a short diagnostic that places the student at **Foundation**,
   **Developing** or **Proficient** *for each module separately*.
2. **Scaffolded modules** — concept text, interactive labs, and practice questions are
   re-pitched to the student's tier for that module. Labs use predict-then-check prompts;
   wrong answers are logged by misconception name.
3. **Feynman explanation** — the student explains each concept in plain words as if to a
   first-year apprentice; the page checks which key ideas are covered.
4. **Smart knowledge summary** — auto-built from tier, lab activity, misconceptions and
   the student's own explanations, and copyable into the ThingLink scenario.

## Embedding in ThingLink

Add an **Embed / Website** tag to the scenario and paste the topic's URL above.
The pages are served over HTTPS and are responsive, so they work inside the ThingLink
iframe on desktop and tablet.

## Repository layout

```
topic1/index.html    Topic 1 — Semiconductors, ICs & PCB
topic3/index.html    Topic 3 — Logic Circuits & Data Converters
topic5/index.html    Topic 5 — Databuses
```

Published with GitHub Pages from `main` / root. To update a topic, drop a file named
`index.html` into that topic's folder and commit to `main`; the URL never changes, so
existing ThingLink tags keep working.
