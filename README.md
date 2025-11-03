# Foodfast

An app for collecting your favourite recipes and auto-create shopping lists.

This is a cross-platform mobile and desktop application built with Angular and Ionic Framework, deployable to iOS, Android, Windows, and Linux.

## Features

- Built with **Angular 20** and **Ionic 8**
- Cross-platform support via **Capacitor**
- Responsive design optimized for mobile and desktop
- Clean, modular architecture following Angular best practices

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher) and **npm**
- **Angular CLI**: `npm install -g @angular/cli`
- **Ionic CLI**: `npm install -g @ionic/cli`

### Platform-Specific Requirements

#### iOS Development
- **macOS** with **Xcode** installed
- **CocoaPods**: `sudo gem install cocoapods`

#### Android Development
- **Android Studio** with Android SDK
- **Java Development Kit (JDK)** 11 or higher

#### Windows/Linux Desktop
- **Electron** (for desktop builds)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/fondencn/foodfast.git
cd foodfast
```

2. Install dependencies:
```bash
npm install
```

## Development

### Run in Browser
To run the application in development mode in your browser:

```bash
npm start
```

Then open your browser and navigate to `http://localhost:4200/`

### Run on iOS Simulator

1. Build the web assets:
```bash
npm run build
```

2. Sync the Capacitor project:
```bash
npx cap sync ios
```

3. Open in Xcode:
```bash
npx cap open ios
```

4. Run the app from Xcode by pressing the Play button

### Run on Android Emulator/Device

1. Build the web assets:
```bash
npm run build
```

2. Sync the Capacitor project:
```bash
npx cap sync android
```

3. Open in Android Studio:
```bash
npx cap open android
```

4. Run the app from Android Studio

## Building for Production

### Build Web Assets

```bash
npm run build
```

The build artifacts will be stored in the `dist/` directory.

### Build for iOS

1. Build the web assets:
```bash
npm run build
```

2. Sync with iOS project:
```bash
npx cap sync ios
```

3. Open in Xcode:
```bash
npx cap open ios
```

4. In Xcode:
   - Select your signing team
   - Choose a device or simulator
   - Product → Archive
   - Follow the App Store submission process

### Build for Android

1. Build the web assets:
```bash
npm run build
```

2. Sync with Android project:
```bash
npx cap sync android
```

3. Open in Android Studio:
```bash
npx cap open android
```

4. In Android Studio:
   - Build → Generate Signed Bundle / APK
   - Follow the wizard to create a release build

### Build for Desktop (Electron)

For Windows and Linux desktop deployment, you can use Electron:

1. Install Electron:
```bash
npm install --save-dev @capacitor-community/electron
```

2. Add Electron platform:
```bash
npx cap add @capacitor-community/electron
```

3. Build and run:
```bash
npm run build
npx cap sync @capacitor-community/electron
npx cap open @capacitor-community/electron
```

## Project Structure

```
foodfast/
├── android/               # Android native project (Capacitor)
├── ios/                   # iOS native project (Capacitor)
├── src/
│   ├── app/
│   │   ├── home/         # Home page component
│   │   ├── app.config.ts # App configuration
│   │   ├── app.routes.ts # Route definitions
│   │   ├── app.ts        # Root component
│   │   └── app.html      # Root template
│   ├── index.html        # Main HTML file
│   ├── main.ts           # Application entry point
│   └── styles.scss       # Global styles
├── capacitor.config.ts   # Capacitor configuration
├── angular.json          # Angular CLI configuration
├── package.json          # npm dependencies
└── tsconfig.json         # TypeScript configuration
```

## Technologies Used

- **Angular 20** - Progressive web application framework
- **Ionic 8** - Cross-platform UI components
- **Capacitor 7** - Native runtime for web apps
- **TypeScript** - Typed superset of JavaScript
- **SCSS** - CSS preprocessor

## Best Practices Followed

This project follows Angular and Ionic best practices:

- **Standalone Components**: Uses Angular standalone components architecture
- **Lazy Loading**: Routes are lazy-loaded for optimal performance
- **Modular Architecture**: Clean separation of concerns
- **TypeScript Strict Mode**: Enhanced type safety
- **Responsive Design**: Mobile-first approach with Ionic components
- **Platform-Specific Optimizations**: Native behavior on each platform

## Testing

Run unit tests:
```bash
npm test
```

## Updating Dependencies

To update Angular, Ionic, and Capacitor:

```bash
npm update
npx cap sync
```

## Troubleshooting

### iOS Build Issues
- Ensure Xcode is up to date
- Run `pod install` in the `ios/App` directory
- Clean build folder in Xcode (Product → Clean Build Folder)

### Android Build Issues
- Check Android SDK is properly installed
- Ensure `ANDROID_HOME` environment variable is set
- Try invalidating caches in Android Studio (File → Invalidate Caches)

### Web Build Issues
- Clear Angular cache: `rm -rf .angular/cache`
- Delete node_modules and reinstall: `rm -rf node_modules && npm install`

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For issues, questions, or contributions, please open an issue in the GitHub repository.

## Resources

- [Angular Documentation](https://angular.dev)
- [Ionic Documentation](https://ionicframework.com/docs)
- [Capacitor Documentation](https://capacitorjs.com/docs)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
