# SAL Career Pathing Tool

GitHub-ready frontend repository, prepared 21 October 2026.

## Upload to GitHub

1. Extract this ZIP.
2. Create a GitHub repository (a private repository is recommended for SAL role structures).
3. Choose **Add file → Upload files**.
4. Upload the **contents** of `SAL-Career-Pathing-GitHub`: `public/`, `netlify.toml`, this README, and the other files. Do not upload the ZIP itself. Keep folders intact.
5. Commit the upload. `netlify.toml` must be at the repository root.

## Publish through Netlify

Connect the GitHub repository to Netlify as an existing project.
- Base directory: leave blank.
- Build command: leave blank; the frontend is already built.
- Publish directory: `public` (also set in `netlify.toml`).

Use the assigned HTTPS `*.netlify.app` URL. No API key or app installation is required for this frontend package. This repository is for Netlify hosting, not GitHub Pages: GitHub Pages does not execute the supplied Netlify backend proxy rules.

## Included

SAL branding, all current function catalogs, Corporate Leadership restricted to CEO direct reports, separate Strategy & Growth function led by Deputy CEO, automatic pathway selection without a pathway-style dropdown, flight waypoints and alternate route, timings, competency comparison, 70–20–10 development plans, guided text/voice coach, document uploads, print/PDF and Outlook drafts.

## Backend and private data

This repository hosts the frontend only. Its `public/_redirects` file connects participant saves and uploads to the existing SAL backend:
https://sal-career-pathing.srijithnair.chatgpt.site

**Keep that backend active. This is not a standalone backend or database migration to Netlify.** There are no employee records, secrets or admin credentials in this download. Records remain in the existing private backend, accessible to the authorized owner at:
https://sal-career-pathing.srijithnair.chatgpt.site/admin

The Netlify `/admin` address redirects to that owner-protected page. Participants do not need owner sign-in. Moving to another origin starts a new browser session; browser-local progress is not transferred automatically. Prior backend records remain available.

Custom domains require a separate backend origin configuration. Use the default HTTPS `*.netlify.app` address for this package.

## Verify after deployment

This package has not been deployed to your GitHub or Netlify account. After publishing, build a sample pathway, send a chat message, confirm the saved status, and verify the record in the owner admin page. Test an optional upload and Excel export before rollout.

The current tool passed automated role-routing, interface, session-token isolation, upload access and owner-access checks. Speech requires browser support and microphone permission. The coach uses guided career logic rather than a general-purpose AI model.

## Editing

Edit the readable `.mjs`, HTML and CSS files in `public/`, then commit. Netlify can redeploy from the connected repository. `parser.mjs` and `pdf.worker.mjs` are prebuilt document-processing assets; preserve them. Keep `_redirects` and `_headers` in `public/`.
