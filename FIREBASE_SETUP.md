# 🔐 Firebase Login Setup Guide

Your login system needs Firebase configuration to work! Follow these steps:

## Step 1: Create a Firebase Project

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Add project" or select an existing project
3. Name it something like "PercysWorld"
4. Disable Google Analytics (not needed for login)

## Step 2: Enable Email/Password Authentication

1. In your Firebase project, go to **Authentication** (left sidebar)
2. Click **Sign-in method**
3. Click **Email/Password**
4. Enable "Email/Password" 
5. Click **Save**

## Step 3: Register Your App

1. Go to **Project Settings** (gear icon top left)
2. Scroll down to "Your apps"
3. Click **Web** (</>) icon
4. Give it a nickname (like "PercysWorld")
5. Click **Register app**
6. Copy the **firebaseConfig** object shown

## Step 4: Update login.html

1. Open `login.html` in your code editor
2. Find the `firebaseConfig` section (around line 170)
3. Replace the placeholder values with your actual Firebase values:

```javascript
const firebaseConfig = {
    apiKey: "YOUR_ACTUAL_API_KEY",
    authDomain: "your-project.firebaseapp.com",
    projectId: "your-project-id",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

## Step 5: Test It!

1. Open `login.html` in your browser
2. Try signing up with a Gmail email
3. Check your email (and spam folder) for the verification link
4. Click the verification link
5. You should be able to login!

## ⚠️ Important Notes

- **Email verification** is automatic - new users MUST verify their email before logging in
- The login page shows verification status
- Users can resend the verification email from the login page
- Firebase has a free tier that should be more than enough for this

## Troubleshooting

**"No account found"** → The email isn't registered yet. Use Sign Up!

**"Too many attempts"** → Firebase blocks after too many failed attempts. Wait 15-30 minutes.

**Not receiving emails** → Check spam folder! Also make sure you enabled Email/Password in Firebase Console.

## Need Help?

Ask Percy if you get stuck! 🐱⚡