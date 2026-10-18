# Wortschatz – German flashcard app (PWA)

Offline-first German flashcard app. Everything lives in `index.html` (vanilla JS, no build step).
Hosted with GitHub Pages from the `main` branch, root folder. Files that must stay at the repo root:
`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.

## Rules from the owner (always follow)
- Make small, surgical edits. Never rewrite the whole app and never remove existing features.
- Never wipe or break saved data: localStorage key `wortschatz.v1` (cards, settings, review log). Keep it backward compatible.
- Before adding new features, give the owner a short bullet summary of what you will add.
- Never hard-code API keys. Keys are entered by the user in Settings and stay on their device.

## How it works
- Study engine: SM-2 spaced repetition; Learn tab (explanations) and Quiz tab (several quiz types); practice sessions do not change the schedule.
- Adding cards: manual form, paste-many box, "Look up words", "Add cards online" generator.
- AI sources: Gemini, ChatGPT and Claude API keys (Settings > AI and word sources) with automatic fallback; plus Wiktionary dictionary lookup.
- `sw.js` is network-first: online = newest files, offline = saved copy. Do not remove the offline fallback.

## Deploying
Commit to `main` and push. GitHub Pages redeploys in 1-2 minutes; the phone app updates the next time it is opened online.
