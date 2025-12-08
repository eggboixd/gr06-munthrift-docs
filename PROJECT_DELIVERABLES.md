# MUN Thrift - Project Deliverables

## Team Members
| Name   |      Student ID      |
|----------|:-------------:|
| Fadhil Revinno Hairiman |  202514421 |
| Kyle Denief |   202245379    |

---

## 1. Core Features Implementation

### ✅ Free Items Catalog
- **Status**: Yes - Successfully Implemented
- **Description**: Users can browse and order free items from the catalog
- **Implementation**: 
  - Item list screen displaying free items
  - Product detail page showing item info
  - Order button to reserve items
  - Order tracking and management

### ✅ Trade Items Catalog
- **Status**: Yes - Successfully Implemented
- **Description**: Users can browse items available for trade and make trade offers
- **Implementation**: 
  - Trade section in item list screen
  - Product detail page showing trade requirements
  - Trade offer form with item details and image upload
  - Contact information visible in profiles for further communication
  - Trade offer management and status tracking

### ✅ Buy Items Catalog
- **Status**: Yes - Successfully Implemented
- **Description**: Users can browse and purchase items with payment processing
- **Implementation**: 
  - Buy section in item list screen
  - Product detail page with pricing and retrieval info
  - Order button leading to checkout/payment
  - Delivery or self-pickup options
  - Cart system for multiple items
  - Order confirmation and tracking

### ✅ User Profile
- **Status**: Yes - Successfully Implemented
- **Description**: Users can manage their profile with personal information for deliveries
- **Implementation**: 
  - Profile screen with editable fields
  - Name, address, and contact information
  - Profile image upload
  - Delivery address management

### ✅ Reseller Profile
- **Status**: Yes - Successfully Implemented
- **Description**: Resellers can manage their profile and personal information
- **Implementation**: 
  - Dedicated profile editing for resellers
  - Contact information display
  - Profile customization
  - External profile viewing for buyers

### ✅ Reseller Dashboard (Adding, Updating, Removing Items)
- **Status**: Yes - Successfully Implemented
- **Description**: Resellers can manage their inventory through CRUD operations
- **Implementation**: 
  - Create listing screen with image upload
  - Edit item functionality
  - Delete item functionality
  - Item status management (available/sold/reserved)
  - Multiple image support per listing

### ✅ Reseller Logs (Items Ordered by Users)
- **Status**: Yes - Successfully Implemented
- **Description**: Resellers can view and manage orders placed by users
- **Implementation**: 
  - Seller orders screen with order visualization
  - Order details screen with item and buyer information
  - Order status tracking (pending/completed/cancelled)
  - Order history and logs

### ✅ Search
- **Status**: Yes - Successfully Implemented
- **Description**: Users can search for items by name or reseller
- **Implementation**: 
  - Search screen with real-time queries
  - Search by item name
  - Search by reseller name
  - Firestore-powered search functionality

### ✅ Service Delivery
- **Status**: Yes - Successfully Implemented
- **Description**: Delivery option management with on-campus/off-campus handling
- **Implementation**: 
  - Delivery option selection (self-pickup or delivery)
  - On-campus free delivery
  - Off-campus delivery with additional fee
  - Delivery address display for resellers
  - Order tracking with delivery status

---

## 2. Optional Features Implementation

### ✅ Reseller Reviews
- **Status**: Yes - Successfully Implemented
- **Description**: Users can review resellers after purchasing items
- **Implementation**: 
  - Review submission after purchase
  - Reviews displayed on reseller profiles
  - Rating system integrated with Firestore
  - Review service for managing feedback
- **Notes**: Reseller response to reviews - Not Implemented (time constraints)

### ❌ Reseller Listing Statistics
- **Status**: No - Not Implemented
- **Reason**: Time constraints and complexity of analytics implementation
- **Proposed Features**: 
  - View count tracking
  - Screen time analytics
  - Click tracking
  - Chart visualizations for statistics

### ✅ User and Reseller Chat Feature
- **Status**: Yes - Successfully Implemented
- **Description**: In-app messaging between buyers and resellers
- **Implementation**: 
  - Chat list screen showing all conversations
  - Real-time chat screen with Firebase integration
  - Conversation initiation from item listings
  - Message timestamps and delivery status
  - Chat service with real-time updates

### ❌ Price Drop Notifications
- **Status**: No - Not Implemented
- **Reason**: Time constraints and feature prioritization
- **Proposed Features**: 
  - Item watchlist functionality
  - Price tracking system
  - Email or push notifications on price drops

### ✅ Advanced Search Features / Filtering
- **Status**: Yes - Successfully Implemented
- **Description**: Advanced filtering and search capabilities
- **Implementation**: 
  - Filter by category (Free/Trade/Buy)
  - Filter by price range
  - Filter by item condition
  - Filter by size and color (for applicable items)
  - Filter by item type
  - Real-time search with multiple filter combinations

