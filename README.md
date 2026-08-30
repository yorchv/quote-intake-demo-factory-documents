# QuoteRivet factory documents

This repository keeps the product documents and evidence produced by Product Factory for QuoteRivet.

## Product

- Product ID: `quote-intake-demo`
- Product name: `QuoteRivet`
- Build ID: `build_quote_intake_demo_2ef739047aad`
- Architecture run: `architecture_quote-intake-demo_2ef739047aad`
- Live product: https://quote-intake-demo-web.vercel.app
- Product source: https://github.com/yorchv/quote-intake-demo

## What is here

The files retain their original factory-relative paths:

- `specs/` contains the checked product spec.
- `artifacts/architecture_quote-intake-demo_2ef739047aad/` contains the architecture, pipeline report, and architecture agent records.
- `artifacts/build_quote_intake_demo_2ef739047aad/spec/` contains spec validation and naming evidence.
- `artifacts/build_quote_intake_demo_2ef739047aad/hosted-app/` contains product documentation, agent tasks, reviews, screenshots, launch material, local verification, deployment planning, and auth provisioning evidence.
- `artifacts/build_quote_intake_demo_2ef739047aad/factory/` contains build, product creation, deployment, and lifecycle reports.
- `artifacts/build_quote_intake_demo_2ef739047aad/repository-publication/` contains source publication reports. The duplicated source package is omitted because the product source has its own repository.
- `artifacts/factory/created-products/` and `artifacts/factory/product-creations/` contain the retained creation state.

`FILES.txt` lists every published file. `MANIFEST.sha256` records its SHA-256 digest.

## Deliberate exclusions

This archive does not contain generated application source, dependency folders, virtual environments, caches, local databases, or provider credentials. The generated `.env` file is also excluded. Those files are either available in the product source repository or should never be committed.
