# Amazon Clone - Enhanced E-commerce Platform

A full-featured Amazon clone built with React.js and Node.js, featuring authentic Amazon-style UI/UX, complete shopping cart functionality, and secure checkout process.

## 🚀 Features

### 🎯 Core E-commerce Features
- **Product Catalog**: Comprehensive database with Electronics, Fashion, Home & Kitchen, and Books
- **Shopping Cart**: Full cart functionality with add/remove products and quantity controls
- **Checkout Process**: Complete checkout flow with address selection and payment processing
- **Order Management**: Order confirmation and success pages with tracking information
- **User Authentication**: Secure login/registration with demo credentials

### 🎨 Amazon-Style UI/UX
- **Hero Carousel**: Auto-rotating banner with navigation arrows and dots
- **Product Cards**: Amazon-style product display with ratings, pricing, and Prime badges
- **Responsive Design**: Mobile-first approach with seamless mobile experience
- **Authentic Styling**: Amazon color schemes, typography, and layout patterns

### 🔐 Authentication & Security
- **JWT Authentication**: Secure token-based authentication system
- **Protected Routes**: Route protection for authenticated users only
- **Password Security**: Bcrypt password hashing and validation
- **Demo Accounts**: Pre-configured test accounts for easy testing

## 🛠️ Technology Stack

### Frontend
- **React 18** - Modern React with hooks and context API
- **React Router DOM** - Client-side routing
- **GSAP** - Smooth animations and transitions
- **CSS3** - Custom styling with Flexbox and Grid
- **Font Awesome** - Icon library

### Backend
- **Node.js** - Server runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **Bcryptjs** - Password hashing
- **CORS** - Cross-origin resource sharing

## 📦 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- Git

### 1. Clone the Repository
```bash
git clone https://github.com/pradeep-iitb/AmazonClone2.git
cd AmazonClone2
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the backend directory:
```env
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/amazonclone
JWT_SECRET=your_jwt_secret_key_here
JWT_EXPIRES_IN=7d
BCRYPT_SALT_ROUNDS=12
```

### 3. Frontend Setup
```bash
cd ../frontend
npm install
```

### 4. Database Seeding
Seed the database with sample products and users:
```bash
cd ../backend
node seed.js
```

### 5. Start the Application
Start both servers (use separate terminals):

**Backend Server:**
```bash
cd backend
npm start
```

**Frontend Server:**
```bash
cd frontend
npm start
```

The application will be available at `http://localhost:3000`

## 🧪 Demo Accounts

Use these pre-configured accounts for testing:

| Email | Password | Role |
|-------|----------|------|
| `customer@example.com` | `Password123!` | Customer |
| `jane@example.com` | `Password123!` | Seller |
| `john@example.com` | `Password123!` | Admin |

## 📱 Features Overview

### Homepage
- **Hero Carousel**: 5 auto-rotating slides with Amazon-style banners
- **Category Cards**: Electronics, Fashion, Home & Kitchen, Books
- **Featured Products**: Grid of products with "Add to Cart" functionality
- **Prime Section**: Amazon Prime promotion banner

### Shopping Cart
- **Real-time Updates**: Cart count in header updates automatically
- **Quantity Controls**: Increase/decrease product quantities
- **Price Calculations**: Subtotal, shipping, tax, and total calculations
- **Persistent State**: Cart contents saved per user account

### Checkout Process
1. **Shipping Address**: Select from saved addresses or add new ones
2. **Payment Method**: Credit card, Amazon Pay, or PayPal options
3. **Order Review**: Final review of items and pricing
4. **Order Confirmation**: Success page with order details

### Authentication
- **Login Page**: Amazon-style login with demo account buttons
- **Registration**: Account creation with validation
- **Protected Routes**: Cart, checkout, and profile pages require authentication

## 🏗️ Project Structure

