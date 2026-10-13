# 4 Leg Finder

Find the lowest-priced **single-ticket** four-segment itinerary through Taipei:

`origin country → TPE → destination city → TPE → origin country`

The origin and final airport may differ, as long as they are in the same country. Results must be priced as one multi-city ticket, not as four independent one-way tickets.

## Structure

- `apps/web`: Next.js search interface
- `apps/api`: Fastify API and flight-provider adapter boundary
- `packages/core`: itinerary rules and candidate validation

## Run locally

```bash
pnpm install
pnpm dev
```

The initial API returns a clearly marked sample itinerary. Replacing the provider adapter with a GDS/NDC source is required for live prices.
