# Lab Report: Task 2.1 - Weather Dashboard

### `fetchWeather(city)`
This function is responsible for fetching the current weather data for a given city. It constructs a URL for the OpenWeatherMap API with the provided city and API key. It then uses the `fetch` API to make an asynchronous request and returns the weather data as a JSON object.

### `fetchForecast(city)`
Similar to `fetchWeather`, this function fetches the 5-day weather forecast. It calls a different OpenWeatherMap API endpoint to get the forecast data. The function handles the asynchronous API call and returns the forecast data in JSON format.

### `displayWeather(data)`
This function takes the current weather data object and dynamically creates HTML to display it. It populates the `weatherDisplay` element with details like the city name, temperature, and weather conditions. This provides a user-friendly view of the current weather.

### `displayForecast(data)`
This function is used to render the 5-day weather forecast. It filters the forecast data to show one entry per day and creates a grid of forecast items. Each item displays the day, a weather icon, and the temperature, which are then appended to the `forecastDisplay` element.

### `searchWeather(cityFromRecent)`
This function orchestrates the weather search process. It retrieves the city from the input field or a recent search, calls `fetchWeather` and `fetchForecast` to get the data, and then uses `displayWeather` and `displayForecast` to update the UI. It also manages loading states and error handling.

### `saveRecentSearch(city)`
To provide a better user experience, this function saves the user's recent searches to `localStorage`. It maintains a list of the 5 most recent unique city searches. This allows users to quickly re-run a search for a previously entered city.

### `loadRecentSearches()`
This function retrieves the list of recent searches from `localStorage` when the page loads. It then dynamically creates and displays clickable elements for each recent search. This allows for quick access to weather information for frequently checked locations.

### `showError(message)`
This function is a simple utility to display error messages to the user. It takes an error message string and sets the `innerHTML` of the `errorMessage` div. This provides clear feedback to the user if an API call fails or input is invalid.

### `clearError()`
This utility function is used to clear any previously displayed error messages. It simply clears the `innerHTML` of the `errorMessage` div. This is typically called before a new search is initiated to reset the UI state.
