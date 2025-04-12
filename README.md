
# 🌦️ Weather Dashboard - MERN Stack

A full-stack weather dashboard built with the MERN stack (MongoDB, Express.js, React, Node.js) that allows users to search for real-time weather conditions by city using the OpenWeatherMap API.

Check it out here: https://hardik-weather-dashboard.netlify.app/

---

## 📁 Project Structure


weather-dashboard/
├── client/                # React frontend
│   ├── src/
│   │   ├── components/
│   │   │   ├── SearchBar.jsx
│   │   │   └── WeatherCard.jsx
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
├── server/                # Express backend
│   ├── routes/
│   │   └── weather.js
│   ├── server.js
│   └── package.json
├── .gitignore
└── README.md


## ⚙️ Functionality

### 🔙 Backend (`/server`)

- Built with **Express.js**, **Axios**, **CORS**, and **dotenv**.
- Provides a single API route:
  ```
  GET /weather?city=CityName
  ```
- Fetches data from OpenWeatherMap API:
  ```
  https://api.openweathermap.org/data/2.5/weather?q=CITY_NAME&appid=API_KEY&units=metric
  ```
- Returns a clean JSON response containing:
  - `temperature`
  - `humidity`
  - `wind_speed`
  - `weather_condition`
  - `icon`
- Handles invalid queries, missing parameters, and API errors gracefully.

---

### 🎨 Frontend (`/client`)

- Built with **Create React App**.
- Two main components:
  - `SearchBar.jsx`: City input and submit button.
  - `WeatherCard.jsx`: Displays weather information in a styled card.
- Uses **Axios** to call the backend API.
- Displays:
  - Loading state
  - Weather info
  - Error messages
- Responsive UI with basic **CSS** or **Bootstrap**.

---

## 🚀 Bonus Features (Optional)

> _Enable these for an even better UX!_

- 🌗 **Dark/Light Mode Toggle**
- 🧠 **Search History** (using `localStorage`)
- 🔍 **City Autocomplete** (via GeoDB Cities API)
- 📆 **5-Day Forecast** (OpenWeatherMap `/forecast` API)
- 🌐 **Deployment**:
  - Backend: Render / Heroku
  - Frontend: Vercel / Netlify

---

## 🛠️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/weather-dashboard.git
cd weather-dashboard
```

---

### 2. Backend Setup (`/server`)
```bash
cd server
npm install
```

> 🔐 Create a `.env` file in `/server`:
```env
OPENWEATHER_API_KEY=your_openweather_api_key
PORT=5000
```

To run the server:
```bash
node server.js
```

---

### 3. Frontend Setup (`/client`)
```bash
cd ../client
npm install
npm start
```

Visit: [http://localhost:3000](http://localhost:3000)

---

## 🌍 API Used

- [OpenWeatherMap](https://openweathermap.org/current)

> Don't forget to sign up and generate your own free API key!

---

## 🧪 Sample API Response

```json
{
  "temperature": 18,
  "humidity": 70,
  "wind_speed": 5,
  "weather_condition": "Cloudy",
  "icon": "04d"
}
```

---

## 📄 .gitignore

Be sure your `.gitignore` excludes:

```gitignore
node_modules/
.env
```

---
---

## 💡 Future Improvements

- 🌦 Weekly Weather Trends
- 📍 Auto-detect user location
- 🔔 Weather Alerts

---

## 🧑‍💻 Author

Made with 💻 by [Hardik Arora](https://github.com/hardik121121)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE)

