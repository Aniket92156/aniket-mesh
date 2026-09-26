# Aniket-mesh- https://match-and-mesh.lovable.app/ 
Cloud storage looks simple from the outside, but underneath it's solving a hard problem: disks fail, networks drop, and data can quietly corrupt — yet users expect their files to just always be there. We built Vault to actually implement that guarantee ourselves, rather than just consuming it as a black box from AWS or Google Cloud. It forced us to reason about real trade-offs — consistency vs. availability, replication cost vs. durability, speed of repair vs. correctness — and prove those decisions live, in front of a judge, instead of just describing them on a slide.
<img width="989" height="615" alt="image" src="https://github.com/user-attachments/assets/42331da2-dab4-46e4-963b-5da518e3d4bd" />

#Vault interactive website

## Goal
Turn the two supplied proposals into one polished, high-fidelity Vault experience. Keep the proposal’s technical facts, use the supplied dark operations-console visual language, and make the central product demo genuinely interactive rather than presenting a static document.

## What I’ll build
- Replace the blank home page with a responsive Vault operations console.
- Lead with live system health, capacity, replication, and integrity indicators.
- Add an object workflow: upload a file, choose replication factor 1–4, inspect generated metadata/checksum, download it, and delete it.
- Add node controls: register a node, take nodes offline or recover them, simulate corruption, run repair, and rebalance object placement.
- Add an activity stream showing upload, failure, integrity, repair, and rebalance events.
- Preserve the proposal material in concise architecture, mechanism, API, scope, build-plan, team, and demo views instead of long static sections.
- Include clear empty, active, warning, failure, repair, and success states; keep the simulation in the browser so the experience works immediately without setup.

## Visual direction
- Dense, professional distributed-systems console using the supplied navy, graphite, mint, amber, coral, and blue palette.
- Space Grotesk for hierarchy, Inter for UI copy, and IBM Plex Mono for IDs, checksums, statuses, and API labels.
- Compact sidebar navigation, strong data hierarchy, restrained motion, sharp diagrams, and responsive mobile layouts.

## Technical details
- Implement as a TanStack Start React page with typed local simulation state.
- Use semantic design tokens in the global stylesheet and reusable UI primitives for all controls.
- Compute real SHA-256 checksums in-browser for uploaded files where supported.
- Keep proposal and simulation data deterministic, with no invented production claims.
- Add complete page metadata and preserve accessibility for keyboard and screen-reader use.

## Verification
- Check the upload → replication → node failure → successful retrieval → repair flow end to end.
- Check corruption detection, recovery, node registration, and rebalancing.
- Verify desktop and mobile layouts, console/runtime errors, and the final preview build.
