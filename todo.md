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

## New GitHub repository copy

- [x] Prepare a clean copy of gym-management-web for a new repository under the user's GitHub account
- [x] Verify README documents prerequisites, environment variables, setup, database workflow, development, production build, testing, PWA, mobile companion, and bilingual support
- [x] Verify the repository contains a project-owned MIT License
- [x] Create the new private GitHub repository and push the verified copy
- [x] Confirm the remote URL, branch, commit author configuration, and repository contents

## UX, CI, and reusable workflow enhancements

- [x] Verify the current GitHub repository names and update README links to the active repositories
- [x] Add interactive toast feedback for successful and failed member operations and other important mutations
- [x] Add a persistent Light/Dark mode toggle with accessible labels and correct theme tokens
- [x] Add GitHub Actions workflows for type checks, tests, and production build verification
- [x] Create and validate a reusable gym-management workflow skill using skill-creator guidance
- [x] Run final checks, save a checkpoint, and push the updated copy to the active repository

## Gap remediation from final review

- [x] Add toast success/error handling for PT package, assignment, session, and attendance mutations
- [x] Refactor dashboard shell and major surfaces to semantic theme tokens for consistent Light/Dark rendering
- [x] Save a new checkpoint after remediation and push all UX/CI changes to the active GitHub repository

## Trainer and room scheduling enhancement

- [x] Review the existing trainers/classes data model and identify missing room scheduling capabilities
- [x] Add room management and conflict-aware class scheduling where supported by the current schema
- [x] Improve trainer management UI with operational fields and interactive feedback
- [x] Verify Toast notifications and Light/Dark mode after the scheduling changes
- [x] Push the latest changes to the active GitHub repository without exposing credentials

## Scheduling and theme verification gaps

- [x] Confirm server-side trainer and room overlap checks plus capacity enforcement in class creation
- [x] Add Vitest coverage for trainer and room scheduling conflicts
- [x] Explicitly verify Light/Dark mode and Toast rendering after room/trainer changes

## Repository and runtime clarification

- [x] Document the difference between the legacy GYM-Management-System Electron/static project and the modern Gym-Management-Web application
- [x] Verify and document the exact startup commands for the modern web app and legacy desktop app
- [x] Update repository links and README guidance so users do not launch the legacy static placeholder when expecting the full web dashboard
- [x] Provide a clear Windows PowerShell troubleshooting section for Python fallback and project selection

## Startup clarification release

- [x] Publish the dedicated Windows PowerShell troubleshooting guidance to the modern web and legacy desktop repositories
- [x] Verify web TypeScript/tests/build and desktop Jest tests (53/53) after documentation updates

## Desktop UI and installer enhancement

- [ ] Align the Electron desktop visual language with the modern PulseForge web dashboard
- [ ] Add bilingual loading animations and explanatory loading/empty/error states
- [x] Configure electron-builder for a Windows installer and documented packaging commands
- [x] Run desktop tests and package/build verification, then save a final checkpoint

## Full desktop system modernization

- [ ] Audit the Electron desktop architecture, modules, data services, and current feature coverage against the modern web system
- [ ] Define the desktop parity scope for members, subscriptions, payments, attendance, trainers, rooms, classes, PT, reports, settings, and bilingual workflows
- [ ] Upgrade the desktop data/services and screens as a coherent system rather than a visual-only refresh
- [ ] Add comprehensive bilingual loading, empty, success, and error states across desktop workflows
- [ ] Configure and document electron-builder installer targets and packaging scripts
- [ ] Run full desktop tests, type checks, package verification, and save a release checkpoint
- [x] Add explicit bilingual empty states for desktop dashboard activities, notifications, and alerts
- [x] Add bilingual dashboard error states with retry handling for failed data loads
- [x] Verify desktop empty/error states with automated tests and package/build checks
