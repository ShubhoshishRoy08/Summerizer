# Quickmeds
Quickmeds is a mobile application built using React Native and Expo, designed to provide users with a seamless experience it is a comprehensive Patient assistive application.

## Table of Contents
- [Prerequisites](#Prerequisites)
- [Setting Up React Expo Development Build](#Setting Up React Expo Development Build)
- [Google Cloud Platform (GCP) Setup](#Google Cloud Platform (GCP) Setup)
- [Running the Application](#Running the Application)
- [Contributing](#Contributing)
- [License](#License)

## Prerequisites
Before setting up the project, ensure you have the following installed on your system:
- [Node.js](https://nodejs.org/) (v14.x or later)
- [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- [EAS CLI](https://docs.expo.dev/build/setup/)
- [Google Cloud SDK (for GCP setup)]()

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
GCP_PROJECT_ID=your_gcp_project_id
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
1. Go to the GCP Console.
2. Create a new project and note down the Project ID.

### 2. Enable Required APIs:
Enable the following APIs for your project:
- Firebase API (if using Firebase services)
- Cloud Storage API
- Cloud Functions API

Navigate to **APIs & Services > Library** and enable the required APIs.

### 3. Set Up Firebase:
1. Go to the Firebase Console.
2. Add a new project and link it to your GCP project.
3. Configure Firebase Authentication, Firestore, and Storage as needed.

### 4. Configure Service Account:
1. Navigate to **IAM & Admin > Service Accounts** in the GCP Console.
2. Create a new service account and grant it the necessary permissions (e.g., **Cloud Storage Admin, Firestore Admin**).
3. Generate a JSON key for the service account and download it.

### 5. Add GCP Credentials to the Project:
1. Place the downloaded JSON key in the `config` folder of your project.
2. Update the `.env` file with the path to the JSON key:

   ```env
   GOOGLE_APPLICATION_CREDENTIALS=config/your-service-account-key.json

### 6. Deploy Cloud Functions (if applicable)
If your project uses Cloud Functions, deploy them using the Google Cloud SDK
```bash
gcloud functions deploy your-function-name --runtime nodejs16 --trigger-http
```