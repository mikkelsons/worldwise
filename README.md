# WorldWise

WorldWise is a React-based web application that helps users track their travel adventures on an interactive world map. Users can log cities they've visited, mark locations, and explore their travel history with ease. The app features user authentication, dynamic routing, lazy-loaded components for performance optimization, and an interactive map powered by Leaflet.

I built this application as a project in the Udemy course "The Ultimate React Course 2025: React, Next.js, Redux & More" taught by Jonas Schmedtmann.

## Features

- **User Authentication**: Secure login system with protected routes to ensure only authenticated users can access the main application.
- **Interactive Map**: Powered by `react-leaflet`, users can view cities as markers, click to add new locations, and use geolocation to center the map.
- **City Tracking**: Users can add and view cities they've visited, with details displayed in a list and on the map.
- **Dynamic Routing**: Built with `react-router-dom` for seamless navigation between pages like Home, Login, Pricing, Product, and the main App layout.
- **Lazy Loading**: Pages are lazy-loaded with `React.lazy` and `Suspense` to optimize performance.
- **Context API**: Manages global state for authentication (`FakeAuthContext`) and city data (`CitiesContext`).
- **Responsive Design**: Styled with modular CSS (CSS Modules) for a consistent and responsive UI.
- **Protected Routes**: Ensures only authenticated users can access the main app using a `ProtectedRoute` component.
- **Geolocation**: Users can use their current location to center the map with a custom `useGeolocation` hook.

## Tech Stack

- **Frontend**: React, React Router, React Leaflet
- **State Management**: React Context API
- **Styling**: CSS Modules
- **Map Integration**: Leaflet via `react-leaflet`
- **Build Tool**: Vite

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/worldwise.git
   cd worldwise
   ```

2. Install dependencies:

   ```bash
    npm install
   ```

   or

   ```bash
   yarn install
   ```

3. Start the fake server (required for city data):

   ```bash
   npm run server
   ```

   This runs json-server to provide a mock API at http://localhost:8000/api/cities using the data/cities.json file, with a 1-second delay to simulate real network requests.

4. Start the development server in a separate terminal:
   ```bash
   npm run dev
   ```
   or
   ```bash
   yarn dev
   ```
   The app should now be running at http://localhost:5173

## Usage

1. **Homepage**: Visit the root URL (`/`) to see the landing page with a call-to-action to start tracking travels.
2. **Login**: Navigate to `/login` and use the pre-filled credentials (`jack@example.com`, `qwerty`) for development purposes.
3. **Main App**: After logging in, you'll be redirected to `/app/cities`, where you can:
   - View a list of cities in the sidebar, fetched from the fake server.
   - Interact with the map to view city markers or add new locations by clicking.
   - Use the "Use your position" button to center the map on your current location.
4. **Other Pages**:
   - `/product`: Learn about the WorldWise app.
   - `/pricing`: View subscription details (static $9/month plan).
   - Any invalid route will display the `PageNotFound` component.
