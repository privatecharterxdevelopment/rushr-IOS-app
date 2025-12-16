# Rushr iOS App

Native iOS app for Rushr built with Capacitor + Next.js.

## Setup

1. Install dependencies:
```bash
npm install
```

2. Copy environment file and fill in your values:
```bash
cp .env.example .env.local
```

3. Run development server:
```bash
npm run dev
```

4. For iOS Simulator:
```bash
# Update capacitor.config.ts - set USE_LOCAL_DEV = true
npx cap copy ios
cd ios/App && pod install
# Open in Xcode and run
open ios/App/App.xcworkspace
```

## Production Build

Set `USE_LOCAL_DEV = false` in `capacitor.config.ts` to load from production URL.

## Structure

- `/ios` - Native iOS project (Xcode)
- `/components` - React components for iOS views
- `/lib` - Utilities and Supabase client
- `/contexts` - React contexts for auth
- `/app` - Next.js app pages