### ⚠️ Payment
- **Status**: Partially Implemented
- **Description**: Basic payment flow without third-party integration
- **Implementation**: 
  - Checkout screen with order summary
  - Payment confirmation (dummy implementation)
  - Order processing without actual payment gateway
  - Cash-on-delivery option available
- **Why Not Fully Implemented**: Third-party payment APIs (Stripe) and bank account linking were not integrated due to time constraints and complexity. The focus was on core functionality rather than payment gateway integration 
 
---

## 3. Project Structure Overview

### Directory Structure

#### **`lib`**
- `main.dart` - Application entry point, Firebase initialization
- `router.dart` - GoRouter configuration for navigation
- `firebase_options.dart` - Firebase configuration

#### **`lib/screens/`** - UI Screens
Contains all the app's user interface screens (22 screens total):
- **Authentication**: `login_screen.dart`, `signup_screen.dart`, `forgot_password_screen.dart`
- **Main Navigation**: `bottom_nav_bar.dart`, `item_list_screen.dart`, `search_screen.dart`, `profile_screen.dart`
- **Shopping**: `cart_screen.dart`, `checkout_screen.dart`, `product_page.dart`, `list_item.dart`
- **Item Management**: `create_listing_screen.dart`
- **Orders**: `order_history_screen.dart`, `order_details_screen.dart`, `seller_orders_screen.dart`
- **Communication**: `chat_list_screen.dart`, `chat_screen.dart`
- **Trading**: `trade_offer_screen.dart`, `trade_offer_details_screen.dart`
- **User Profile**: `edit_profile_screen.dart`, `external_profile_screen.dart`
- **Notifications**: `notifications_screen.dart`


#### **`lib/services/`** - Business Logic & Firebase Integration
Contains service classes that handle data operations and Firebase interactions:
- `auth_service.dart` - Firebase Authentication management
- `firestore_service.dart` - Firestore database operations
- `storage_service.dart` - Firebase Storage for image uploads
- `cart_service.dart` - Shopping cart logic
- `chat_service.dart` - Real-time chat functionality
- `notification_service.dart` - Push notification handling
- `reviews_service.dart` - User reviews

#### **`lib/models/`** - Data Models
Data classes representing app entities:
- `user_info.dart` - User profile data
- `item.dart` - Product/item listings
- `cart_item.dart` - Shopping cart items
- `order.dart` - Purchase orders
- `chat.dart` - Chat messages
- `notification.dart` - Notification data
- `trade_offer.dart` - Trade offer details
- `review.dart` - User reviews

#### **`lib/controllers/`** - State Management
Riverpod controllers for state management:
- `user_info_controller.dart` - User profile state
- `item_controller.dart` - Item listings state
- `cart_controller.dart` - Shopping cart state


#### **`assets/`** - Static Resources
- `images/` - App images and icons

#### **`functions/`** - Firebase Cloud Functions
- `index.js` - Cloud functions for backend operations
- `DEPLOY_GUIDE.md` - Deployment instructions

#### **Platform-specific Directories**
- `android/` - Android-specific configuration

---

### Navigation Flow

```
Login Screen (Initial Route)
    ↓
    ├─→ Signup Screen
    ├─→ Forgot Password Screen
    └─→ (After Login) Bottom Navigation Bar
            ↓
            ├─→ Tab 1: Item List Screen (Home/Free Items)
            │       ├─→ Product Page
            │       │       ├─→ External Profile Screen
            │       │       ├─→ Chat Screen
            │       │       └─→ Trade Offer Screen
            │       │               └─→ Trade Offer Details Screen
            │       └─→ Create Listing Screen
            │
            ├─→ Tab 2: Search Screen
            │       └─→ Product Page (same as above)
            │
            ├─→ Tab 3: Cart Screen
            │       └─→ Checkout Screen
            │               └─→ Order Details Screen
            │
            └─→ Tab 4: Profile Screen
                    ├─→ Edit Profile Screen
                    ├─→ Notifications Screen
                    ├─→ Order History Screen
                    │       └─→ Order Details Screen
                    ├─→ Seller Orders Screen
                    │       └─→ Order Details Screen
                    └─→ Chat List Screen
                            └─→ Chat Screen
```

**Navigation Implementation**: 
- Uses `go_router` package for declarative routing
- Auth state managed with Riverpod
- Automatic redirect logic (unauthenticated users → login, authenticated users → home)
- Deep linking support for notifications

---

## 4. Firebase Integration

