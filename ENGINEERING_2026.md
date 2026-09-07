# 2026 Engineering Evidence

This repository is intentionally preserved as a historical Angular foundation rather than silently rewritten.

## What this proves

- Angular application structure and routing
- TypeScript/RxJS-based frontend development
- Build and test automation
- A reproducible CI path for the historical stack

## Modernization boundary

The original application is the evidence of the earlier engineering decision. Modern platform concerns—typed API contracts, accessibility, observability, security, containerized environments, and current Angular patterns—belong in the portfolio's newer flagship implementations.

## Reproduce

```bash
npm ci --legacy-peer-deps
npm run build -- --configuration production
npm test -- --watch=false --browsers=ChromeHeadless
```

CI executes the same core validation. See `MountainBridges` for the portfolio-level modernization roadmap and trend radar.
