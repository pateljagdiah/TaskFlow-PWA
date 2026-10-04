# TaskFlow – Smart To-Do List (PWA)

A modern, offline-first Progressive Web App (PWA) designed primarily for mobile productivity and Android phones. Built with React, TypeScript, Vite, Tailwind CSS, and IndexedDB.

---

## 📱 Features

- **Offline-First Storage**: Full offline functionality using browser IndexedDB (`idb`) — tasks and settings are always available without network connectivity.
- **Mobile-First Android Design**: Tailored for phone screens with a bottom navigation bar, Floating Action Button (+), swipe-to-delete gestures, bottom sheet modals, and safe-area padding.
- **Productivity Pulse**: Home screen tracking today's progress, completion rate percentage, remaining tasks, and high-priority counters.
- **Task Management**:
  - Full CRUD: Create, Edit, Delete, Complete, Restore tasks.
  - Due date & optional due time.
  - Priority indicators with both icons and textual badges (Low, Medium, High).
  - Categorization across Personal, Work, Study, Shopping, Health, and Other spaces.
  - Recurring tasks with automatic next-occurrence generation (Daily, Weekly, Monthly).
  - Confetti celebration upon task completion.
- **Instant Search & Filters**: Search across titles, notes, and categories. Filter by All, Today, Upcoming, Completed, and High Priority. Sort by Due Date, Priority, Creation Date, or Alphabetical.
- **Web Reminders**: Non-intrusive notification system leveraging the Web Notification API and Service Worker alarms.
- **Themes**: Light, Dark, and System theme support with persistent settings.
- **PWA & PWABuilder Ready**:
  - Web App Manifest (`manifest.webmanifest`) with standalone display, theme color, icons, and shortcuts.
  - Full Service Worker (`sw.js`) with cache-first static caching and network-first navigation fallback.
  - Crisp generated 192x192, 512x512, and maskable icons.
  - Seamless "Install App" prompt banner and header shortcut.

---

## 🛠️ Tech Stack

- **Framework**: React 19 + TypeScript
- **Bundler**: Vite
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Local Database**: IndexedDB (via `idb`)
- **Animations**: CSS animations + `canvas-confetti`
- **PWA**: Service Worker (`public/sw.js`) + Web App Manifest (`public/manifest.webmanifest`)

---

## 🚀 Getting Started

### Install Dependencies
```bash
npm install
```

### Run Locally (Dev)
```bash
npm run dev
```

### Production Build
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

---

## ☁️ Deployment (Vercel & PWABuilder)

### Vercel Deployment
1. Connect this repository to Vercel.
2. Vercel automatically detects the Vite framework with the build command:
   ```bash
   npm run build
   ```
   (which runs `tsc -b && vite build`) and output directory `dist`.
3. The TypeScript configuration is fully pre-configured (`tsconfig.json`, `tsconfig.app.json`, `tsconfig.node.json`) to pass all strict build checks with zero warnings or errors.

### PWABuilder App Store Packaging
Once deployed to HTTPS (e.g. `https://your-taskflow.vercel.app`):
1. Navigate to [pwabuilder.com](https://www.pwabuilder.com/).
2. Enter your deployed URL.
3. TaskFlow passes all PWA criteria (Valid Manifest, Service Worker, 192x192 & 512x512 icons, maskable icons, HTTPS ready).
4. Download the Android APK/AAB bundle for Google Play Store or install directly from Chrome on Android.
