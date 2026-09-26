🗺️ Mapty — Workout Tracking Application
Mapty is an interactive workout tracking web application built with JavaScript, HTML, CSS, Leaflet.js, and OpenStreetMap. The main purpose of this project is to allow users to record their running and cycling workouts by selecting a location directly on an interactive map.

The application first uses the Geolocation API to get the user's current location and displays it on the map. Users can then click anywhere on the map to open the workout form and create a new workout. Depending on the selected workout type, the form dynamically switches between the required fields for running and cycling.

The project is built using Object-Oriented Programming (OOP) with three main classes: Workout, Running, and Cycling. The Workout class works as the base class and contains common workout information such as date, ID, coordinates, distance, and duration. The Running and Cycling classes extend the base class and add their own specific properties and calculations.

For running workouts, the application stores distance, duration, and cadence and uses the calcPace() function to automatically calculate the running pace in min/km. For cycling workouts, it stores distance, duration, and elevation gain and uses the calcSpeed() function to calculate cycling speed in km/h.

The main application logic is handled by the App class. It contains different methods responsible for managing the map, form, workouts, markers, user interactions, and stored data. Functions such as _getPosition() and _loadMap() handle the user's location and map initialization, while _showForm(), _hideForm(), and _toggleElevationField() manage the workout form. The _newWorkout() function handles the complete process of validating user input, creating the appropriate workout object, calculating its statistics, rendering it on the map and workout list, and saving it to Local Storage.

The _renderWorkoutMarker() function creates a marker on the map for every workout and displays workout information through a popup. The _renderWorkout() function dynamically generates the workout card containing information such as distance, duration, pace/speed, cadence, or elevation gain. The _moveToPopup() function allows users to click a workout from the list and automatically move the map to that workout's location.

The project also uses Local Storage for data persistence. The _setLocalStorage() function saves workout data in the browser, while _getLocalStorage() retrieves previously saved workouts when the application is opened again. A reset() function is also included to clear the stored workout data and reset the application.

The project demonstrates practical use of modern JavaScript concepts including classes, inheritance, private class fields, encapsulation, DOM manipulation, event handling, form validation, template literals, array methods, Geolocation API, Local Storage API, and third-party map integration with Leaflet.js.

Overall, this project combines JavaScript OOP concepts with browser APIs and an interactive map to create a practical workout tracking application where users can create, calculate, display, locate, and persist running and cycling workouts.
