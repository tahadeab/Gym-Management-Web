# PulseForge Desktop

The supported desktop application is the Electron wrapper around the **same production Web build** used by PulseForge Web. The Electron wrapper is intentionally thin: it opens the Web UI, starts the production Node server when running locally, and preserves the Web application's bilingual Arabic/English interface, RTL/LTR behavior, theme controls, tRPC APIs, authentication flow, reports, exports, and responsive layout.

## Commands

```bash
pnpm desktop:check   # Validate the Electron entry
pnpm desktop:test    # Electron smoke test for Web startup, RTL, and routes
pnpm desktop:dev     # Build Web and open it in Electron
pnpm desktop:dir     # Build an unpacked desktop directory
pnpm desktop:win     # Build the Windows NSIS installer on Windows or CI
```

## Architecture

The desktop app uses the Web repository as its source of truth. It does **not** use the legacy `GYM_SYSTEM-2.0` SQLite dashboard for the modern product shell. Business data is served by the Web server and its configured database/API layer. The older Electron repository remains available for historical/source-release compatibility, but it is not the target UI for the modern PulseForge Desktop conversion.

For a hosted deployment, set `PULSEFORGE_WEB_URL` before launching Electron. Without that variable, Electron starts the local production Web server from the packaged application and opens the local URL. Authentication continues to use the Web OAuth flow; a real authenticated session is required to test protected member, finance, class, PT, and attendance operations.

## Release

Windows NSIS generation must run on Windows or GitHub Actions. The resulting installer is produced by `electron-builder` and should be distributed through the GitHub Release assets rather than committed to the repository. Temporary `release/` output is ignored by Git to avoid committing large Chromium binaries.
