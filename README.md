# Quickmeds
Welcome to QuickMeds, a React Native Expo project aimed at building a comprehensive patient assistive application. This README provides instructions and important information for setting up and running the application during its initial development phase.

## Table of Contents
- [Prerequisites](#Prerequisites)
- [Setting Up React Expo Development Build](#Setting-Up-React-Expo-Development-Build)
- [Google Cloud Platform (GCP) Setup](#Google-Cloud-Platform-(GCP)-Setup)
- [Running the Application](#Running-the-Application)
- [Contributing](#Contributing)
- [License](#License)

## Prerequisites
Follow the eas documentation to install the necessary dependencies , also the platform is a expo development build
1. Install npx expo-cli: Ensure you have npx expo-cli installed. You can do this with:
```bash
npm install -g expo-cli
```
2. Login with EAS Credentials: Log in to your Expo account:
```bash
npx expo login
```
3. Build the Platform for Android: To generate an APK for the emulator or physical device, use the command:
```bash
npx expo run:android
```
After the build completes, download the APK and install it on your emulator or physical device.


## Setting Up React Expo Development Build
Follow these steps to set up the React Expo development environment:

### 1. Clone the Repository
```bash
git clone https://github.com/kumareshbalaji48/Quickmeds.git
cd Quickmeds
```
### 2. Install Dependencies
Install all the required dependencies using npm or Yarn:
```bash
npm install
# or
yarn install
```

### 3. Configure Environment Variables
Create a `.env` file in each app directory and add the necessary environment variables. For example
```bash
API_KEY=your_api_key_here
```

### 4. Start the Development Server
Run the Expo development server
```bash
expo start
```
This will open a browser window with the Expo Dev Tools. You can run the app on an emulator or a physical device using the Expo Go app.


## Google Cloud Platform (GCP) Setup
To set up GCP for the Quickmeds project, follow these steps:

### 1. Create a GCP Project:
- Go to the GCP Console.
- Create a new project and note down the Project ID.

### 2. Enable Required APIs:
Enable the following APIs for your project:
- Firebase API (if using Firebase services)
- Cloud Storage API
- Cloud Functions API

Navigate to **APIs & Services > Library** and enable the required APIs.

### 3. Set Up Firebase:
- Add a new project and link it to your GCP project.
- Go to the Firebase Console.
- Configure Firebase Authentication, Firestore, and Storage as needed.

### 4. Configure Service Account:
- Navigate to **IAM & Admin > Service Accounts** in the GCP Console.
- Create a new service account and grant it the necessary permissions (e.g., **Cloud Storage Admin, Firestore Admin**).
- Generate a JSON key for the service account and download it.

### 5. Add GCP Credentials to the Project:
- Place the downloaded JSON key in the `config` folder of your project.
- Update the `.env` file with the path to the JSON key:

   ```env
   GOOGLE_APPLICATION_CREDENTIALS=config/your-service-account-key.json

### 6. Deploy Cloud Functions (if applicable)
If your project uses Cloud Functions, deploy them using the Google Cloud SDK
```bash
gcloud functions deploy your-function-name --runtime nodejs16 --trigger-http
```


## Running the Application
Once the setup is complete, you can run the application using the following steps:
### 1. Start the Expo Development Server
```bash
expo start
```
### 2. Run on a Physical Device
- Install the Expo Go app on your Android or iOS device.
- Scan the QR code displayed in the Expo Dev Tools to run the app on your device.
### 3. Run on an Emulator
- Use an Android Emulator or iOS Simulator to run the app.
- Follow the instructions in the Expo Dev Tools to launch the app on the emulator.

## Future Plans
- Fully integrate live appointment booking with web interface.
- Complete backend implementation for all features.
- Upgrade to Firebase Blaze Plan for enhanced functionality.
- Expand feature set to include push notifications and detailed analytics.