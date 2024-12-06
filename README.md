# Tunelink CS520 Project
Made by Ozel Yilmazel, Aryan Nair, Hanna Jiang, Rachel Lahav, Ryan Zaid

## Introduction
TuneLink is a mobile social media platform designed to help music enthusiasts discover and share music through short snippets. The app allows users to link their snippets to Spotify or YouTube for full song access, encouraging both discovery and promotion of new music. Users will be able to interact with the music snippets through likes and follows, creating a vibrant community centered around music sharing and discovery.

## Installation instructions and configuration
This section will prepare your local copy to run the application and tests.

Please directly clone this repository. Navigate to the cloned directory

Please make sure you have node.js and npm installed. For frontend you also need Expo Go set up on your mobile phone.

### Backend Installation
- Navigate to `tunelink-backend`.
- Create a new .env file.
- Go to `https://drive.google.com/file/d/1CXZcNirtCNC43OU_aRnYcX-yG6y0CEGw/view?usp=sharing`, download the file and copy its contents to the .env file you created.
- Navigate to `tunelink-backend/data`.
- Unzip `test_data.zip` inside `/data`.
- Navigate inside created `test_data` directory and navigate to `test_audio`, remove files inside this directory.
- Go to `https://drive.google.com/drive/folders/1vvtAXnvMvA6ErBT0sbgSsn79shp8YUKL?usp=sharing` to download uncompressed audio files, place them in `test_audio` directory. These samples are used in testing and creating a mock social environment in the application. Apple cannot play corrupted audio files, compression corrupts it, that's why we need this extra step. If you want, you can add your own mp3 files.
- Run `npm i`.

### Frontend Installation
- Navigate to `tunelink-frontend`.
- Run ifconfig on Mac, run ipconfig on Windows. Scroll to find `en0`, and there copy `inet` value, it should be like `172.31.176.131`, this is your backend's ip.
- Copy the inet value into `.env` inside `tunelink-frontend`. You will have to repeat this step if you change networks
- Do not change port value unless you have changed it on the backend
- Make your account in Expo Go.
- Run `npm i`.

## Running the application
- Open two terminals
- In one terminal navigate to `tunelink-backend` and run `npm test -- tests/uploadRoutes.tests.js`. This will populate the database with sample users. You don't have to do this each time you want to run the app, but it is good to have a fresh start.
- After the uploads are complete run `npm start`, it should print server listening, you can now use the API.
- On the other terminal navigate to `tunelink-frontend` and run `npm start`, it should show a QR code, please scan the code with your phone, you should have an account in Expo Go already.
- You should be in the application now, you can create account and browse.

## Running tests
- Navigate to `tunelink-backend`.
- We need to run each test separately to not introduce a race condition across tests. Each test will drop the database, this is to make a consistent environment each time.
- Wait until completion of each test.
- Run `npm test -- tests/app.test.js`
- Run `npm test -- tests/auth.test.js`
- Run `npm test -- tests/fileRoutes.test.js`
- Run `npm test -- tests/postRoutes.test.js`
- Run `npm test -- tests/userRoutes.test.js`
- Run `npm test -- tests/uploadRoutes.test.js`

Tests cover each route in the API, and covers controller logic of each route. You can also test with Postman with your own queries.


email authors with any questions. Feel free to browse tickets on our project on GitHub Projects of the organization.
