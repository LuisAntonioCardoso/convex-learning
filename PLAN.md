# Convex Learning Diary

Portfolio + learning project. Explore Convex top-to-bottom. Production-grade patterns. Multi-DB integration. Self-host capabilities.

## Vision

Build comprehensive showroom. Each doc page = feature exploration. Live demos. Code walkthroughs. Compare implementations (Convex vs Postgres). Learn via doing.

## Structure

```
convex-explore/
├── convex/          # Backend (Convex functions)
├── src/             # Astro + Svelte frontend
├── docs/            # Learning diary (embedded in Astro)
├── tests/           # Unit + integration tests
├── docker/          # Self-host setup
└── scripts/         # Deploy, archive, sync utilities
```

## Learning Phases

### Phase 1: Init
- [ ] Convex headless (cloud free tier)
- [ ] Astro + Svelte frontend (cloud)
- [ ] Local dev setup (`npx convex dev`)
- [ ] Deploy both

### Phase 2: Convex Basics + Docs
- [ ] Queries, mutations, schema design
- [ ] Add doc pages (live demos + code)

### Phase 3: Testing + Production Patterns
- [ ] Unit/integration tests
- [ ] Error handling, retry logic
- [ ] Doc pages for patterns

### Phase 4: Data Relationships
- [ ] 1→many, many→many, polymorphic, nested, graph
- [ ] Doc pages + compare approaches

### Phase 5: Features
- [ ] Real-time subscriptions
- [ ] Full-text search
- [ ] File uploads
- [ ] Transactions
- [ ] Batch operations
- [ ] Access control (row-level, field-level)
- [ ] Aggregations
- [ ] Background jobs (actions/scheduled)
- [ ] Webhooks
- [ ] Caching strategies
- [ ] Rate limiting
- [ ] Data validation
- [ ] Doc pages + live demos

### Phase 6: Components + Integrations
- [ ] Convex components architecture
- [ ] Auth (Convex Auth + Clerk parallel examples)
- [ ] Payments (Stripe)
- [ ] Other integrations
- [ ] Doc pages

### Phase 7: Advanced Multi-DB + Archive
- [ ] Postgres standalone implementation
- [ ] Convex ↔ Postgres sync patterns (bidirectional)
- [ ] Archive/analytics layer (Postgres = cold storage, Convex = hot)
- [ ] Doc pages + comparisons
- [ ] Performance benchmarks

### Phase 8: Polish + Self-Host
- [ ] Showroom refinement
- [ ] Self-host Convex setup (Docker/local)
- [ ] Deploy archive system
- [ ] Learning diary review + polish

## Doc Pages Roadmap

Each page = feature exploration. Live demo + code + explanation.

```
/docs/
├── 01-setup.md               # Init guide
├── 02-basics.md              # Queries, mutations, schema
├── 03-testing.md             # Unit/integration patterns
├── 04-relationships.md       # Data model types
├── 05-subscriptions.md       # Real-time
├── 06-search.md              # Full-text search
├── 07-uploads.md             # File storage
├── 08-transactions.md        # ACID guarantees
├── 09-batch.md               # Bulk operations
├── 10-access-control.md      # Row/field level
├── 11-aggregations.md        # Analytics queries
├── 12-jobs.md                # Background tasks
├── 13-webhooks.md            # External integrations
├── 14-caching.md             # Performance optimization
├── 15-rate-limiting.md       # Request throttling
├── 16-validation.md          # Schema + runtime validation
├── 17-components.md          # Modular architecture
├── 18-auth-convex.md         # Convex Auth
├── 19-auth-clerk.md          # Clerk integration
├── 20-payments.md            # Stripe integration
├── 21-postgres-standalone.md # Postgres patterns
├── 22-postgres-sync.md       # Bidirectional sync
├── 23-archive-analytics.md   # Multi-DB strategy
└── 24-self-host.md           # Local deployment
```

## Getting Started

```bash
# Phase 1: Init
npm create convex@latest
npm create astro@latest
# (follow setup guides)

# Local dev
npm run dev
npx convex dev

# Deploy
npx convex deploy
npm run build && npm run deploy
```

## Tech Stack

- **Backend**: Convex (headless)
- **Frontend**: Astro + Svelte
- **Database**: Convex (primary), Postgres (integration/archive)
- **Auth**: Convex Auth + Clerk
- **Payments**: Stripe (learning only)
- **Testing**: Vitest + integration tests
- **Deployment**: Convex cloud (free), Vercel (Astro), Docker (self-host)

## Learning Goals

1. Master Convex core (queries, mutations, subscriptions)
2. Implement all features + production patterns
3. Compare Convex vs Postgres approaches
4. Build multi-DB system (hot + cold data)
5. Deploy locally + cloud
6. Document everything via showroom

## Notes

- Learning diary embedded in Astro site
- Each phase adds doc pages + working code
- Live demos where possible
- Production-grade patterns (error handling, testing, caching)
- Portfolio-ready by end

---

**Status**: Phase 1 in progress
