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
