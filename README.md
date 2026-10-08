# MyPantry

MyPantry is a cross-platform mobile application built with Flutter and Firebase designed for managing home pantry inventory, reducing food waste, discovering recipes, and tracking ingredient expiration dates. It enables users to keep an active inventory of their pantry items, search for recipes tailored to available ingredients, publish and share custom recipes, and receive expiration alerts.

---

## Features

### Pantry Inventory Management
- Track ingredient names, quantities, calories, and expiration dates.
- Automated ingredient search and autocomplete powered by the Open Food Facts API.
- Quick operations to add, edit, or consume ingredients.

### Recipe Discovery and Filtering
- Search recipes by title or filter by currently available pantry ingredients.
- Categorized recipe views: Search, Saved recipes, and My Recipes.
- Display recipe details including difficulty levels, required ingredients, step-by-step instructions, and images.

### Recipe Creation and Social Interaction
- Create, edit, and publish recipes with images and step-by-step instructions.
- Rate recipes using a like system.
- Post comments on recipes and manage comments on self-authored recipes.
- Share recipes via deep links generated using Firebase Dynamic Links.

### Notifications and Expiration Alerts
- Local push notifications scheduled using Firebase Cloud Messaging, `flutter_local_notifications`, and timezone data to alert users prior to ingredient expiration.

### Authentication and User Security
- Email and password authentication using Firebase Auth.
- Persistent login sessions backed by `shared_preferences`.
- Account management features including name updates, password changes requiring previous password verification, logout, and account deletion.

---

## Technologies Used

### Framework & Platform
- **Flutter** (Dart SDK `^3.7.0`)

### Backend & Cloud Services
- **Firebase Core**
- **Firebase Authentication**
- **Cloud Firestore**
- **Firebase Storage**
- **Firebase Messaging**
- **Firebase Dynamic Links**

### External Data & APIs
- **Open Food Facts API** (via `http`)

### Libraries & Packages
- **Local Storage & State Persistence**: `shared_preferences`
- **Notifications**: `flutter_local_notifications`, `timezone`
- **UI Components**: `flutter_typeahead`, `image_picker`, `share_plus`, `fluttertoast`, `flutter_keyboard_visibility`, `cupertino_icons`
- **Testing & Development**: `flutter_lints`, `test`, `mockito`, `mocktail`, `build_runner`

---

## Project Structure

```
lib/
├── databaseConnection/
│   ├── firestore_source.dart
│   ├── firestore_source_implementation.dart
│   ├── ingredientLogic/         # Ingredient data source & Open Food Facts integration
│   ├── pantryLogic/             # Pantry storage management
│   └── recipeLogic/             # Recipe data persistence & comments
├── services/                    # Firebase Auth, Dynamic Links, and Notification services
├── user/                        # User session management
├── screen/                      # Primary application screens (Pantry, Recipes, Settings, Auth)
├── widgets/                     # Reusable widgets, screen components, and dialogs
├── firebase_options.dart        # Platform Firebase configuration
└── main.dart                    # Application entry point and deep link route handling
```

---

## Getting Started

### Prerequisites

Ensure you have the following installed on your development machine:
- Flutter SDK (`^3.7.0` or higher)
- Dart SDK
- Android Studio, Xcode, or Visual Studio Code with the Flutter extension
- Firebase project setup (`google-services.json` for Android and `GoogleService-Info.plist` for iOS, or `firebase_options.dart`)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/LEIC-ES-2024-25/2LEIC06T5.git
   cd es-proj
   ```

2. Fetch project dependencies:
   ```bash
   flutter pub get
   ```

3. Run static analysis to verify project code:
   ```bash
   flutter analyze
   ```

4. Launch the application:
   ```bash
   flutter run
   ```

### Building for Release

- **Android APK**:
  ```bash
  flutter build apk
  ```

- **iOS Bundle**:
  ```bash
  flutter build ios
  ```

- **Web App**:
  ```bash
  flutter build web
  ```

---

## Documentation

Comprehensive project documentation, software design reports, user stories, and architectural diagrams are available in the [`docs/`](docs/) directory.
