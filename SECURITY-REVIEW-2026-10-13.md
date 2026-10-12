# Security review — 2026-10-13

Prepared by i729. This review records tested source changes; it is not a certification of the deployed service.

## Change

Disable the project-wide npm force setting and update compatible dependencies, including Vitest. Keep framework, stylesheet and Wix platform major versions unchanged until their migrations can be tested.

## Validation

Lockfile audits completed; compatible manifest changes reviewed. Full Wix build and hosted CMS authorization tests remain outstanding.

## Dependency audit

Counts refer to package findings across the complete locked dependency tree, including tooling; they are not counts of distinct exploitable production vulnerabilities.

| Package project | Before | After | Remaining critical | Remaining high |
| --- | ---: | ---: | ---: | ---: |
| win-stats-app | 71 | 36 | 4 | 25 |

## Required before rollout

Known dependency findings remain, including critical alerts in the pinned Astro/Wix/tooling tree. Do not treat this repository as cleared for production based on this audit. Wix CMS/member collection permissions and hosting/runtime configuration are external and were not available to verify. No supported complete Wix build or major-version migration was performed.

## Scope

Source and locally fetched Git branches/tags/available pull-request heads were inspected. Private production settings, actual database policies, deployed binaries, backup stores, and third-party service permissions were not changed. Current-source cleanup does not remove data from Git history, existing forks, cached copies, or previously downloaded assets. Sensitive values are intentionally omitted.
