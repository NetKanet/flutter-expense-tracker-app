# Flutter Expense Tracker App

A personal expense tracker app built with Flutter & Dart, following [Academind's Flutter & Dart - The Complete Guide](https://www.udemy.com/course/learn-flutter-dart-to-build-ios-android-apps/) on Udemy (Section 5-6).

## Features

- Add expenses with title, amount, date, and category
- Swipe to delete with undo (Dismissible + SnackBar)
- Visual bar chart grouped by category
- Dark mode support (system-based)
- Responsive layout — landscape: chart beside list, modal adapts

## What I Learned

### Section 5 — Expense Tracker Core
- **StatefulWidget** — managing expense list with setState()
- **ListView.builder** — efficient rendering (only visible items)
- **Dismissible + ValueKey** — swipe to delete pattern
- **TextEditingController + dispose()** — managing input lifecycle
- **showModalBottomSheet / showDialog / showDatePicker** — overlays
- **ScaffoldMessenger + SnackBar** — notifications with Undo
- **ThemeData().copyWith() + ColorScheme.fromSeed()** — theming from one place
- **Dark mode** — ThemeData.dark().copyWith() + kDarkColorScheme
- **enum + Initializer list** — type-safe categories + auto-generated UUID
- **Validation** — tryParse, trim, isEmpty, logical operators

### Section 6 — Responsive & Adaptive UI
- **Widget Size Constraints** — how parent constraints + child preferences determine size
- **Expanded** — fixes unconstrained-inside-unconstrained (ListView in Column, Chart in Row)
- **LayoutBuilder** — responsive layout based on parent constraints (not screen size)
- **MediaQuery** — screen width for main layout, viewInsets.bottom for keyboard
- **SingleChildScrollView** — scrollable modal when keyboard opens
- **SafeArea / useSafeArea** — avoid notch and system UI overlap
- **Collection if/else** — conditional widgets in list without curly braces

## Project Structure

```
lib/
├── main.dart                       # Entry point + ThemeData (light & dark)
├── models/
│   └── expense.dart                # Expense, Category enum, ExpenseBucket
└── widgets/
    ├── expenses.dart               # Main screen — list + chart + responsive layout
    ├── new_expense.dart            # Add expense modal — LayoutBuilder responsive
    ├── expenses_list/
    │   ├── expenses_list.dart      # ListView.builder + Dismissible
    │   └── expense_item.dart       # Individual expense Card
    └── chart/
        ├── chart.dart              # Spending overview chart
        └── chart_bar.dart          # FractionallySizedBox bar
```

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install)
- An emulator or physical device

### Run

```bash
git clone https://github.com/NetKanet/flutter-expense-tracker-app.git
cd flutter-expense-tracker-app
flutter pub get
flutter run
```

### Debug with DevTools

```
Cmd+Shift+P → "Flutter: Open DevTools in Web Browser"
```

Use **Flutter Inspector → Layout Explorer** to see widget constraints and sizing.

## Screenshots

<!-- Add screenshots here -->

## Credits

- [Flutter & Dart - The Complete Guide](https://www.udemy.com/course/learn-flutter-dart-to-build-ios-android-apps/) by Maximilian Schwarzmuller (Academind)
- Section 5 — Building the Expense Tracker
- Section 6 — Responsive & Adaptive User Interfaces
