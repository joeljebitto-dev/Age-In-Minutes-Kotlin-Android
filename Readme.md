# Age In Minutes - Kotlin Android

A simple Android app built with Kotlin that calculates a user's age in minutes. The app lets the user select a date using an Android date picker, then calculates the difference between the selected date and the current date in minutes.

## Features

* Native Android app built with Kotlin
* XML-based Android UI
* Date picker for selecting a birth date or past date
* Prevents future date selection
* Displays the selected date
* Calculates age/duration in minutes
* Simple single-screen layout
* AppCompat-based activity

## Tech Stack

* Kotlin
* Android SDK
* Android Gradle Plugin
* AppCompat
* Material Components
* ConstraintLayout
* XML layouts
* Gradle

## Project Structure

```text
Age-In-Minutes-Kotlin-Android/
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── java/com/joeljebitto/ageinminutesapp/
│   │       │   └── MainActivity.kt
│   │       ├── res/
│   │       │   ├── layout/
│   │       │   │   └── activity_main.xml
│   │       │   ├── values/
│   │       │   └── mipmap-*/
│   │       └── AndroidManifest.xml
│   └── build.gradle
├── build.gradle
├── settings.gradle
└── README.md
```

## How It Works

The app uses `DatePickerDialog` to let the user select a date. After selection, it converts both the selected date and the current date into minutes, then subtracts them to calculate the total elapsed minutes.

Main flow:

```text
Launch app
  ↓
Tap Select Date
  ↓
Choose a past date
  ↓
Display selected date
  ↓
Calculate elapsed time in minutes
  ↓
Show result on screen
```

The app prevents selecting future dates by setting the date picker's maximum date to the current date.

## Requirements

* Android Studio
* Android SDK
* JDK 8 or compatible Java toolchain
* Gradle / Android Gradle Plugin support

Project configuration:

```text
compileSdkVersion 30
minSdkVersion 16
targetSdkVersion 30
applicationId com.joeljebitto.ageinminutesapp
```

## Getting Started

Clone the repository:

```bash
git clone https://github.com/joeljebitto-dev/Age-In-Minutes-Kotlin-Android.git
cd Age-In-Minutes-Kotlin-Android
```

Open the project in Android Studio.

Then:

1. Let Android Studio sync Gradle.
2. Select an emulator or connected Android device.
3. Click **Run**.

## Running from Command Line

Build the debug APK:

```bash
./gradlew assembleDebug
```

On Windows:

```bash
gradlew.bat assembleDebug
```

Install on a connected Android device:

```bash
./gradlew installDebug
```

## App UI

The app screen contains:

* Title text
* Date selection button
* Selected date output
* Calculated minutes output
* Supporting label text

## Notes

* This is a beginner-friendly Android project.
* The UI is implemented using classic Android XML views.
* The main logic is implemented in `MainActivity.kt`.
* The selected date is parsed with `SimpleDateFormat`.
* The result is displayed as total minutes elapsed from the selected date to the current date.

## Future Improvements

* Fix month display formatting if needed, since Android `Calendar.MONTH` is zero-based
* Add age display in years, months, days, hours, and minutes
* Add input validation and parse-error handling
* Add support for different date formats
* Improve UI styling and spacing
* Add dark mode support
* Replace deprecated `jcenter()` repository usage
* Replace deprecated Kotlin Android Extensions if introduced later
* Update Android Gradle Plugin and Kotlin versions
* Add unit tests for date calculation logic
* Add ViewModel-based architecture for better separation of concerns

## Author

Built by [Joel Jebitto](https://github.com/joeljebitto-dev).
