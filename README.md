
---

# Route Planner – Real-Time Navigation Website


## **Overview**

Route Planner is an interactive web application that allows users to plan optimal routes in real-time using Google Maps. Leveraging the **Traveling Salesman Problem (TSP)** algorithm, Distance Matrix, and Google Directions API, this tool helps commuters efficiently plan multi-stop journeys. Users can select travel modes, visualize step-by-step directions, and interact with the map for precise location management.

---

## **Features**

* **Real-Time Marker Placement:** Click anywhere on the map to drop a marker. Each marker automatically fetches the address using reverse geocoding.
* **Travel Mode Selection:** Choose between Driving, Walking, Bicycling, and Transit.
* **Optimized Routes:** Calculates the shortest possible route for multiple waypoints using the TSP algorithm and Distance Matrix API.
* **Step-by-Step Directions:** View directions for each segment of the journey with distance and duration details.
* **Dynamic Map Interaction:** Drag markers to update routes and addresses in real-time.
* **User Location Compass:** Center the map on your current location with one click.
* **Responsive UI:** Minimal and intuitive interface with dropdowns, collapsible steps, and real-time updates.
* **Custom Polyline Animations:** Routes are visually drawn on the map with smooth animations.
* **Route Removal:** Clear all directions instantly to reset the map.

---

## **How It Works**

1. **Marker Placement:** Users place markers on the map representing destinations.
2. **Distance Calculation:** The app uses Google Distance Matrix API to calculate travel times between all markers.
3. **Optimal Path Calculation:** Implements a recursive TSP algorithm with memoization to determine the route with the minimum travel time.
4. **Directions Rendering:** The Google Directions API provides detailed step-by-step instructions for each leg of the route.
5. **Interactive Map Features:** Users can drag markers, click the compass to center the map, or select travel modes to dynamically update routes.

---

## **Technologies Used**

* **Frontend:** React.js
* **Google Maps Integration:**

  * `@react-google-maps/api` for map rendering and markers
  * `react-places-autocomplete` for address search
  * Google Distance Matrix API & Directions API for routing
* **UI Components:** Material-UI (`IconButton`, `DeleteIcon`) for interactive elements
* **Animation & Interaction:** Custom polyline animations for route drawing
* **State Management:** React `useState`, `useRef`, and `useCallback`

---

## **Why This Project Is Unique**

* Combines **real-time geolocation**, **TSP optimization**, and **step-by-step directions** in one seamless map interface.
* Fully **interactive and dynamic**—markers can be added, removed, or dragged to instantly recalculate routes.
* Supports **multiple travel modes** and intelligently adjusts routes for each mode.
* Provides **animated route visualization** for better user experience, unlike standard map directions that instantly render static routes.
* Lightweight, responsive, and easy to use, suitable for commuters, delivery planning, or logistics simulation.

---

## **Setup & Installation**

1. Clone the repository:

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file and add your Google Maps API Key:

```
REACT_APP_GOOGLE_MAPS_API_KEY=YOUR_API_KEY_HERE
```

4. Run the app:

```bash
npm start
```

5. Open `http://localhost:3000` in your browser.

---

## **Folder Structure**

```
/src
 ├─ /components
 │   ├─ AddressBox.js       # Marker address component with delete option
 │   ├─ Compass.js          # Button to center map on user location
 │   ├─ Directions.js       # Handles route calculation & TSP logic
 │   ├─ DropdownSteps.js    # Step-by-step directions dropdown
 │   └─ InputBox.js         # Google Places autocomplete input
 ├─ /styles
 │   └─ mapStyles.js        # Custom map styling
 └─ App.js                  # Main application component
```

---

## **License**

This project is licensed under the MIT License.

---

