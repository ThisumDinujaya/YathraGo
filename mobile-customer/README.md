# YathraGo Customer Mobile App

This is the YathraGo customer mobile app built with [Expo](https://expo.dev) and React Native. It provides a seamless experience for customers (parents and staff) to book and manage their transport.

## ✨ Features

- **Find transport services**: Find and book verified transport(School/Staff) services.
- Manage multiple profiles: Manage multiple child profiles with own staff profile
- **Real-time Tracking**: Monitor ongoing trips on a live map.
- **Modern UI**: Clean and intuitive interface powered by NativeWind (Tailwind CSS).
- **Cross-platform**: Consistent experience across iOS and Android.

## 🛠️ Tech Stack

- **Framework**: React Native, Expo
- **Styling**: NativeWind (Tailwind CSS)
- **Language**: TypeScript
- **Navigation**: Expo Router (File-based routing)

## 🚀 Getting Started

1. **Install dependencies**

   ```bash
   npm install
   ```

2. **Start the development server**

   ```bash
   npm run dev
   # or
   npx expo start
   ```

3. **Run on a device or emulator**
   - Press `a` to open on an Android emulator.
   - Press `i` to open on an iOS simulator (macOS only).
   - Scan the QR code using the Expo Go app on your physical device.

## 📁 Project Structure

```
mobile-customer/
├── app/                    # File-based routing (screens)
│   ├── (tabs)/             # Main tab navigation
│   ├── index.tsx           # Entry point
│   └── welcome.tsx         # Splash/Welcome screen
├── assets/                 # Images and fonts
├── components/             # Reusable UI components
└── constants/              # App constants and themes
```

## 📄 License

This project is part of the YathraGo ecosystem.