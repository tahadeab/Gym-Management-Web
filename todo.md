# Project TODO

- [x] Define database schema for members, subscriptions, payments, attendance, trainers, classes, bookings, PT packages, PT assignments, and PT sessions
- [x] Add financial and operational query helpers with date-range filters
- [x] Add tRPC procedures for dashboard KPIs and analytics
- [x] Add XLSX export for financial reports and member data
- [x] Build bilingual Arabic/English dashboard with persistent RTL/LTR language switching
- [x] Build member management with search, filters, subscription status, create, and edit flows
- [x] Build monthly subscription lifecycle management: create, renew, freeze, unfreeze, expiring, and expired
- [x] Build attendance check-in/check-out and daily attendance reporting
- [x] Build trainer management and trainer relationships
- [x] Build class scheduling, capacity, pricing, trainer assignment, booking, and cancellation
- [x] Build personal training packages, member assignments, session tracking, and completion flow
- [x] Add Vitest coverage for new database and router procedures
- [x] Run type checks, tests, and browser verification
- [x] Save the final checkpoint and provide the live preview and project version

## Verification follow-ups

- [x] Implement and verify member XLSX export end-to-end, including UI trigger and backend generation
- [x] Verify and complete member CRUD, search, filters, and subscription-status UI handlers
- [x] Verify subscription renew, freeze, and unfreeze lifecycle handlers and tests
- [x] Verify trainer specialties, assigned classes, and PT client relationships
- [x] Verify class scheduling, capacity enforcement, booking, and cancellation flows
- [x] Verify PT packages, assignments, session tracking, and completion flow
- [x] Add Vitest coverage for gym database helpers and tRPC procedures beyond auth
- [x] Save a final checkpoint after all verification follow-ups are complete

## Required corrections before release

- [x] Add member delete support in the backend and UI for complete CRUD
- [x] Show each member's actual subscription status in the members table
- [x] Add Vitest coverage for subscription renew, freeze, and unfreeze lifecycle logic
- [x] Refactor class cancellation to target a specific booking for a displayed class and member

## Mobile, PWA, and repository expansion

- [x] Create a native Expo mobile app project for gym members and staff
- [x] Add bilingual Arabic/English mobile navigation with persistent RTL/LTR preference
- [x] Connect mobile app to the gym tRPC/API backend with authenticated data flows
- [x] Add mobile dashboard, members, subscriptions, classes/bookings, PT, attendance, and notifications screens
- [x] Add PWA manifest, service worker, install metadata, and offline-safe app shell to gym-management-web
- [x] Verify PWA install metadata and responsive mobile behavior
- [x] Write comprehensive bilingual README documentation for the web/PWA and mobile projects
- [x] Create a separate GitHub repository and push gym-management-web with the bilingual README
- [x] Run mobile and web type checks/tests and save final checkpoints

## Release corrections

- [x] Implement real Expo navigation with multiple screens and global language/RTL state
- [x] Add and document a mobile bearer-session authentication flow for protected backend access
- [x] Perform browser verification for PWA install metadata and responsive mobile behavior after the PWA changes
- [x] Save a post-change checkpoint after mobile/PWA verification

## Mobile implementation completion

- [x] Replace placeholder Expo Members, Subscriptions, Classes, PT, Attendance, and Notifications views with production data-driven screens
- [x] Run final mobile TypeScript validation after data-driven screen integration
- [x] Save final cross-platform checkpoint after mobile implementation completion

## Final documentation and release verification

- [x] Rewrite the web/PWA README with complete English setup, architecture, features, API, environment, testing, deployment, and Arabic support documentation
- [x] Rewrite the mobile README with Expo setup, API configuration, bearer authentication, bilingual behavior, and verification instructions
- [x] Update the desktop README with complete build, test, bilingual, SQLite, and release instructions
- [x] Add MIT license files to the web and desktop repositories and verify the mobile license
- [x] Run final web, mobile, and desktop checks and record any limitations honestly
- [x] Save a final checkpoint after documentation and verification changes

## Final verification findings

- [x] Document that the desktop repository has no configured installer/package build script and provide the supported source-release procedure
- [x] Record final verification limitations: ADMIN_PASSWORD must be set for production, mobile token entry is transitional, and native push delivery is not configured
