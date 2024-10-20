# MindChat - Real-time Chat Application

MindChat is a real-time chat application built with Svelte and Firebase. It allows users to log in with their Google account and participate in a global chat room.

## Features

- Google Authentication
- Real-time messaging
- User avatars
- Responsive design

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Node.js (v14 or later)
- npm (v6 or later)
- A Firebase account

## Project Setup

1. Clone the repository:
   ```
   git clone https://github.com/willianctti/mindchat-svelte
   cd mindchat-svelte
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a `src/firebase.js` file with your Firebase configuration:
   ```javascript
   import { initializeApp } from 'firebase/app';
   import { getAuth, GoogleAuthProvider } from 'firebase/auth';
   import { getFirestore } from 'firebase/firestore';

   const firebaseConfig = {
     // Your Firebase configuration object goes here
   };

   const app = initializeApp(firebaseConfig);
   export const auth = getAuth(app);
   export const googleProvider = new GoogleAuthProvider();
   export const db = getFirestore(app);
   ```

4. Start the development server:
   ```
   npm run dev
   ```

5. Open your browser and navigate to `http://localhost:8080`

6. You should now see the MindChat application running. You can log in with your Google account and start chatting!
