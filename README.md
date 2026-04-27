# 🌤️ Weather App

A clean, responsive weather web app built with **HTML**, **CSS**, and **vanilla JavaScript** that fetches real-time weather data for any city using the **OpenWeatherMap API**.

---

## ✨ Features

- 🔍 **City Search** — Enter any city name to instantly fetch its current weather
- 🌡️ **Temperature** — Displays current temperature in °C
- 💧 **Humidity** — Shows the humidity percentage
- 💨 **Wind Speed** — Displays wind speed in km/h
- 🌤️ **Dynamic Weather Icons** — Icons change based on weather conditions (Clear, Clouds, Rain, etc.)
- 🎨 **Dynamic Gradient Background** — Card gradient shifts with weather/temperature (cool tones for cold, warm tones for hot)
- ❌ **Error Handling** — Shows a friendly "Invalid city name!" message for unrecognized inputs


## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | App structure and layout |
| CSS3 | Styling, gradients, flexbox, transitions |
| JavaScript | API calls, DOM manipulation, logic |
| OpenWeatherMap API | Live weather data source |


## ⚙️ How It Works

1. User types a city name and clicks the search button (or presses Enter)
2. JavaScript captures the input and constructs an API request URL:
   ```
   https://api.openweathermap.org/data/2.5/weather?q={city}&appid={apiKey}&units=metric
   ```
3. The `fetch()` function sends an async GET request to OpenWeatherMap
4. The JSON response is parsed to extract:
   - `main.temp` → Temperature
   - `main.humidity` → Humidity
   - `wind.speed` → Wind Speed
   - `weather[0].main` → Condition (Clear, Clouds, Rain, etc.)
5. DOM is updated dynamically with the fetched values
6. If the API returns a `404` status, the error message is displayed


## 🔑 API Reference

This app uses the **OpenWeatherMap Current Weather Data API**:

```
GET https://api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}&units=metric
```
