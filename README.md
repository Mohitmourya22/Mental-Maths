# Mental Maths

**Mental Maths practice app — GDSC Solution Challenge 2024 project**

Mental Maths ek Android quiz app hai jo users ko timed multiple-choice maths questions ke saath mental calculation improve karne mein madad karti hai. App level-wise gameplay, countdown timer, scores, unlocked progress aur in-app sound effects ke saath banaayi gayi hai.

## Features

- Multiple difficulty levels
- Har round mein 10 multiple-choice questions
- Countdown timer aur circular progress indicator
- Correct/wrong answer score tracking
- Resume, restart aur next-level navigation
- SharedPreferences ke through level progress save
- Question data ko assets ke encrypted JSON format se load karna
- Native C++ component integration
- Splash screen aur custom app theme

## Tech Stack

- **Language:** Kotlin
- **UI:** Android XML layouts, View Binding
- **Minimum SDK:** 21 (Android 5.0)
- **Target/Compile SDK:** 33 (Android 13)
- **Data:** Gson, JSON assets
- **Encryption:** Themis library
- **Other:** AndroidX, Material Components, ConstraintLayout, SplashScreen API
- **Native:** CMake / C++

## Project Structure

Repository mein Android project source ZIP archive ke andar diya gaya hai:

```text
Mental-Maths/
├── Mental maths.zip       # Android Studio project
└── README.md
```

Archive ke andar app structure roughly is tarah hai:

```text
Math-Quiz-App-master/
├── app/
│   ├── src/main/
│   │   ├── assets/        # question.json & encryptedQuestion.json
│   │   ├── cpp/           # Native C++ code
│   │   ├── java/          # Kotlin activities, adapters & utilities
│   │   └── res/           # Layouts, drawable, fonts & resources
│   └── build.gradle
├── gradle/
├── gradlew
├── gradlew.bat
└── build.gradle
```

## Setup aur Run

1. Repository ko clone karein:

```bash
git clone https://github.com/Mohitmourya22/Mental-Maths.git
cd Mental-Maths
```

2. `Mental maths.zip` archive ko extract karein.

```bash
unzip "Mental maths.zip"
cd Math-Quiz-App-master
```

3. Android Studio mein project folder `Math-Quiz-App-master` ko open karein.

4. Gradle sync complete hone ka wait karein, phir Android device ya emulator select karke app run karein.

### Requirements

- Android Studio compatible with Android Gradle Plugin used in the project
- JDK 8 or newer
- Android SDK Platform 33
- Android device/API 21+ ya emulator

## How It Works

- `WelcomeActivity` app ka splash/welcome entry point hai.
- `LevelActivity` available levels aur saved progress dikhata hai.
- `QuestionActivity` encrypted question JSON ko assets se decrypt/load karta hai.
- Questions ko 10-item rounds mein split kiya gaya hai.
- User ke correct answers ke basis par score aur next level unlock hota hai.
- Progress aur relevant app state `SharedPreferenceManger` ke through persist hoti hai.

## Build APK

ZIP extract karne ke baad project root se:

```bash
./gradlew assembleDebug
```

Debug APK `app/build/outputs/apk/debug/` mein milegi.

Windows par:

```bat
gradlew.bat assembleDebug
```

## Screenshots

Project archive mein `screenshot/img1.png` se `screenshot/img4.png` tak sample app screenshots available hain.

## Contributing

Suggestions, bug reports aur improvements ke liye issue open karein ya pull request bhejein.

## Acknowledgement

This project was created for the **GDSC Solution Challenge 2024**.
