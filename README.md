1️⃣ Install Dependencies

Inside the project folder:

npm install

2️⃣ Create a .env File

Inside the project root, create:

EXPO_PUBLIC_OPENROUTER_KEY=your_openrouter_key_here

3️⃣ Update app.config.js

Make sure this file exists with:

import "dotenv/config";

export default {
  expo: {
    name: "jebb",
    slug: "jebb",
    extra: {
      openrouterKey: process.env.EXPO_PUBLIC_OPENROUTER_KEY,
    },
  },
};

4️⃣ Add Firebase Config

In src/services/firebaseConfig.js, add your Firebase credentials.

5️⃣ Start Metro + Expo
npx expo start


This opens the Expo Developer Tools.

6️⃣ Run on Your Device or Emulator
To run on Android:
npm run android


or press a in the Expo terminal.

To run on iOS (Mac only):
npm run ios


or press i.

To run on Web:
npm run web

7️⃣ Clear Cache (if needed)

If you face errors:

npx expo start -c
