# Hosted Deploy Preflight

Status: `ready_for_provider_deployment`
Production ready: `False`
Build: `build_quote_intake_demo_2ef739047aad`
Package: `artifacts/build_quote_intake_demo_2ef739047aad/hosted-app`

## Checks

- PASS: build selected
- PASS: package-manifest.json exists
- PASS: deployment-plan.json exists
- PASS: backend/Dockerfile exists
- PASS: backend/railway.json exists
- PASS: backend/app.py exists
- PASS: backend/migrations/000_isolation.sql exists
- PASS: backend/migrations/001_init.sql exists
- PASS: frontend/Dockerfile exists
- PASS: frontend/vercel.json exists
- PASS: frontend/package.json exists
- PASS: frontend-npm-test.log exists
- PASS: frontend-npm-build.log exists
- PASS: scripts/deploy-plan.sh exists
- PASS: scripts/check_launch_readiness.py exists
- PASS: scripts/validate-live-evidence.py exists
- PASS: live-evidence-template.json exists
- PASS: hosted deployment tier is supported
- PASS: Railway Serverless setting confirmed for sleeping API tier
- PASS: shared Postgres role/schema isolation confirmed
- PASS: hosted app local package evidence exists
- PASS: Vercel CLI available
- PASS: Vercel CLI authenticated
- PASS: Railway CLI available
- PASS: Railway CLI authenticated
- PASS: PRODUCT_DATABASE_URL configured
- PASS: INKPASS_URL configured with https
- PASS: INKPASS service API key configured
- PASS: PRODUCT_ALLOWED_ORIGINS configured without wildcard

## Missing For Hosted Deploy

- none

## Next Commands

1. `cd artifacts/build_quote_intake_demo_2ef739047aad/hosted-app && bash scripts/deploy-plan.sh`
2. `railway status --json`
3. `vercel whoami`
4. `configure Railway env: PRODUCT_ENV, PRODUCT_DATABASE_URL, PRODUCT_ALLOWED_ORIGINS, INKPASS_AUTH_MODE, INKPASS_URL, PRODUCT_INKPASS_SERVICE_API_KEY`
5. `configure Vercel env: NEXT_PUBLIC_PRODUCT_API_URL, NEXT_PUBLIC_SITE_URL, NEXT_PUBLIC_INKPASS_CLIENT_SLUG, NEXT_PUBLIC_POSTHOG_PROJECT_TOKEN`
6. `cd artifacts/build_quote_intake_demo_2ef739047aad/hosted-app && python scripts/validate-live-evidence.py <live-evidence.json>`
