
# Tip Calculator Android App

## Overview
The **Tip Calculator** app is a simple Android application that allows users to calculate the tip amount based on their bill and the desired tip percentage. The app also provides an option to round up the tip amount for convenience.

## Features
- Input the bill amount and tip percentage.
- Automatic calculation of the tip amount.
- Option to round up the tip to the nearest whole number.
- User-friendly interface built using **Jetpack Compose**.
- Supports currency formatting based on local settings.

## Technologies Used
- **Kotlin**: The primary programming language.
- **Jetpack Compose**: For building the UI.
- **Material3 Components**: For a modern and sleek design.
- **Android Studio**: The development environment.

## How It Works
1. The user enters the bill amount.
2. The user specifies the tip percentage.
3. The app calculates the tip and displays the amount.
4. The user can toggle the "Round Up Tip" switch to round up the tip amount.
5. The total tip is displayed in a formatted currency style.

## Code Breakdown
### **Main Components**
- **`MainActivity.kt`**: The entry point of the app, setting up the UI.
- **`TipTimeLayout()`**: The main UI function that contains the input fields and result display.
- **`EditNumberField()`**: A reusable composable function for text input with a leading icon.
- **`RoundTheTipRow()`**: A switch to toggle the rounding of the tip.
- **`calculateTip()`**: The function that calculates the tip based on user input.

### **Key Functions**
```kotlin
private fun calculateTip(amount: Double, tipPercent: Double = 15.0, roundUp: Boolean): String {
    var tip = tipPercent / 100 * amount
    if (roundUp) {
        tip = kotlin.math.ceil(tip)
    }
    return NumberFormat.getCurrencyInstance().format(tip)
}
```
- **Takes in bill amount and tip percentage**
- **Rounds up the tip if the toggle is enabled**
- **Formats the tip amount to the local currency format**

## Setup & Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/tip-calculator.git
   ```
2. Open the project in **Android Studio**.
3. Sync Gradle dependencies.
4. Run the app on an emulator or a physical device.

## Screenshots
![tip calculator android app](img.png)

## License
```
Licensed under the Apache License, Version 2.0.
You may obtain a copy at https://www.apache.org/licenses/LICENSE-2.0
```

## Contribution
Feel free to fork the repository and submit a pull request with improvements or bug fixes.

---
**Author**: The Android Open Source Project

