# Weather App

A simple, interactive weather application that provides current weather and 5-day forecast information for any city. The app uses the OpenWeatherMap API to retrieve weather data and presents it with a clean, responsive UI.

## Features

* Displays the current weather (temperature, description, humidity, wind speed).
* Shows a 5-day weather forecast with daily temperatures and weather conditions.
* Allows users to search for the weather by typing the name of a city.
* Uses icons from OpenWeatherMap to display weather conditions.
* Automatically updates the weather every 15 minutes.

## Tech Stack

* **Frontend**: HTML, CSS, JavaScript
* **Weather API**: OpenWeatherMap API ([https://openweathermap.org/](https://openweathermap.org/))

## Setup & Installation

To set up this project locally, follow the steps below:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/weather-app.git
   ```

2. **Open the project**:
   Navigate to the project folder and open `index.html` in your web browser.

3. **API Key**:

   * You will need an API key from OpenWeatherMap. You can sign up and get a free API key at [OpenWeatherMap](https://openweathermap.org/).
   * Replace the `appID` value in the `script.js` file with your own API key.

## Usage

1. **Search for a city**: Enter the name of a city in the search bar at the bottom of the app.
2. **View weather details**: Once you enter a city, the app will display the current weather along with a 5-day forecast.

## File Structure

```
/weather-app
  ├── index.html       # Main HTML structure of the app
  ├── style.css        # Stylesheet for the app UI
  ├── script.js        # JavaScript for handling API calls and logic
  └── README.md        # This readme file
```

## Code Explanation

1. **HTML Structure (`index.html`)**:

   * The HTML provides the structure of the app, including sections for displaying the current weather, forecast, and city search input.

2. **CSS Styling (`style.css`)**:

   * The CSS provides styles for the weather cards, the background, and other UI elements. It includes responsive designs, hover effects, and custom fonts.

3. **JavaScript Logic (`script.js`)**:

   * The script makes an HTTP request to the OpenWeatherMap API using Axios to fetch weather data.
   * The current temperature, weather description, and forecast for the next 5 days are displayed dynamically.
   * The weather information is updated automatically every 15 minutes using the `setInterval` function.

4. **Icons**:

   * Weather icons are displayed based on the data returned by OpenWeatherMap using the icon codes.

## Example API Request

The `getWeather` function makes a request to the OpenWeatherMap API to retrieve the weather forecast:

```js
const response = await axios.get('https://api.openweathermap.org/data/2.5/forecast', {
    params: {
        q: city,
        appid: 'YOUR_API_KEY',
        units: 'metric'
    }
});
```

## Contribution

Feel free to fork this repository and contribute by opening a pull request. Contributions such as bug fixes, feature enhancements, and code improvements are always welcome.

## License

This project is open-source and available under the [MIT License](LICENSE).

---

