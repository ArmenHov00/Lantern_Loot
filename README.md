# Lantern Loot

Asian fantasy 5×5 cluster slot using fictional credits only. Plain HTML, CSS and vanilla JavaScript with bundled original artwork.

## Play locally

Run `python3 -m http.server 8000` from this folder, then open http://localhost:8000. No build or dependency installation is required.

## Deploy to Netlify

Import this repository. Production branch: `main`. Leave the build command empty. Publish directory: `.`. A Netlify Drop deployment is separate; link its existing project to this repository to enable automatic updates.

## Controls and rules

Use +/− to change the bet, select Classic/Turbo/Max, then press the circular arrow or Space. Five or more orthogonally connected symbols pay; cascades use ×1/×2/×3/×5. Initial 3+ Scatters trigger 10 free spins. See RULES.md and the in-game information panel for details. Start balance is 10,000 fictional credits. Pending saved rounds recover once on reload. Reset is in Settings.

## Latest presentation

Mobile uses a taller board, compact controls and Safari safe-area/visible-viewport handling. Winning symbols burst into compact fireworks. All modes share celebration pacing; every third win adds a 4.8-second inferno. The final celebration starts 160 ms after the last winning-cell explosion begins, overlapping the sparks.

## Development and verification

Source is in src/; original PNG artwork is in assets/. Node.js runs tests/*.cjs; Python runs tests/package.py after build.py. `python3 build.py` produces a standalone embedded HTML and source ZIP in the parent deliverables folder.

Automated tests cover rules, accounting, recovery, reels, mobile geometry, effect cleanup and celebration overlap. They use virtual clocks and DOM/Canvas doubles. Real Safari/browser visual inspection remains outstanding; see FLOW_UPDATE.md and the included reports. Audio uses synthesized placeholders. This is an entertainment prototype, not certified gambling software; simulation estimates are not guarantees.
