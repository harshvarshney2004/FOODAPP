Here's a `README.md` file that documents your C++ food ordering application:

---

# FOODinTHRIVE 🍔🍟

A command-line C++ application simulating a food ordering system with features like restaurant selection, menu browsing, price and ETA filtering, payment, and coupon discounts.

---

## 🚀 Features

- User-friendly terminal interface for selecting place of stay
- Displays nearby restaurants based on ETA (using Dijkstra’s algorithm)
- Filter restaurant list by **Price** or **ETA**
- Interactive menu selection with quantity-based pricing
- Payment method simulation (Cash, Card, UPI)
- Coupon validation for discounts (`FREE25`, `SAVE25`, `HUGE`, `EASTY`)
- Final route displayed from stay to restaurant

---

## 🛠 Technologies Used

- **C++** (Standard Template Library)
- **Graph Algorithms** – Dijkstra's algorithm for shortest ETA
- **Data Structures**:
  - `unordered_map` for fast mapping of places and menu data
  - `vector`, `set`, `pair` for storing restaurant and menu information

---

## 🧾 How It Works

1. **Place Selection**  
   User selects their current place of stay from a list.

2. **Nearby Restaurants**  
   Using Dijkstra’s algorithm, restaurants are sorted based on shortest travel time from the user’s location.

3. **Filter Options**  
   User can filter restaurant listings by:
   - Lowest to Highest **Price**
   - Lowest to Highest **ETA**

4. **Menu Selection**  
   The user browses the menu of a chosen restaurant and adds items with desired quantities.

5. **Apply Coupon**  
   Option to apply a discount coupon. Valid coupons apply a 25% discount.

6. **Payment Method**  
   Simulates a payment process (card, UPI, or cash).

7. **Order Summary**  
   Displays the final price, route to the restaurant, and ETA + cooking time.

---

## 📁 File Structure

- `main()` – Entry point of the application.
- `markings()` – Initializes the map of stay and restaurant places.
- `addEdges()` – Connects the locations (edges in graph).
- `dijkstra(int rest)` – Calculates shortest distance (ETA) from user's location.
- `addMenus()` – Initializes menus for each restaurant.
- `printmenu()` – Handles user menu selection and pricing logic.
- `printPath(int cur)` – Displays path from user's location to restaurant.

---

## 🎟 Available Coupons

You can apply one of the following coupons for a 25% discount:
- `FREE25`
- `SAVE25`
- `HUGE`
- `EASTY`

---

## 💡 Sample Output

```
            FOODinTHRIVE
    Where are you currently staying at?
    1. Hostel
    2. Home
    ...
    
    Top Picks for you:
    1. McDonalds - Rs129 - ETA 10 mins
    2. The Chef - Rs100 - ETA 12 mins
    ...
    
    Enter your restaurant choice:
    View Menu
    Select items and quantity
    Enter coupon
    Choose payment method
    ...
    Food is Preparing
    Delivery ETA: 12 minutes + 20 minutes cooking time
    Path: Home -> Sector 15 -> McDonalds
```

---

## 🔧 Future Improvements

- Add support for online order tracking
- Real-time traffic integration for ETA
- GUI version using a framework like Qt
- Persistent database for orders

---

## 📌 Note

- This is a simulation and not connected to real-world APIs or payment gateways.
- Developed for academic/demonstration purposes.

---

## 📄 License

This project is licensed under the MIT License.

---

Let me know if you'd like this formatted as a downloadable `.md` file or need help customizing it further!
