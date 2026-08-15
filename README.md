# PulseForge Gym Management Web

PulseForge Gym Management is a bilingual Arabic/English web application for operating a modern gym. It combines member management, monthly subscriptions, financial analytics, class scheduling, bookings, attendance, trainers, and personal training in one responsive workspace.

> The application supports English (LTR) and Arabic (RTL). The selected language is persisted in the browser and applies across the dashboard without a page reload.

## Features

The application provides KPI dashboards for members, active subscriptions, daily revenue, attendance, and expiring memberships. Financial reports include configurable date ranges, revenue trends, payment-method distribution, subscription revenue, and immediate XLSX export for reports and filtered member data.

Operations teams can create, edit, search, filter, and safely archive members while seeing the real subscription lifecycle. Subscription workflows include monthly creation, renewal, freeze, unfreeze, expiring, expired, and cancelled states. The class module supports trainer assignment, capacity, pricing, scheduling, booking, and scoped cancellation. Attendance, trainer profiles, PT packages, member assignments, scheduled sessions, and session completion are also connected to the database.

The web application is installable as a Progressive Web App. It includes a web manifest, install metadata, an offline-safe application shell, and a production Service Worker that does not cache API responses.

## Technology

| Layer | Technology |
|---|---|
| Frontend | React 19, Vite, Tailwind CSS 4, Recharts, shadcn/ui |
| Backend | Express, tRPC 11, TypeScript |
| Database | MySQL/TiDB through Drizzle ORM |
| Authentication | Manus OAuth and protected tRPC procedures |
| Export | XLSX workbook generation |
| Mobile companion | React Native / Expo project: `gym-management-mobile` |
| Quality | TypeScript checks and Vitest |

## Requirements

Install Node.js 20 or newer, pnpm, and access to a MySQL/TiDB database. The managed deployment environment supplies the required authentication and database environment variables. For local development, use a `.env` file based on the environment variables documented by the deployment environment; never commit secrets.

## Web setup

```bash
pnpm install
pnpm check
pnpm test
pnpm dev
```

The development server opens the local preview URL printed by Vite. The production build is created with:

```bash
pnpm build
pnpm start
```

Database schema changes must be generated with Drizzle and applied through the project's controlled migration workflow. Do not use destructive SQL against a production database without a reviewed backup and migration plan.

## PWA installation

Open the production HTTPS URL in a supported browser, then use the browser's **Install app** or **Add to Home Screen** action. The application includes `/manifest.webmanifest` and `/sw.js`. API routes are intentionally excluded from Service Worker caching so membership, payments, attendance, and reports always request current server data.

## Mobile companion app

The native companion project is maintained separately at `/home/ubuntu/gym-management-mobile`. It uses Expo and TypeScript, supports Arabic and English with persistent language selection, and calls the same tRPC backend through `EXPO_PUBLIC_API_URL`.

```bash
cd gym-management-mobile
npm install
EXPO_PUBLIC_API_URL=https://YOUR-GYM-DOMAIN npm start
```

The mobile app expects an authenticated backend session. Configure the approved mobile authentication flow and store a short-lived session token in the platform's secure storage before using protected operations. The current mobile shell exposes dashboard metrics and upcoming classes and displays an explicit unavailable state when the API or authentication is not configured; it does not fabricate business numbers.

## Testing

Run the web checks with:

```bash
pnpm check
pnpm test -- --run
```

Run the mobile TypeScript check with:

```bash
cd gym-management-mobile
npx tsc --noEmit
```

The web test suite covers authentication and feature procedures for subscriptions, trainers, classes, bookings, and personal training. Browser verification should be performed against the production build before release.

## Security and data handling

All protected business procedures require an authenticated user. Administrative operations should remain behind the server-side role guard. XLSX files are generated from authorized query results in the browser and are not stored on the server. The Service Worker never caches `/api/` requests. Do not commit `.env`, session tokens, database credentials, exported member data, or backup files.

## Repository layout

```text
client/                 React web application and PWA entry point
drizzle/                Drizzle schema and migrations
server/                 Database helpers, tRPC routers, and tests
shared/                 Shared constants and types
todo.md                 Feature and verification history
```

## العربية

PulseForge Gym Management هو تطبيق ويب احترافي ثنائي اللغة لإدارة الصالات الرياضية. يدعم التطبيق إدارة الأعضاء والاشتراكات الشهرية والمدفوعات والتقارير المالية والحضور والمدربين والحصص والحجوزات والتدريب الشخصي من خلال لوحة تحكم واحدة متجاوبة.

يدعم التطبيق **العربية باتجاه RTL والإنجليزية باتجاه LTR**، ويحفظ اختيار اللغة في المتصفح ويطبقه على جميع الصفحات دون إعادة تحميل. تتضمن التقارير مؤشرات الأداء واتجاهات الإيرادات وتوزيع طرق الدفع وتصدير بيانات التقارير والأعضاء إلى ملفات XLSX مباشرة.

يمكن تثبيت نسخة الويب على الهاتف كتطبيق PWA من خلال HTTPS ثم اختيار **تثبيت التطبيق** أو **إضافة إلى الشاشة الرئيسية**. يحتوي المشروع على manifest وService Worker، مع استثناء طلبات API من التخزين المؤقت حتى تبقى بيانات الأعضاء والمدفوعات والحضور والتقارير محدثة.

يوجد أيضاً مشروع Expo مستقل باسم `gym-management-mobile` كتطبيق مرافق أصلي للموبايل، ويدعم اللغتين ويحفظ اختيار اللغة ويتصل بنفس خادم tRPC عند إعداد `EXPO_PUBLIC_API_URL` وتدفق المصادقة الخاص بالموبايل.

## الدعم والمساهمة

قبل إرسال تغيير، شغّل `pnpm check` و`pnpm test -- --run`، ثم راجع التوافق بين مخطط Drizzle واستعلامات قاعدة البيانات وإجراءات tRPC وواجهة المستخدم. يجب أن تكون أي إضافة جديدة ثنائية اللغة، وأن تحافظ على صلاحيات الوصول، وأن تضيف اختبارات مناسبة للتدفقات الحساسة.

## License

This project is distributed under the license included in the repository.
