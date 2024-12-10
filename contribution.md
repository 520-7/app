# Contributions
- Ozel Yilmazel: Backend server, post routes, user routes, mongodb integration, recommendation algorithm, upload post functionality, bug patches, backend API tests.
  - Backend is used to efficiently communicate with mongodb and abstracts details for the frontend. It handles many types of functionality to support a social media. Frontend uses these routes all throughout the application. Recommendation algorithm is used by the frontend feed-screen to show appropriate posts to users. Upload post screen allows users to select images and audio from device's own storage. Fixed bugs throughout the app. Wrote the testing suite for the application, testing suite tests each route with high coverage. Used Node.js and express, and jest for testing. Frontend used react-native and paper components library.
  - Backend was used by everyone while developing the frontend
  - Tests were used to satisfy CI/CD
  - Provided functional code for make post screen, profile screen, and edit profile screen, these screens were later on styled by Hanna and added more functionality by Ryan.
  - Fixed bugs in genre search in backend and fixed the tests associated with the route.

- Ryan Zaid: Designed and wrote code for the base layout for the profile screen, following screen, edit profile screen, and search screen.
  - Utilized React Native and Paper.
  - Handled screen switching. Implementation relied on passing a userId through various screens via a stored param list, making navigation seamless and more secure.
  - Data was fetched at each screen based on userId from MongoDB, leaving less room for vulnerability in passing of data.
  - This was an expansion on the base design of the entire frontend designed by Aryan. Aryan started with implementing the Signup, Onboarding, and Feed screens in order to establish a color scheme and base code structure.
  - Hanna and Rachel further expanded on these, making them more readable and usable by honing in their design
- Linked the frontend to the backend using fetch requests
  - handled error in which a user's IP address needed to be passed into requests and handled on the server
  - fixed backend "PUT" requests to allow for updating images. Uploading of images ("POST") was handled by Ozel within the user authentication route accessed by the signup screen, but no routing was implemented for the changing of these images. This was important to allow users to change their profile picture
- Miscellaneous bugs
  - error handling for user not found during search, others

- Hanna Jiang: Profile screen, sign up screen, post screen, feed screen, frontend server requests, minor bug fixes, basic server tests.
  - Different creens allow the user to interaect with the app and see their social network. UI elements from React Native and paper, and connected backend API calls to the frontend for a seamless user experience. The feed page uses the recommendation algorithm and posts held in the Mongo database, and the signup integrates with the baceknd to hold new profiles, as well as encrypts passwords. Bug fixes, usually for type errors.

- Aryan Nair: Sign up screen, login screen, onboarding screen, feed screen, frontend server requests, UI fixes, logo design, integrated feed screen w/ other screens.
   - Created onboarding and feed page with React Native and paper to provide fluid user experience. Frontend server requests to retrieve other user data and authenticate user. Feed page is the main page, so tried variations of it (Instagram, Spotify like posts) until decided on the final design that fit with the project.

- Rachel Lahav: Genre search, login/signup screen, minor bug fixes, quality testing
  - Genre search allow users to search up 5 random accounts who share the genre of interest. Login and signup essential to onboarding, done in React Native and paper. Quality checks in code for formatting and commenting code.
