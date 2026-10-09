# NUNES Catalogue Studio V4.7 — Release Gate

## Verified 2026-10-09

- Source repository: `Nunes-instruments/Catalog-gen`, main commit `8c80c099f288ac9fc4af5773ccb1dfa5a3e5be31`.
- Vercel preview deployment: `dpl_8iet96xZoAQQS1J16joYVePVzuU7` (READY), preview `https://nunes-indiamart-automation-4q9j7sjq8-instruasia-6728.vercel.app/`.
- Build logs show successful clone, Python dependency installation, and deployment.
- Uploaded `templates/index.html` still uses title `NUNES Product Research & IndiaMART V4.1` and lacks the V4.7 catalogue-first UI.
- The repo contains Windows-dependent Flask, Playwright and local file workflows.

## Required before production promotion

1. Replace V4.1 interface with vetted V4.7 Catalogue/Mini Catalogue first selector and review workflow.
2. Disable IndiaMART publishing actions in the catalogue-only interface and corresponding public endpoints.
3. Keep credentials, Google Sheet tokens, user sessions and runtime data outside public Git.
4. Verify Flask routes under Vercel runtime. A successful build is not proof of runtime operation.
5. Use secure authenticated remote worker or move stateless PDF generation to cloud functions with appropriate persistent object storage; do not expose Windows PC directly to the public Internet.
6. Validate full catalogue and mini catalogue PDF output against the Itron and Leak Testing references, using approved data and images.
7. Confirm remote access from a second computer and protect business data with authentication.
8. Only then deploy to production and verify the production URL.

The currently deployed preview is **not** a verified working Catalogue Studio V4.7.
