# @alphorax/react-native-inline-play-install

Google Play Inline Install wrapper for React Native Android apps. This library lets you launch the Google Play inline install half-sheet experience inside your app, using the latest Play Store APIs.

> ⚠️ Android-only. No-op on iOS.

---

## ✨ Features

- ✅ Seamless Google Play inline install from within your app
- ✅ Fallback to full Play Store page when inline not available
- ✅ Built with Kotlin native code
- ✅ TypeScript-first interface
- ✅ Optimized for React Native 0.63+

---

## 📦 Installation

```sh
npm install @alphorax/react-native-inline-play-install
# or
yarn add @alphorax/react-native-inline-play-install
```

> Make sure auto-linking is enabled in your React Native project.

---

## ⚙️ Usage

### Import
```ts
import InlinePlayInstall from '@alphorax/react-native-inline-play-install';
```

### Invoke the installer
```ts
InlinePlayInstall.launchInlineInstall({
  targetPackage: 'com.example.targetapp',
  callerPackage: 'com.alphorax.myapp',
  referrer: 'utm_source=myapp&utm_medium=native',
  cslId: 'custom_listing_abc123'
});
```

---

## 🔒 Permissions

No extra permissions are required beyond internet and access to the Play Store.

---

## 📱 Platform Support

| Platform | Support |
|----------|---------|
| Android  | ✅ Yes  |
| iOS      | ❌ No (safe no-op) |

---

## 🧪 Example

You can test this with any app that:
- Is published on the Play Store
- Uses a Custom Store Listing ID (CSL ID)
- Has inline install enabled in Play Console experiments (if required)

---

## 🔧 API

### `launchInlineInstall(options: InlineInstallOptions): Promise<string>`

#### Parameters

| Name           | Type     | Description                                |
|----------------|----------|--------------------------------------------|
| targetPackage  | string   | Package name of the app to install         |
| callerPackage  | string   | Your app’s package name                    |
| referrer       | string   | UTM referrer info                          |
| cslId          | string   | Custom store listing ID                    |

#### Returns
- `Promise<string>` — resolves on success, rejects on failure.

---

## 📁 Structure

```
@alphorax/react-native-inline-play-install
├── android/                         // Kotlin module
├── src/                             // TS interface
├── types/                           // TypeScript types
├── index.ts                         // Platform guard wrapper
├── package.json
├── tsconfig.json
├── README.md
```

---

## 🏗 Contributing

Pull requests and issues welcome!

```sh
git clone https://github.com/alphorax/react-native-inline-play-install.git
cd react-native-inline-play-install
npm install
```

### Run Example (Android)

```sh
cd example
npx react-native run-android
```

---

## 📜 License

MIT © [Alphorax](https://github.com/alphorax)
