# 🌤️ Weather App

A clean, responsive Weather App built with pure **HTML**, **CSS**, and **JavaScript** that fetches real-time weather data from the **OpenWeatherMap API** and displays temperature, humidity, and wind speed for any city in the world.

---

## 📸 Preview

| Default State | Weather Result | Error State |
|---|---|---|
| Search box with placeholder | City weather card with data | Invalid city name message |

---

## ✨ Features

- 🔍 **City Search** — Enter any city name to get live weather data instantly
- 🌡️ **Temperature** — Displays current temperature in °C
- 💧 **Humidity** — Shows the current humidity percentage
- 💨 **Wind Speed** — Displays real-time wind speed in km/h
- 🌤️ **Dynamic Weather Icons** — Icons change based on weather condition (Clear, Clouds, Rain, etc.)
- 🎨 **Dynamic Background** — Card gradient changes color based on weather conditions (warm tones for hot, cool tones for cold/rainy)
- ❌ **Error Handling** — Displays a friendly "Invalid city name!" message for unrecognized city inputs

---

## 🛠️ Built With

- **HTML5** — Markup and structure
- **CSS3** — Styling, gradients, Flexbox layout, transitions
- **JavaScript** — API calls, DOM manipulation, async/await
- **OpenWeatherMap API** — Free weather data API


---

## ⚙️ How It Works

1. User types a city name into the search box and clicks the search button (or presses Enter)
2. JavaScript captures the input and constructs the API request URL using the city name and API key
3. A `fetch()` call is made to the OpenWeatherMap current weather endpoint
4. The JSON response is parsed to extract:
   - City name
   - Temperature (converted from Kelvin to °C)
   - Humidity percentage
   - Wind speed in km/h
   - Weather condition ID (used to pick the right icon and background)
5. The DOM is dynamically updated to display all weather information
6. If the city is not found (API returns `cod: 404`), an error message is shown

---

## 🔑 API Reference

This project uses the **OpenWeatherMap Current Weather API**:

```
https://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}&units=metric
```

| Parameter | Description |
|---|---|
| `q` | City name entered by the user |
| `appid` | Your personal OpenWeatherMap API key |
| `units=metric` | Returns temperature in Celsius |


---

## ⚠️ Common Issues

**401 Invalid API Key**
> Make sure the API key is correctly copied and activated. New keys from OpenWeatherMap may take up to an hour to activate after registration.

**City Not Found**
> Double-check the spelling of the city name. The app will display "Invalid city name!" for unrecognized inputs.

---


## 🙏 Acknowledgements

- [OpenWeatherMap](https://openweathermap.org/) for the free weather API
- Inspired by the **Easy Tutorials** YouTube channel

---
