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
- [ ] Verify trainer specialties, assigned classes, and PT client relationships
- [x] Verify class scheduling, capacity enforcement, booking, and cancellation flows
- [ ] Verify PT packages, assignments, session tracking, and completion flow
- [ ] Add Vitest coverage for gym database helpers and tRPC procedures beyond auth
- [x] Save a final checkpoint after all verification follow-ups are complete

## Required corrections before release

- [x] Add member delete support in the backend and UI for complete CRUD
- [x] Show each member's actual subscription status in the members table
- [ ] Add Vitest coverage for subscription renew, freeze, and unfreeze lifecycle logic
- [x] Refactor class cancellation to target a specific booking for a displayed class and member
