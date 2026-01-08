# Treenihaaste

A 3-week workout challenge web application that tracks daily push-ups and sit-ups exercises with cloud synchronization.

## Features

- **21-day progressive workout plan** with increasing repetitions
- **Daily tracking** with visual progress indicators
- **Rest days** built into the schedule
- **Google & Apple Sign-In** for cross-device synchronization
- **Cloud storage** with Firebase Firestore
- **Local storage fallback** when not signed in
- **Real-time sync** across devices
- **Responsive design** with dark theme
- **Finnish language interface**

## Workout Schedule

The challenge consists of 3 weeks with 2 rest days per week:
- **Week 1**: 5-9 push-ups, 10-20 sit-ups
- **Week 2**: 10-18 push-ups, 22-35 sit-ups  
- **Week 3**: 20-30 push-ups, 38-60 sit-ups

## Usage

1. Open `index.html` in your web browser
2. **Optional**: Sign in with Google or Apple ID to sync across devices
3. The app automatically highlights today's workout
4. Click "SUORITA!" to mark today's workout as complete
5. Use "POISTA SUORITUS" to undo completion if needed
6. Your progress syncs automatically when signed in

## Setup

### Basic Usage (Local Storage Only)
- Simply open `index.html` - no setup required
- Progress saved locally in browser

### Cloud Sync Setup
1. Follow instructions in `firebase-setup.md`
2. Create Firebase project with Authentication and Firestore
3. Update Firebase config in `index.html`
4. Deploy or serve over HTTPS for authentication to work

## Technical Details

- **Frontend**: Pure HTML, CSS, and JavaScript (ES6 modules)
- **Authentication**: Firebase Auth (Google & Apple)
- **Database**: Firebase Firestore for cloud sync
- **Fallback**: localStorage for offline/guest usage
- **Real-time**: Live sync across signed-in devices
- **Start date**: January 8, 2026

## File Structure

```
Treenihaaste/
├── index.html          # Main application file
├── firebase-setup.md   # Firebase configuration guide
└── README.md          # This file
```

## Security

- User data is private and only accessible by the authenticated user
- Firebase security rules prevent unauthorized access
- No personal data stored beyond what's provided by auth providers