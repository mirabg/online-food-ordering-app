# Online Food Ordering App – Functionality Overview

This web application is a simple, responsive online food ordering system built with HTML, TailwindCSS, and JavaScript. It demonstrates core features commonly found in modern food ordering platforms, including user authentication, menu browsing, cart management, and persistent storage using localStorage.

---

## Key Features

### 1. **User Authentication**
- **Login Page:**  
  Users must log in with a username and password to access the menu.  
  - **Hint:** The default credentials are shown on the login page (`admin` / `admin-password`).
- **Session Management:**  
  On successful login, the username is saved to `localStorage`.  
  If a user is not logged in, they are redirected to the login page when trying to access the menu.

### 2. **Menu Display**
- **Menu Page:**  
  After logging in, users are taken to the menu page, which displays a list of food items (e.g., burgers, fries, pizza).
- **AJAX Loading:**  
  Menu items are loaded dynamically from a menu-items.json file using AJAX.
- **Menu Cards:**  
  Each menu item is shown as a card with an image, name, description, price, and rating.

### 3. **Cart Functionality**
- **Add to Cart:**  
  Each menu card has an "Add to Cart" button. Clicking it adds the item to the cart. If the item already exists in the cart, its quantity increases.
- **Cart Badge:**  
  The cart button in the header displays a badge showing the total number of items in the cart and the total price.
- **Cart Sidebar:**  
  Clicking the cart button toggles a sidebar on the right, showing all cart items.
  - **Quantity Controls:** Users can increase, decrease, or directly edit the quantity of each item.
  - **Remove Items:** Users can remove items from the cart.
  - **Cart Total:** The total price of all items is displayed at the bottom of the sidebar.
- **Persistence:**  
  The cart is saved in `localStorage`, so it persists across page reloads.

### 4. **User Session and Logout**
- **Username Display:**  
  The logged-in username is shown in the header.
- **Logout:**  
  A logout button allows users to end their session, which removes the username from `localStorage` and redirects to the login page.

### 5. **Responsive Design**
- The app uses TailwindCSS for a modern, responsive layout that works well on both desktop and mobile devices.

---

## How It Works

1. **Login:**  
   The user logs in with the provided credentials. On success, they are redirected to the menu page.

2. **Browse Menu:**  
   The menu is loaded via AJAX and displayed as a grid of cards.

3. **Manage Cart:**  
   Users can add items to the cart, adjust quantities, or remove items. The cart sidebar can be toggled from the header.

4. **Session Management:**  
   The app checks for a logged-in user on every page load. If not found, it redirects to the login page.

5. **Logout:**  
   The user can log out at any time, which clears their session and returns them to the login screen.

---

## Technologies Used

- **HTML5**
- **TailwindCSS** (via CDN)
- **Vanilla JavaScript**
- **localStorage** for persistent cart and session data
- **AJAX** for loading menu items

---

This app provides a foundation for a more advanced food ordering system and can be extended with features like order checkout, user registration, and backend integration.