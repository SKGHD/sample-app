# sample-app

Reference application repo for the ArgoPlatform learning clone.

## Purpose

Demonstrates how an app team integrates with central CI workflows using one standard orchestrator workflow.

## Key Files

- `.github/workflows/argoplatform-ci.yml`
- `appInfo.json`
- `environmentInfo.json`
- `build.json`
- `build-version.json`
- `Dockerfile`

## Promotion Model

1. Enable target environment in `environmentInfo.json`
2. Run namespace action for that environment
3. Bump `build-version.json`
4. Run build action
5. Run deploy action for the target environment

## Required GitHub Setup

- Secret: `GH_PAT`
- Optional variable: `AUTO_DEPLOY_ENV`
- Environments: `dev`, `test`, `stage`, `prod`
