# Hosted Deployment Execution

Status: `hosted_launch_ready_pending_production_evidence`
Passed: `True`
Production ready: `False`
Build: `build_quote_intake_demo_2ef739047aad`
Package: `artifacts/build_quote_intake_demo_2ef739047aad/hosted-app`
Mutation allowed: `True`
Provider commands executed: `True`
Web URL: `https://quote-intake-demo-web.vercel.app`
API URL: `https://quote-intake-demo-api-production.up.railway.app`

## Steps

- PASS `hosted_deploy_preflight`: ready_for_provider_deployment
- PASS `railway_deploy_api`: passed
- PASS `vercel_deploy_web`: passed
- PASS `hosted_launch_readiness`: passed

## Missing For Live Product

- ingest accepted production evidence before claiming production_ready
- return hosted InkPass auth, Postgres persistence, CORS, and production CI evidence

## Next Commands

1. `PYTHONPATH=src python -m product_factory_runtime --db data/factory.sqlite3 --artifacts artifacts run-hosted-deploy-preflight build_quote_intake_demo_2ef739047aad`
2. `PYTHONPATH=src python -m product_factory_runtime --db data/factory.sqlite3 --artifacts artifacts execute-hosted-deploy build_quote_intake_demo_2ef739047aad --allow-provider-mutation`
3. `cd artifacts/build_quote_intake_demo_2ef739047aad/hosted-app && python scripts/check_launch_readiness.py --web-url https://quote-intake-demo-web.vercel.app --api-url https://quote-intake-demo-api-production.up.railway.app --json`
4. `PYTHONPATH=src python -m product_factory_runtime --db data/factory.sqlite3 --artifacts artifacts certify-deployable-product build_quote_intake_demo_2ef739047aad --web-url https://quote-intake-demo-web.vercel.app --api-url https://quote-intake-demo-api-production.up.railway.app`
