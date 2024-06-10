Weather App


Overview

This is a React-based weather application that fetches and displays the current weather information for a specified location. By default, it shows the weather for New Delhi. Users can search for weather information in other locations using the search bar.

Features

Displays current weather conditions such as temperature, humidity, and wind speed.
Provides weather icons and background images corresponding to the current weather.
Allows users to search for weather information by entering a location.
Displays a loading animation while fetching data.
Shows a "Not Found" message if the location entered is invalid.


Technologies Used

React: JavaScript library for building user interfaces.

OpenWeatherMap API: Provides weather data.

CSS: For styling the application.

Prerequisites


Node.js: Ensure you have Node.js installed on your machine.
Getting Started
Follow these steps to run the application locally:

Clone the repository:

bash
Copy code
git clone <>
cd <weatherapp>

Install dependencies:

bash
Copy code
npm install
Add your OpenWeatherMap API key:
Replace the placeholder API key in the code (b30e91a303363a894619ce94e221eca2) with your own key. You can obtain an API key by signing up on the OpenWeatherMap website.

Run the application:

bash
Copy code
npm start
Open the application:
Open your web browser and navigate to http://localhost:3000.

Code Explanation

Main Components

WeatherApp: The main component that handles the state and logic of the application.

State Variables:

data: Stores the weather data fetched from the API.
location: Stores the location input by the user.
loading: Boolean indicating whether data is being fetched.

Effect Hook:

Fetches weather data for the default location (New Delhi) when the component mounts.

Event Handlers:

handleInputChange: Updates the location state when the user types in the search bar.
search: Fetches weather data for the entered location when the search button is clicked or the Enter key is pressed.
handleKeyDown: Triggers the search function on pressing the Enter key.
Weather and Background Images:
Maps weather conditions to corresponding images and background styles.

Date Formatting:
Formats and displays the current date.

UI Components
Search Bar: Allows users to enter a location to fetch weather data.
Weather Display: Shows weather icon, type, temperature, humidity, and wind speed.
Loading Animation: Displays while fetching data.
Error Message: Displays if the location is not found.
Known Issues
The application does not handle network errors gracefully. If the fetch request fails (e.g., due to network issues), the app does not provide feedback to the user.
The API key is hardcoded in the source code, which is not secure. Consider using environment variables to store sensitive information.


Future Improvements

Add error handling for network requests.
Implement responsive design for better mobile support.
Enhance the UI with more detailed weather information (e.g., forecast, sunrise/sunset times).
Store the API key securely using environment variables.