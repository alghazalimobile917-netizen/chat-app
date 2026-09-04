# Chat App — Independent Deployment

This package is prepared as a starting point for running the project outside Manus.

## 1. Requirements

- Node.js 20+ (recommended)
- npm 10+
- Git (recommended)
- A free hosting account such as Vercel for the web app

## 2. Install locally

Open a terminal in this folder:

```bash
npm install
npm run dev
```

Then open the local address shown by Vite (normally http://localhost:5173).

## 3. Production build

```bash
npm run build
```

If the project uses a server package/script, use the scripts shown by:

```bash
npm run
```

## 4. Important: Manus services

The original project may still contain integrations with Manus services (authentication,
file storage, AI, speech-to-text, maps, etc.). Those services cannot be made independent
merely by removing the Manus runtime plugin.

Before production launch, search the project for:

- `manus`
- `forge`
- `oauth`
- `S3`
- environment variables beginning with `VITE_` or server-side secrets

Replace each Manus-dependent service with an independent provider.

## 5. Temporary free hosting — Vercel

Recommended path:

1. Create a GitHub repository and upload this project.
2. Sign in to Vercel with GitHub.
3. Import the repository.
4. If Vercel detects Vite/React, accept the detected settings.
5. Build command: `npm run build`
6. Output directory: usually `dist`
7. Add required environment variables under Project Settings → Environment Variables.
8. Deploy.

Vercel will provide a temporary address such as:

`your-project.vercel.app`

You can later attach your official domain without rebuilding the application.

## 6. If the project has a backend/database

Do NOT put database passwords or API secrets inside frontend files.

Use environment variables and an independent database/backend provider.
The exact variables depend on the project and must be identified before launch.

## 7. Recommended migration order

1. Run the project locally.
2. Identify all Manus dependencies.
3. Move authentication to an independent provider.
4. Move database/storage to independent services.
5. Move AI and speech services to independent APIs.
6. Test messages, images, uploads, permissions and admin functions.
7. Deploy to Vercel.
8. Test the temporary domain.
9. Connect the official domain at launch.

## 8. Notes

This ZIP is intentionally conservative: it does not pretend that Manus-specific
backend services have been replaced when their credentials/configuration are not known.
The next migration step should be based on the actual source files and environment
configuration.
