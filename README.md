# Gym_Tracker


A modern, mobile-first **Gym Tracker web application** designed to help users manage workouts, track nutrition and macros, explore exercises, manage their profile, and export their fitness data.

The application uses a shared browser-based data system so different sections of the app can work together seamlessly.

---
## 🚀 Live Demo

🔗 **Live Application:**
https://pathrabe2416.github.io/Gym_Tracker/

---

## 📌 Overview

**Gym Tracker** is a lightweight fitness management application built with a clean, modern dark-themed interface.

The application brings workout management and nutrition tracking into one place, allowing users to:

* Manage their workout routine
* Browse and save exercises
* Add exercises directly to workouts
* Track sets and reps
* Log meals and nutrition
* Monitor calories and macronutrients
* Calculate personalized macro goals
* Manage user profile information
* View workout muscle distribution
* Export fitness data as a report

---

## ✨ Features

### 🏠 Dashboard

The dashboard provides a centralized overview of the user's fitness data.

**Includes:**

* User profile information
* Current weight
* Height
* Today's workout
* Water intake
* Muscle-group distribution
* Nutrition overview
* Daily macro information
* Protein, carbohydrates, fats and calories

The dashboard reads shared application data from `localStorage` so information updated on other pages can be reflected here.

---

### 🥗 Nutrition & Macro Tracking

The Nutrition section allows users to manage their daily food intake.

**Features:**

* Search food items
* Add meals
* Set serving quantities
* Calculate nutritional values
* Track:

  * Calories
  * Protein
  * Carbohydrates
  * Fats
* View daily nutrition totals
* Calculate macro goals dynamically from user information

The application stores nutrition information together with the main `gymTrackerData` object.

---

### 🏋️ Workout Management

The Workout section allows users to manage their active training routine.

**Features:**

* View today's workout
* Display exercise count
* View sets and reps
* Remove exercises
* Start a workout session
* Finish a workout session
* Maintain the active workout between pages

The active workout is stored inside:

```text
gymTrackerData.activeWorkout
```

---

### 💪 Exercise Library

The Exercise Library provides a collection of exercises that can be used to build workouts.

**Features:**

* Browse exercises
* View exercise information
* Filter exercises
* Save favorite exercises
* Add exercises to the active workout
* Display:

  * Target muscle
  * Equipment
  * Difficulty
  * Sets & reps

Exercises added from the library are synchronized with the Workout section.

---

### 📊 Muscle Distribution

The dashboard calculates muscle-group distribution based on the exercises contained in the active workout.

The application uses the number of sets as a practical representation of training volume.

Supported muscle groups include categories such as:

* Chest
* Back
* Legs
* Shoulders
* Arms
* Core
* Other

This data is then presented as a visual distribution on the dashboard.

---

### ⚙️ Settings

The Settings section provides a central place for managing application and user information.

The stored user information is also used by the nutrition system when calculating personalized macro goals.

---

### 📄 Export & Reports

The application includes an Export section for generating a structured fitness report.

The report can include information such as:

* User profile
* Fitness information
* Nutrition data
* Workout information
* Muscle distribution

The export page also includes print/PDF-oriented styling for generating a cleaner report.

---

## 🔄 Application Data Flow

The application uses a shared browser storage architecture.

```text
                    ┌─────────────────┐
                    │  gymTrackerData │
                    │   localStorage  │
                    └────────┬────────┘
                             │
       ┌─────────────┬───────┼────────┬─────────────┐
       │             │       │        │             │
       ▼             ▼       ▼        ▼             ▼
   Dashboard     Nutrition Workouts Exercises    Settings
       │             │       │        │             │
       └─────────────┴───────┴────────┴─────────────┘
                             │
                             ▼
                         Export
```

This architecture allows different pages to read and update shared application data without requiring a backend database.

---

## 💾 Data Storage

The current application uses browser `localStorage`.

Main storage key:

```javascript
gymTrackerData
```

Important data areas include:

```text
gymTrackerData
│
├── user
├── goals
├── nutrition
│   ├── meals
│   └── today
└── activeWorkout
    ├── name
    ├── durationMin
    └── exercises
```

This makes the application simple to run locally without requiring a server or external database.

---

## 🛠️ Technologies Used

* **HTML5**
* **CSS3**
* **JavaScript**
* **Browser LocalStorage**
* **SVG Icons**
* **Responsive / Mobile-first UI**

---

## 🎨 Design

The application follows a modern fitness-dashboard design approach with:

* Dark interface
* Green accent color
* Mobile-first layout
* Rounded cards
* Compact information hierarchy
* Bottom navigation
* Responsive components
* Minimal and focused UI

The application is designed around a mobile-width experience while maintaining a clean desktop presentation.

---

## 📁 Project Structure

```text
Gym-Tracker/
│
├── index.html          # Dashboard
├── macros.html         # Nutrition & Macro Tracking
├── workouts.html       # Workout Management
├── exercises.html      # Exercise Library
├── settings.html       # User & App Settings
├── export.html         # Data Export / Report
│
└── README.md
```

> File names may vary depending on the final project version.

---


## 🔗 Page Navigation

The application is organized into interconnected sections:

```text
Dashboard
   │
   ├── Workouts
   │      └── Exercise Library
   │
   ├── Nutrition
   │
   ├── Settings
   │
   └── Export
```

Each section is designed to work with the shared application data.

---




## 🤝 Contributing

Contributions, suggestions and improvements are welcome.

If you want to contribute:

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Test the application
5. Submit a pull request

---

## 📜 License

This project is available for educational and personal development purposes.

Add your preferred license here if you decide to publish the project under a specific open-source license.

---

## 👨‍💻 Project

**Gym Tracker**
A simple and practical fitness management application focused on workout organization, nutrition tracking and personal fitness data.

⭐ If you find the project useful, consider giving the repository a star.
