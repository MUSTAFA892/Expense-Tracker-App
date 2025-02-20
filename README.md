
# Expense Management App 💰

## Description 📄

This project is a simple yet powerful Expense Management app designed to help users keep track of their daily expenses. Built with Expo, it leverages the capabilities of React Native to provide a seamless and intuitive user experience. The app focuses on privacy and offline functionality by using local storage to save expense data directly on the user's device.

## About this project 📱

This is an Expense Management app built with Expo. The app allows users to track their expenses using local storage, without the need for a database.

### Additional Features 🚀

- **Update Profile**: Users can update their profile information, including name, email, and profile picture.
- **Manage Categories**: Users can add, edit, or delete expense categories to better organize their expenses.
- **Change PIN**: Users can set or change a PIN to secure access to the app.
- **Filters and Searching**: Users can filter and search transactions by amount, category, date, or description to quickly find specific expenses.
- **Export Transactions**: Users can export their transaction history as a CSV file for easy sharing and record-keeping.

## Environment Variables 🌐

This project uses environment variables to manage sensitive information. Create a `.env` file in the root directory and add the following:

```
EXPO_PUBLIC_SECURE_KEY=your_secure_key_here
```

Make sure to replace `your_secure_key_here` with your actual secure key.

## Features ✨

- Add new expenses with details such as amount, category, and date.
- View a list of all recorded expenses.
- Edit or delete existing expenses.
- Filter expenses by category or date.

## Local Storage 💾

This app uses the [AsyncStorage](https://react-native-async-storage.github.io/async-storage/docs/install/) library to store data locally on the device. This ensures that your expense data is available even when offline.

## Installation 🛠️

1. Clone the repository:

   ```bash
   git clone https://github.com/rohitp-18/expense-tracker-app.git
   cd expense-management-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the app:

   ```bash
   npx expo start
   ```

## Building APK for Android 📱

To build your app for Android and generate an APK file, follow these steps:

1. **Login to EAS**:
   - Run the following command to check the current user you're logged in as:
     ```bash
     eas whoami
     ```
   - If you’re not logged in yet, run the command:
     ```bash
     eas login
     ```

2. **Install EAS CLI** (if not installed):
   ```bash
   npm install --global eas-cli
   ```

3. **Initialize Your Project**:
   - If you're creating a new project using **Expo**, run the following command:
     ```bash
     eas init --id <your_id>
     ```

4. **Build for Android**:
   - Start the build for the Android platform using the command:
     ```bash
     eas build -p android
     ```

5. **APK or AAB File**:
   - If the build completes successfully, you will get an `.apk` file for Android. If not, you'll get an `.aab` file. In that case, follow the additional steps below to generate the APK.

6. **Using AAB to Generate APK** (if you get `.aab`):
   - Download **BundleTool** from the official GitHub releases page:
     [BundleTool Releases](https://github.com/google/bundletool/releases)
   - Download and extract the **`.aab`** and **`bundletool-all-1.18.0.jar`** files into the same folder.
   - Open a **command prompt** in that folder and run the following command to generate APKs from the `.aab` file:
     ```bash
     java -jar bundletool-all-1.18.0.jar build-apks --bundle=app.aab --output=expense.apks --mode=universal
     ```

   - Replace `app.aab` with the name of your `.aab` file, and replace `bundletool-all-1.18.0.jar` with the name of your **bundletool jar** file.
   - The output will generate an **`.apks`** file, which contains the APKs.

7. **Extract the APK**:
   - Compress the `.apks` file into a `.zip` archive and then extract it. You will find the generated APK file inside.

## Usage 📖

1. Open the app on your device or emulator.
2. Use the interface to add, view, edit, and delete expenses.
3. Filter expenses to view specific categories or date ranges.

---