### **Firebase Authentication**
- **Purpose**: User login, signup, and password recovery
- **Implementation**: 
  - Email/password authentication
  - Auth state persistence across app restarts
  - Auth state changes monitored via Riverpod providers

### **Cloud Firestore**
- **Purpose**: Primary database for all app data
- **Collections**:
  - `users` - User profiles and information
  - `items` - Product listings with details, prices, and availability
  - `orders` - Purchase transactions and order history
  - `chats` - Chat messages between users
  - `notifications` - In-app notification records
  - `trade_offers` - Trade proposals and status
  - `reviews` - User ratings and reviews
- **Implementation**: 
  - Real-time data synchronization
  - Complex queries with filtering and sorting

### **Firebase Cloud Storage**
- **Purpose**: Store and retrieve images
- **Use Cases**:
  - User profile pictures
  - Product/item images
  - Multiple images per listing support
- **Implementation**: 
  - Image upload with compression
  - URL generation for display
  - File deletion on item removal

### **Firebase Cloud Messaging (FCM)**
- **Purpose**: Push notifications for real-time updates
- **Use Cases**:
  - New message notifications
  - Order status updates
  - Trade offer notifications
  - General app notifications
- **Implementation**: 
  - FCM token management per user
  - Background and foreground message handling
  - Notification click handling with deep links
  - Local notifications integration

### **Firebase Cloud Functions** (Optional Backend)
- **Purpose**: Server-side logic and automation
- **Location**: `functions/index.js`
- **Note**: Deployment guide available in `functions/DEPLOY_GUIDE.md`

---

## 6. Challenges and Solutions

### Challenge 1: Image Upload and Management
**Problem**: Handling multiple image uploads per item, managing file sizes, ensuring proper storage organization, and displaying images efficiently without performance issues.

**Solution**: 
- Created dedicated `StorageService` with organized file paths (e.g., `items/{itemId}/{imageIndex}.jpg`)
- Implemented image compression before upload using `image_picker` package
- Added progress indicators during upload
- Used Firebase Storage URLs with caching for efficient retrieval
- Implemented proper cleanup (delete images when item is deleted)
- Added error handling for permission issues and network failures

**Result**: Reliable image upload system with good performance and proper resource management. Users can upload multiple clear product images without app slowdown.

---

### Challenge 2: Navigation and Auth State Management
**Problem**: Complex navigation requirements with authentication redirects, deep linking from notifications, and maintaining proper navigation stack while preventing unauthorized access.

**Solution**: 
- Implemented `go_router` with custom redirect logic
- Created auth state listener using Riverpod that watches Firebase Auth changes
- Configured automatic redirects:
  - Unauthenticated users → login screen
  - Authenticated users on auth pages → home screen
  - Preserve intended destination after login
- Integrated deep linking for notification navigation
- Used named routes for clean navigation code
- Implemented proper route guards to protect sensitive screens

**Technical Implementation**:
```dart
// Router with auth-based redirect
redirect: (context, state) {
  final isLoggedIn = authState.value != null;
  final isOnAuthPage = /* check auth pages */;
  
  if (!isLoggedIn) return isOnAuthPage ? null : '/login';
  if (isLoggedIn && isOnAuthPage) return '/free';
  return null;
}
```

**Result**: Seamless navigation experience with proper authentication flow, deep linking support, and no unauthorized access to protected screens.


### Challenge 3: Native Android Notification Implementation
**Problem**: Implementing push notifications that work reliably on Android devices, handling both foreground and background notification states, managing notification channels, and ensuring proper notification display with custom actions and deep linking.

**Solution**: 
- Integrated `flutter_local_notifications` package for native Android notification handling
- Configured Firebase Cloud Messaging (FCM) for push notification delivery
- Created Android notification channels with proper importance levels
- Implemented background notification handler for when app is closed
- Set up foreground notification listener for when app is active
- Configured notification intents for deep linking to specific screens
- Added notification permission handling for Android 13+
- Implemented FCM token management and storage in Firestore

**Technical Implementation**:
```dart
// Background notification handler
@pragma('vm:entry-point')
Future<void> firebaseMessagingBackgroundHandler(RemoteMessage message) async {
  await Firebase.initializeApp();
  // Handle background notification
}

// Notification channel configuration
const AndroidNotificationChannel channel = AndroidNotificationChannel(
  'high_importance_channel',
  'High Importance Notifications',
  importance: Importance.max,
);
```

**Challenges Faced**:
- Android notification channel configuration for different Android versions
- Handling notification permissions on Android 13+
- Managing notification icons and images properly
- Deep linking from notification to specific screens
- Ensuring notifications display in both foreground and background states

**Result**: Fully functional push notification system that works reliably across different Android versions, properly displays notifications in all app states, and seamlessly navigates users to relevant screens when notifications are tapped.
