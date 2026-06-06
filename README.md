# 🚌 GRT Stop Request App

A proof-of-concept web app that lets passengers on Grand River Transit (GRT) buses in Kitchener-Waterloo digitally request a stop — replacing or supplementing the physical stop-request button when it's broken or unavailable.

---

## 🧩 The Problem

Many GRT buses have broken or unreliable stop-request buttons (the red strip you press to signal your stop). This app provides a digital alternative: passengers tap a button on their phone, and the bus driver sees a real-time alert on a dashboard.

---

## 💡 How It Works

1. **Passenger opens the web app** on their phone
2. **Selects their bus route** (e.g. iXpress 200, Route 7, etc.)
3. **Taps "Request My Stop"**
4. A real-time signal is sent via **Firebase Realtime Database**
5. The **driver's dashboard** (open on a mounted tablet or phone) shows a flashing stop request alert

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React (Progressive Web App) |
| Real-time DB | Firebase Realtime Database |
| Push Notifications | Firebase Cloud Messaging (FCM) |
| Route Data | GRT GTFS Open Data (free, public) |
| Hosting | Firebase Hosting |

---

## 📁 Project Structure

```
grt-stop-request/
├── public/
│   └── index.html
├── src/
│   ├── passenger/
│   │   ├── PassengerView.jsx       # Route selector + stop request button
│   │   └── PassengerView.css
│   ├── driver/
│   │   ├── DriverDashboard.jsx     # Real-time alert display for drivers
│   │   └── DriverDashboard.css
│   ├── firebase.js                 # Firebase config + DB connection
│   └── App.jsx
├── .env                            # Firebase credentials (not committed)
├── .gitignore
├── package.json
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v18+)
- A free [Firebase](https://firebase.google.com) account

### Installation

```bash
git clone https://github.com/your-username/grt-stop-request.git
cd grt-stop-request
npm install
```

### Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com) and create a new project
2. Enable **Realtime Database**
3. Enable **Cloud Messaging** (for push notifications)
4. Copy your Firebase config into a `.env` file:

```env
REACT_APP_FIREBASE_API_KEY=your_api_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
REACT_APP_FIREBASE_DATABASE_URL=https://your_project.firebaseio.com
REACT_APP_FIREBASE_PROJECT_ID=your_project_id
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
REACT_APP_FIREBASE_APP_ID=your_app_id
```

### Run Locally

```bash
npm start
```

- **Passenger view:** `http://localhost:3000/passenger`
- **Driver dashboard:** `http://localhost:3000/driver`

---

## 🗺️ Route Data

This app uses GRT's publicly available **GTFS (General Transit Feed Specification)** data, which includes all routes, stops, and schedules.

- Download: [Region of Waterloo Open Data](https://www.regionofwaterloo.ca/en/living-here/grt-open-data.aspx)
- Format: CSV files (`routes.txt`, `stops.txt`, `trips.txt`)

---

## 📱 Features

### Passenger App
- [x] Select bus route from a list
- [x] One-tap stop request
- [x] Confirmation feedback ("Stop requested!")
- [ ] Auto-detect nearby route via GPS *(planned)*
- [ ] Accessibility mode (larger button, screen reader support) *(planned)*

### Driver Dashboard
- [x] Real-time stop request alerts
- [x] Shows route number and request time
- [x] Audio alert on new request
- [ ] Mark request as acknowledged *(planned)*
- [ ] Multi-passenger queue view *(planned)*

---

## 🔒 Privacy

- No user accounts or login required
- No personal data collected
- Requests are anonymous and ephemeral (cleared after the stop is acknowledged)

---

## 🤝 Contributing & Next Steps

This is a proof-of-concept intended for demonstration to **GRT / Region of Waterloo** as part of their Smart Cities initiative.

If you'd like to contribute or help move this toward a real pilot program:

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes
4. Open a pull request

To contact the Region of Waterloo about transit innovation:
👉 [regionofwaterloo.ca](https://www.regionofwaterloo.ca)

---

## 📄 License

MIT License — free to use, modify, and distribute.
