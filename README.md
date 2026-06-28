# 💸 SplitSmart Pro — v2.0

## Changes in this version
- **Google-only login** — Phone OTP and Gmail OTP removed
- **Real Firebase Auth** — Uses your Firebase project credentials
- **Account picker** — `prompt: "select_account"` shows only accounts already signed in on the device
- **Scrollable login panel** — Right panel scrolls on smaller screens

## Setup
```bash
npm install
npm run dev   # → http://localhost:5173
```

## Firebase setup
1. Go to https://console.firebase.google.com
2. Your project: `splitsmart-ece78`
3. Authentication → Sign-in method → Enable **Google**
4. Authentication → Settings → Authorized domains → add `localhost` + your deployed domain

## Firebase config (already set)
```js
apiKey:            "AIzaSyCkWB4EDmUNuX_Wu81uin-M8KqfzsmiZlg"
authDomain:        "splitsmart-ece78.firebaseapp.com"
projectId:         "splitsmart-ece78"
storageBucket:     "splitsmart-ece78.firebasestorage.app"
messagingSenderId: "77251465174"
appId:             "1:77251465174:web:4f2a9a0abef30be95ede77"
```

## How Google login works
Clicking "Continue with Google" calls `signInWithPopup` with
`prompt: "select_account"` — the browser shows ONLY the Google accounts
that are already signed in on this device. No manual email entry required.