```
AmazonClone2/
├── backend/
│   ├── middleware/
│   │   └── auth.js                 # Authentication middleware
│   ├── models/
│   │   ├── User.js                 # User model with cart and addresses
│   │   ├── Product.js              # Product model with specifications
│   │   └── Order.js                # Order model
│   ├── routes/
│   │   ├── auth.js                 # Authentication routes
│   │   ├── products.js             # Product routes
│   │   └── users.js                # User and cart routes
│   ├── seed.js                     # Database seeding script
│   ├── server.js                   # Express server setup
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Auth/
│   │   │   │   └── ProtectedRoute.js
│   │   │   └── Layout/
│   │   │       ├── Header.js       # Navigation with cart count
│   │   │       └── Footer.js
│   │   ├── contexts/
│   │   │   ├── AuthContext.js      # Authentication state management
│   │   │   └── CartContext.js      # Cart state management
│   │   ├── pages/
│   │   │   ├── Auth/
│   │   │   │   ├── Login.js        # Amazon-style login page
│   │   │   │   └── Register.js     # Registration page
│   │   │   ├── Cart.js             # Shopping cart page
│   │   │   ├── Checkout.js         # Checkout process
│   │   │   ├── OrderSuccess.js     # Order confirmation
│   │   │   └── Home.js             # Homepage with carousel
│   │   ├── styles/
│   │   │   └── Auth.css            # Authentication page styles
│   │   └── App.js                  # Main app component
│   └── package.json
├── .gitignore                      # Git ignore file (excludes node_modules)
└── README.md
```

## 🎨 Design Features

### Amazon-Authentic Styling
- **Color Scheme**: Amazon's signature orange (#FF9900) and blue (#232F3E)
- **Typography**: Amazon's font families and sizing
- **Layout Patterns**: Grid systems and spacing matching Amazon's design
- **Interactive Elements**: Hover effects, transitions, and animations

### Responsive Design
- **Mobile-First**: Optimized for mobile devices
- **Tablet Support**: Adaptive layouts for tablet screens
- **Desktop Enhancement**: Full desktop experience with expanded features

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user

### Products
- `GET /api/products` - Get all products (with filtering)
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Create product (sellers only)

### Cart & User
- `GET /api/users/cart` - Get user's cart
- `POST /api/users/cart` - Add item to cart
- `PUT /api/users/cart/:productId` - Update cart item quantity
- `DELETE /api/users/cart/:productId` - Remove item from cart
- `GET /api/users/cart/summary` - Get cart summary (count & total)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is for educational purposes. Amazon and all related marks are trademarks of Amazon.com, Inc. or its affiliates.

## 🙏 Acknowledgments

- Amazon.com for design inspiration
- React.js and Node.js communities
- MongoDB for database solutions
- Font Awesome for icons

---

**Note**: This is a clone project created for educational purposes to demonstrate full-stack development skills. It is not affiliated with Amazon.com in any way.

## Features

### Backend Features
- **Authentication & Authorization**: JWT-based auth with role-based access control
- **User Management**: Registration, login, profile management, password change
- **Product Management**: CRUD operations with Amazon image URLs
- **Shopping Cart**: Add, update, remove items with real-time calculations
- **Wishlist**: Save favorite products
- **Order Management**: Complete order processing
- **Address Management**: Multiple shipping addresses
- **Search & Filtering**: Advanced product search with filters

### Frontend Features
- **Responsive Design**: Amazon-like UI with mobile-first approach
- **GSAP Animations**: Smooth page transitions and interactive elements
- **React Router**: Single-page application with protected routes
- **Context Management**: Global state for auth and cart
- **Real-time Updates**: Live cart and wishlist updates
- **Toast Notifications**: User feedback for all actions

## Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - Authentication tokens
- **bcryptjs** - Password hashing
- **express-validator** - Input validation

### Frontend
- **React** - Frontend library
- **React Router DOM** - Client-side routing
- **GSAP** - Animations and interactions
- **Axios** - HTTP client
- **React Hot Toast** - Notifications
- **React Hook Form** - Form handling
- **React Icons** - Icon library

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd AmazonClone1
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Environment Setup**
   
   Create a `.env` file in the backend directory:
   ```env
   NODE_ENV=development
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/amazon_clone
   JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
   JWT_EXPIRES_IN=7d
   BCRYPT_SALT_ROUNDS=12
   ```

5. **Seed the database**
   ```bash
   cd backend
   node seed.js
   ```

