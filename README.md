# Ashmit Gupta — Portfolio

A circuit-board-themed personal portfolio site — backend systems and embedded hardware, laid out like a PCB.

## Live Demo

Deploy `index.html` (renamed from `ashmit-portfolio.html`) to GitHub Pages, or open it directly in a browser.

## Features

* **Animated Circuit Hero:** An SVG trace draws itself on load, connecting a central chip to nodes labeled with core skills (C++, Flask, SQL, Arduino).
* **Scroll-Linked Timeline:** Education and experience laid out as a PCB trace that fills in as you scroll.
* **Skills as a Bill of Materials:** Every skill from the resume rendered as a component chip, grouped by category (Languages, Core CS, Frameworks, Databases & Tools, Hardware).
* **Live Coding Stats:** Real-time data pulled from:
  * GitHub REST API — public repos, followers, total stars, top language.
  * LeetCode (community API) — total solved, easy/medium/hard breakdown, contest rating.
  * AtCoder (community API) — problems solved, solve-count rank.
* **Projects Grid:** Library Management API, Task Manager API, and the Smart PCM Decoder & Audio System, each with tech tags and repo links.
* **Achievements & Leadership:** DSA problem count, competition results, certifications, NCC and DevComm roles.
* **Responsive Design:** Full mobile layout with a collapsible nav menu.

## Technologies Used

* **HTML5** — semantic structure.
* **CSS3** — custom properties, CSS Grid/Flexbox, keyframe animations, scroll-driven progress bar.
* **JavaScript (Vanilla)** — DOM manipulation, IntersectionObserver for scroll reveals and active-nav highlighting, async fetch for live stats.
* **REST APIs** — GitHub REST API, plus community LeetCode and AtCoder stats endpoints (see note below).
* **Google Fonts** — Space Grotesk, Inter, IBM Plex Mono.
* **Devicon** — technology icons in the skills section.

## A Note on Live Stats

GitHub has an official public API, so those numbers are always reliable. **LeetCode and AtCoder have no official public API** — the site uses community-maintained endpoints instead:

| Platform | Endpoint used | Fallback |
|---|---|---|
| LeetCode (solved counts) | `leetcode-stats-api.herokuapp.com` | `leetcode-stats.tashif.codes` |
| LeetCode (contest rating) | `alfa-leetcode-api.onrender.com` | `leetcode-stats.tashif.codes` |
| AtCoder | `kenkoooo.com/atcoder/atcoder-api` | — |

These can occasionally go down or change shape without notice. If a stat shows "n/a", the site is working correctly — it just means that particular service didn't respond. No user action needed, but if an endpoint disappears permanently, that section will need a new API swapped in.

To point these at a different account, search for the relevant `const user = '...'` line inside the `<script>` block near the bottom of `index.html`.

## Local Setup

1. Clone the repository:

   ```
   git clone https://github.com/ashmitgupta637/ashmitgupta637.github.io.git
   ```

2. Navigate to the project directory:

   ```
   cd ashmitgupta637.github.io
   ```

3. Make sure `resume.pdf` sits in the same folder as `index.html` — the "Download Resume" buttons link to it directly.

4. Open `index.html` in your web browser.

## Author

**Ashmit Gupta**

* GitHub: [@ashmitgupta637](https://github.com/ashmitgupta637)
* LinkedIn: [Ashmit Gupta](https://www.linkedin.com/in/ashmit-gupta-a619a6285/)
* LeetCode: [AshNova](https://leetcode.com/AshNova/)
* AtCoder: [ashmit_gupta637](https://atcoder.jp/users/ashmit_gupta637)
