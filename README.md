# ColdChain Pulse

Cold-chain monitoring for MedSwift Logistics: dispatch board, telemetry alerts, QR+PIN chain of custody,
an offline-first driver PWA, and tamper-evident audit reports.

| Path | What |
|---|---|
| `docs/PRD.md` | Product requirements |
| `design/` | 7 UI mockups (`.dc.html`) + map to implementing files |
| `frontend/` | Next.js 14 + TypeScript app (mock API built in) |

## Run the frontend
```bash
cd frontend
cp .env.example .env.local     # NEXT_PUBLIC_API_MODE=mock works with no backend
npm install
npm run dev                    # http://localhost:3000
npm run typecheck && npm test
```
Mock sign-ins (password `demo1234`): `dispatch@demo.coldchain`, `driver@demo.coldchain`,
`driver2@demo.coldchain` (critical shipment), `clinic@`, `auditor@`, `admin@` (all `@demo.coldchain`).
Set `NEXT_PUBLIC_API_MODE=live` and `NEXT_PUBLIC_API_URL` to use the real backend.

> Status: written without a package install available, so it has not yet been built or tested.
> Run `npm install && npm run typecheck && npm test` first and fix anything it reports.
