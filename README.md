# Japan Luggage Check

Free, unofficial checker for Japan travelers: **will my suitcase fit on the Shinkansen** (oversized-baggage rule by line) and **what does Yamato TA-Q-BIN luggage forwarding cost** (any prefecture pair or to an airport) at Yamato's current cash and cashless rates (revised 2025-10-01).

- Full app and API (Vercel): https://japan-luggage.vercel.app
- Checker (GitHub Pages): https://akiba-labs.github.io/japan-luggage/
- API: `GET/POST /api/check`, `GET /api/rules`, `/openapi.json`, `/llms.txt`, `/.well-known/ai-plugin.json`
- Share pages: `/r?l=75&w=50&h=30&kg=22&f=tokyo&t=kyoto&line=tokaido` with `/og` cards
- MCP: `japan_luggage_check` on https://free-agent-tools.vercel.app/mcp

Free, no key, CORS open. Educational estimate, not affiliated with Yamato, JR or any airport.

```
npm install
npm test
npm run dev
npm run build
npm run build:pages
```

`npm run build` is the Vercel app (checker, JSON API, share pages). `npm run build:pages` writes a static `out/` for GitHub Pages and checks that internal links and assets resolve under `/japan-luggage`. Server routes stay in the repo; the Pages script only moves them aside for that build.

GitHub settings: **Settings → Pages → Build and deployment → Source: GitHub Actions**. Pushes to `main` deploy with `.github/workflows/pages.yml`. The copy-paste steps for the other tool repos are at the top of `scripts/build-pages.mjs`.

MIT licensed.
