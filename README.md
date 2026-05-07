# Foodweb Project

This project is now a static HTML site plus a small Node server that gives `admin.html` and `menu.html` one shared product catalog.

## Run the project

1. Make sure Node.js is installed.
2. From the project root, run `npm start`.
3. Open `http://localhost:3000/admin.html` to manage products.
4. Open `http://localhost:3000/menu.html` to view the live menu.

When the server starts for the first time, it creates `data/products.json` automatically by seeding from the current menu page. After that, admin changes are written to that file, so the catalog is shared across refreshes, browser sessions, and devices using the same project/server.

## Structure

- `admin.html` - Admin dashboard for product management
- `menu.html` - Public menu page
- `server.js` - Dependency-free Node server and shared product API
- `data/products.json` - Shared catalog file created automatically on first run
- `assets/` - Static CSS, JavaScript, images, and fonts

## Notes

- If you open the HTML files directly without `npm start`, the menu page falls back to its built-in static markup.
- Uploaded admin images are saved into the shared catalog as resized data URLs so they can publish with the product data.
