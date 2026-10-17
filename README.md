# Kaifal Haal (كيف الحال؟) — Speak Their Language.

AI-powered Arabic dialect translator (Saudi, Emirati, Kuwaiti, Qatari) for English, Malayalam and Manglish input.

## Run
1. `npm install`
2. `cp .env.example .env` and set `GEMINI_API_KEY` (get one at https://aistudio.google.com/apikey)
3. `node --env-file=.env server.js`  (Node 20.6+) then open http://localhost:3000

## Structure
- `server.js` — Express server, `/api/translate` (validation, throttle, Gemini call, schema check), `/api/health`
- `public/index.html` — UI: translator, phrasebook, history/favorites (localStorage)
- `.env.example` — config template (`GEMINI_API_KEY`, `GEMINI_MODEL`, `PORT`)

## Deploy
Any Node host (Render, Railway, Fly.io, Cloud Run). Set `GEMINI_API_KEY` as a secret environment variable on the host; never commit `.env`. Start command: `npm start`.
