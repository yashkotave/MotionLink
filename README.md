# MotionLink

Real-time location tracking app built with Node.js, Express, Socket.IO, and Leaflet that updates live device movement on the map.

## Features

* Real-time live location tracking
* Continuous location updates using Geolocation API
* Multi-user tracking with unique Socket.IO connections
* Live marker updates on Leaflet map
* Automatic marker removal when a user disconnects
* Mobile testing support using ngrok with HTTPS
* OpenStreetMap integration for map tiles

## Tech Stack

* Node.js
* Express.js
* EJS
* Socket.IO
* Leaflet.js
* HTML
* CSS
* JavaScript
* ngrok (for mobile testing)

## Project Structure

```text
MotionLink/
│
├── public/
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       └── script.js
│
├── views/
│   └── index.ejs
│
├── app.js
├── package.json
└── README.md
```

## Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd MotionLink
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run the server

```bash
node app.js
```

or

```bash
nodemon app.js
```

### 4. Open in browser

```text
http://localhost:3000
```

## Mobile Testing

For mobile geolocation testing, use ngrok for HTTPS access.

### Install ngrok

```bash
npm install -g ngrok
```

### Start ngrok

```bash
ngrok http 3000
```

Use the generated HTTPS URL on your mobile browser.

## How It Works

1. Browser checks for geolocation support
2. `watchPosition()` continuously tracks user location
3. Latitude and longitude are sent using Socket.IO
4. Server broadcasts live location updates to all connected users
5. Leaflet updates markers on the map in real time
6. When a user disconnects, their marker is removed

## Future Improvements

* User authentication
* Custom user profile markers
* Route history tracking
* Distance calculation
* Geofencing alerts
* Admin dashboard
* Database integration

## Author

Yash
