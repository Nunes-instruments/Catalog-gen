# NUNES V4.7 Catalogue Studio — staging status

This branch is a **staging branch**, not a complete application upload or deployment.

The requested application is an existing Windows Flask service. Its PDF workflow is:

1. Choose Catalogue (Itron-style) or Mini Catalogue (Leak Testing-style).
2. Select products from the connected Google Sheet or existing product history.
3. Fetch or research product details and approved images.
4. Review and correct details.
5. Generate and download the matching PDF template.

IndiaMART publishing is intentionally excluded from the intended V4.7 interface.

## Security

Keep .env, credentials, Google service-account JSON, IndiaMART sessions, local product records, output PDFs, and logs out of Git. This repository is **public**. No Windows automation credentials should be added here.

## Hosting

Vercel can host a web UI but cannot run the persistent Windows Playwright/Ollama worker. A secured authenticated API/worker bridge and explicit access control are needed to support real research and PDF generation. Do not redirect Vercel directly to an unauthenticated temporary Cloudflare Quick Tunnel.

## Outstanding

- Upload the complete vetted source tree and PDF template assets; this branch does not yet contain them.
- Adapt/deploy the web UI.
- Configure authentication, durable job handling, and Windows worker.
- Verify full Catalogue and Mini Catalogue PDF workflow with real approved data.

Preserve `main` until those steps pass end-to-end testing.
