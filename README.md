# AWS Lambda Weather Function 🌤️

This is a simple AWS Lambda function written in Node.js that fetches real-time weather data from the OpenWeatherMap API based on a provided city name.

## 🧠 Features

- Uses HTTPS to call an external API
- Returns temperature and weather description
- Accepts city input via query string (`?city=Austin`)
- Handles errors and logs output
- Uses environment variable for API key

## 🛠️ How It Works

The function takes a city name from the `queryStringParameters` in the event object and uses the OpenWeatherMap API to fetch current weather data in imperial units (°F).

Example API URL it constructs:

https://api.openweathermap.org/data/2.5/weather?q=Austin&appid=YOUR_API_KEY&units=imperial

## 📦 Environment Variable

| Key                  | Description                       |
|----------------------|-----------------------------------|
| `OPENWEATHER_API_KEY` | Your OpenWeatherMap API key       |

## 🧪 Sample Test Event (AWS Console)

```json
{
  "queryStringParameters": {
    "city": "Austin"
  }
}
