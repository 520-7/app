# Tunelink CS520 Project
Made by Ozel Yilmazel, Aryan Nair, Hanna Jiang, Rachel Lahav, Ryan Zaid

# For Graders
1. URL FOR THIS REPOSITORY: `https://github.com/520-7/app`
2. We have organized our code in submodules, this repository is a parent repository to obey submission guidelines.
3. Source code can be found in the repos linked in in this repository, one for the frontend and one for the backend. [Tunelink Frontend Repository](https://github.com/520-7/tunelink-frontend) [Tunelink Backend Repository](https://github.com/520-7/tunelink-backend)
4. Test code found in repository folder labelled tests [TuneLink tests](https://github.com/520-7/tunelink-backend/tree/main/tests).
5. Comprehensive ReadMe in each repository, most general overview can be found in the frontend repository at [Tunelink Frontend Repository](https://github.com/520-7/tunelink-frontend).
6. Demo at [TuneLink WalkThrough](https://drive.google.com/file/d/1na2T1S1jm1Wh_7zE_rlJNU153vUyQzkb/view)

## Introduction
TuneLink is a mobile social media platform designed to help music enthusiasts discover and share music through short snippets. The app allows users to link their snippets to Spotify or YouTube for full song access, encouraging both discovery and promotion of new music. Users will be able to interact with the music snippets through likes and follows, creating a vibrant community centered around music sharing and discovery.

### Demo Video
[TuneLink WalkThrough](https://drive.google.com/file/d/1na2T1S1jm1Wh_7zE_rlJNU153vUyQzkb/view)

## Links to individual code repos
We had to make this parent repository for rubric purposes, you can explore individual components here.

[Tunelink Frontend Repository](https://github.com/520-7/tunelink-frontend)
[Tunelink Backend Repository](https://github.com/520-7/tunelink-backend)

## Installation instructions and configuration
This section will prepare your local copy to run the application and tests.

Please directly clone this repository. Navigate to the cloned directory

Please make sure you have node.js and npm installed. For frontend you also need Expo Go set up on your mobile phone.

### Clone the repo

### Submodules set up
- At the cloned repository root, run `git submodule update --init --recursive`.

### Backend Installation
- Navigate to `tunelink-backend`.
- Create a new .env file.
- Go to `https://drive.google.com/file/d/1CXZcNirtCNC43OU_aRnYcX-yG6y0CEGw/view?usp=sharing`, download the file and copy its contents to the .env file you created.
- Navigate to `tunelink-backend/data`.
- Unzip `test_data.zip` inside `/data`.
- Navigate inside created `test_data` directory and navigate to `test_audio`, remove files inside this directory.
- Go to `https://drive.google.com/drive/folders/1vvtAXnvMvA6ErBT0sbgSsn79shp8YUKL?usp=sharing` to download uncompressed audio files. Download each individually and place them in `test_audio` directory. These samples are used in testing and creating a mock social environment in the application. Apple cannot play corrupted audio files, compression corrupts it, that's why we need this extra step. If you want, you can add your own mp3 files.
- Run `npm i`.

### Frontend Installation
- Navigate to `tunelink-frontend`.
- Run ifconfig on Mac, run ipconfig on Windows. Scroll to find `en0`, and there copy `inet` value, it should be like `172.31.176.131`, this is your backend's ip. The IPv4 address on windows will be what you need.
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

## Contributions
- Ozel Yilmazel: Backend server, post routes, user routes, mongodb integration, recommendation algorithm, upload post functionality, bug patches, backend API tests

Email authors with any questions. Feel free to browse tickets on our project on GitHub Projects of the organization.
