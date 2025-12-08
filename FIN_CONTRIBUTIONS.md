# Individual Contribution

## Contributor Information

- **Name:** Fadhil Hairiman
- **Group Number:** 6
- **Project Title:** MUN Thrift

---

## Contributions

### Contribution 1 

- **Feature/Task:** Authentication
- **Short Description:**
	- Login and signup pages and logic
    - App wide auth state

- **Evidence of Work:**
	- https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/19

- **Reflection:**
	- **Impact on Project:** Users are able to create and login into their accounts with states saved for their items listings and ratings
	- **Challenges Encountered:** Setting up and integrating the firebase project and firebase auth to flutter.

---

### Contribution 2 

- **Feature/Task:** Creating and Edit Listings
- **Short Description:**
	- Form for creating and editing listings
    - Ability to so listings
    - Firebase integration for these pages

- **Evidence of Work:**
	- https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/31

- **Reflection:**
	- **Impact on Project:** Users are able to create item listings for free items, paid items, and trade items through a specialzied form page.
	- **Challenges Encountered:** Making sure the firebase rules for storage are consistent because sometimes it works for a few days, but after those few days users get a warning about storage authentication when they try to make item listing or view chat or order history, so I had to redeploy the firebase rules once in a while. 

---

### Contribution 3 

- **Feature/Task:** Shopping Cart and Checkout
- **Short Description:**
	- 

- **Evidence of Work:**
	- https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/33
    - https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/35
    - https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/31

- **Reflection:**
	- **Impact on Project:** Users are able to see a list of items they want to buy/get for free, edit the list, and checkout the items. It will then send a notification to the seller for them to accept and update the order status. Users can also see the history of items they have bought/sold
	- **Challenges Encountered:** Managing the cart state with Riverpod and ensuring the cart persisted across different screens and app sessions. Had to handle edge cases like removing items from cart, updating quantities, and calculating totals for both free and paid items while maintaining consistent state. 

---

### Contribution 4 

- **Feature/Task:** Order Management
- **Short Description:**
	- Page to see orders
    - Page to see progress of orders
    - Firebase integration for those features

- **Evidence of Work:**
	- https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/37

- **Reflection:**
	- **Impact on Project:** Users can track their orders from placement to completion, view detailed order information including items, status, and delivery details. Sellers can manage incoming orders, update order statuses (pending, accepted, in-transit, completed), and track their sales history. This creates a complete order lifecycle management system for both buyers and sellers.
	- **Challenges Encountered:** Designing a flexible order status system that works for both free items and paid items, and implementing real-time updates so both buyer and seller see status changes immediately. Also had to handle different user views (buyer vs seller) with proper data filtering using Firestore queries.

---

### Contribution 5 

- **Feature/Task:** Notifications
- **Short Description:**
    - Notifications for order updates and chats
	- In app notifications
    - Android push notifications

- **Evidence of Work:**
    - https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/53
    - https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/54
	- https://github.com/eggboixd/gr06-munthrift-fall-2025/pull/55

- **Reflection:**
	- **Impact on Project:** Users can get notification when they recieve new message or have an update on their order so that they won't miss it.
	- **Challenges Encountered:** Implementing the native Android notification was particularly challenging as it required configuring Firebase Cloud Messaging (FCM), setting up notification channels for Android 8.0+, handling permissions, and integrating with Firebase Cloud Functions to trigger notifications from backend events. Had to debug issues with notification delivery, payload handling, and ensuring notifications worked both when the app was in foreground and background states.