6. **Start the application**
   
   **Backend** (Terminal 1):
   ```bash
   cd backend
   npm start
   ```
   
   **Frontend** (Terminal 2):
   ```bash
   cd frontend
   npm start
   ```

7. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000

## Sample Login Credentials

After seeding the database, you can use these credentials:

- **Admin**: john@example.com / Password123!
- **Seller**: jane@example.com / Password123!
- **Customer**: customer@example.com / Password123!

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile
- `PUT /api/auth/change-password` - Change password
- `POST /api/auth/addresses` - Add address

### Products
- `GET /api/products` - Get all products (with search/filter)
- `GET /api/products/featured` - Get featured products
- `GET /api/products/bestsellers` - Get bestsellers
- `GET /api/products/categories` - Get product categories
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Create product (Seller/Admin)
- `PUT /api/products/:id` - Update product (Seller/Admin)
- `DELETE /api/products/:id` - Delete product (Seller/Admin)
- `POST /api/products/:id/reviews` - Add product review

### User Cart & Wishlist
- `GET /api/users/cart` - Get cart items
- `POST /api/users/cart` - Add item to cart
- `PUT /api/users/cart/:productId` - Update cart item quantity
- `DELETE /api/users/cart/:productId` - Remove item from cart
- `DELETE /api/users/cart` - Clear cart
- `GET /api/users/wishlist` - Get wishlist
- `POST /api/users/wishlist/:productId` - Toggle wishlist item

## Product Images

The application uses real Amazon product images with URLs following the pattern:
```
https://m.media-amazon.com/images/I/[IMAGE_ID].[EXTENSION]
```

Sample products include:
- Amazon Echo Dot (5th Gen)
- iPhone 15 Pro Max
- Sony WH-1000XM5 Headphones
- YETI Rambler Tumbler
- North Face Backpack
- Instant Vortex Air Fryer

## Database Schema

### User Model
- Personal information (name, email, password)
- Shopping cart (with product references)
- Wishlist (product references)
- Multiple addresses
- Order history
- Role-based permissions

### Product Model
- Product details (title, description, price)
- Amazon image URLs and thumbnails
- Specifications and features
- Reviews and ratings
- Stock management
- Category and tags
- Seller information

### Order Model
- Order items with product details
- Shipping and billing addresses
- Payment information
- Order status tracking
- Delivery tracking

## Features in Detail

### Authentication System
- Secure password hashing with bcrypt
- JWT tokens with configurable expiration
- Role-based access control (User, Seller, Admin)
- Protected routes and middleware

### Shopping Cart
- Real-time cart updates
- Persistent cart across sessions
- Quantity management with stock validation
- Price calculations with tax and shipping

### Product Management
- Dynamic product rendering
- Advanced search and filtering
- Category-based browsing
- Product reviews and ratings

### Animations
- GSAP-powered smooth transitions
- Scroll-triggered animations
- Interactive hover effects
- Loading states and micro-interactions

## Development

### Project Structure
```
AmazonClone1/
├── backend/
│   ├── models/          # Database schemas
│   ├── routes/          # API routes
│   ├── middleware/      # Custom middleware
│   ├── server.js        # Express server
│   ├── seed.js          # Database seeding
│   └── .env             # Environment variables
└── frontend/
    ├── src/
    │   ├── components/  # Reusable components
    │   ├── pages/       # Page components
    │   ├── contexts/    # React contexts
    │   ├── utils/       # Utility functions
    │   └── index.css    # Global styles
    └── public/          # Static assets
```

### Available Scripts

**Backend:**
- `npm start` - Start production server
- `npm run dev` - Start development server with nodemon
- `node seed.js` - Seed database with sample data

**Frontend:**
- `npm start` - Start development server
- `npm run build` - Build for production
- `npm test` - Run tests

## Future Enhancements

- [ ] Payment integration (Stripe/PayPal)
- [ ] Order tracking and notifications
- [ ] Advanced product filters
- [ ] Product recommendations
- [ ] Email verification
- [ ] Password reset functionality
- [ ] Admin dashboard
- [ ] Seller dashboard
- [ ] Product comparison
- [ ] Advanced search with Elasticsearch

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Amazon for design inspiration
- React community for excellent tools
- GSAP for animation capabilities
- MongoDB for flexible data storage