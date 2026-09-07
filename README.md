# Angular Kickstart — Enterprise Frontend Foundation

> Historical Angular application preserved as evidence of frontend foundations, testing, build tooling and incremental modernization.

## 30-second read

This repository started as an Angular application/e2e foundation. The 2026 modernization keeps the historical implementation intact while adding a clearer engineering contract around **build reproducibility, testability, dependency risk and migration decisions**.

**Primary question:** how do you modernize an aging frontend without breaking existing behaviour?

## What this demonstrates

- Angular application structure and routing
- TypeScript/RxJS fundamentals
- component and service boundaries
- browser/application testing
- legacy build-tool constraints
- dependency and lockfile drift
- incremental modernization rather than a destructive rewrite

## Run it online

### Browser IDE — recommended

**[Open in GitHub Codespaces](https://codespaces.new/MountainBridge/Angular-kickstart)**

This is the full project runtime: repository + terminal + forwarded application port.

### Browser playground

**[Open in StackBlitz](https://stackblitz.com/github/MountainBridge/Angular-kickstart)**

StackBlitz is useful for browser-based inspection, but this historical Angular version may require dependency/runtime adjustments. Codespaces is the authoritative run path for this repository.

## Run locally

```bash
npm install --legacy-peer-deps
npm start
```

Then open `http://localhost:4200/`.

## CI / evidence

GitHub Actions validates installation, build and tests against the historical dependency graph. The workflow is intentionally explicit about legacy constraints instead of silently upgrading the application.

## Failure modes worth discussing

| Failure | Engineering question |
|---|---|
| dependency drift | Can the old application still be reproduced? |
| breaking Angular upgrade | What existing journeys are at risk? |
| RxJS behaviour change | Which streams and subscriptions need regression coverage? |
| browser compatibility | What is the supported execution matrix? |
| build-tool incompatibility | Do we migrate tooling first or the framework first? |

## Modernization path

```text
Historical Angular app
        ↓
Reproduce current behaviour
        ↓
Capture journeys + regression evidence
        ↓
Stabilize CI / dependencies
        ↓
Introduce modern Angular patterns incrementally
        ↓
Measure blast radius
        ↓
Retire legacy tooling safely
```

## Interview prompts

1. What would you test before upgrading Angular?
2. How would you identify the blast radius of an RxJS/framework upgrade?
3. When is incremental migration safer than a rewrite?
4. How would you make browser tests deterministic?
5. What evidence would convince you that the upgrade did not break existing journeys?

## Related engineering casebook

See the broader engineering standards and modernization roadmap in `MountainBridges`.
