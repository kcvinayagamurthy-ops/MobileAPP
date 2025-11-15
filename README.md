# Restaurant Website with Cart

A full-stack restaurant website with menu display, shopping cart, billing system, QR code payment, bill printing, monthly sales reports, and admin CRUD operations for menu management.

## Features

- **Menu Display**: Beautiful grid layout showing menu items with images, names, and prices
- **Shopping Cart**: Add items by clicking, view cart, update quantities, remove items
- **Billing System**: Automatic calculation of subtotal and grand total
- **Payment**: Pay Now button with QR code generation for payment
- **Print Bill**: Print functionality for bill/receipt
- **Clear Cart**: Button to clear all items from cart
- **Menu Management**: Admin panel with CRUD operations (Create, Read, Update, Delete menu items)
- **Sales Report**: Monthly sales tracking and reporting for admin

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Backend**: Node.js with Express
- **Database**: JSON file storage
- **QR Code**: qrcode.js library (CDN)

## Setup Instructions

### Prerequisites

- Node.js (v14 or higher)
- npm (Node Package Manager)

### Installation

1. Install backend dependencies:
```bash
cd backend
npm install
```

2. Create image placeholders (optional):
   - Create placeholder images for menu items in `public/images/`:
     - idly.jpg
     - puttu.jpg
     - poori.jpg
     - dosa.jpg
     - coffee.jpg
     - tea.jpg
     - vada.jpg
   - Or use placeholder image services by updating image URLs in `backend/data/menu.json`

3. Start the backend server:
```bash
cd backend
npm start
```

The server will start on `http://localhost:3000`

### Running the Application

1. Open your browser and navigate to:
   - Customer page: `http://localhost:3000`
   - Admin panel: `http://localhost:3000/admin`

2. **Customer Features**:
   - Browse menu items
   - Click on items to add to cart
   - View cart, update quantities, remove items
   - Click "Pay Now" to see QR code
   - Click "Print Bill" to print receipt
   - Click "Clear" to empty cart

3. **Admin Features**:
   - Add new menu items
   - Edit existing menu items
   - Delete menu items
   - Generate monthly sales reports
   - View item-wise sales statistics

## Project Structure

```
/
├── public/
│   ├── index.html          # Customer-facing page
│   ├── admin.html          # Admin panel
│   ├── css/
│   │   ├── style.css       # Customer page styles
│   │   └── admin.css       # Admin panel styles
│   ├── js/
│   │   ├── menu.js         # Menu display and fetching
│   │   ├── cart.js         # Cart management
│   │   ├── payment.js      # Payment and billing
│   │   ├── admin.js        # Admin CRUD operations
│   │   └── sales.js        # Sales report functionality
│   └── images/             # Menu item images
├── backend/
│   ├── server.js           # Express server setup
│   ├── routes/
│   │   ├── menuRoutes.js   # Menu API routes
│   │   └── orderRoutes.js  # Orders and sales API routes
│   ├── data/
│   │   ├── menu.json       # Menu items data
│   │   └── orders.json     # Orders data (created on first order)
│   └── package.json        # Backend dependencies
└── README.md
```

## API Endpoints

### Menu Routes
- `GET /api/menu` - Fetch all menu items
- `POST /api/menu` - Create new menu item
- `PUT /api/menu/:id` - Update menu item
- `DELETE /api/menu/:id` - Delete menu item

### Order Routes
- `POST /api/orders` - Save order (for sales tracking)
- `GET /api/sales/monthly?year=YYYY&month=MM` - Get monthly sales report

## Default Menu Items

The application comes with the following default menu items:
- Idly - ₹30
- Puttu - ₹40
- Poori - ₹50
- Dosa - ₹60
- Coffee - ₹20
- Tea - ₹15
- Vada - ₹25

## Notes

- Cart data is persisted in browser's localStorage
- Orders are saved to `backend/data/orders.json` for sales tracking
- Menu items are stored in `backend/data/menu.json`
- For production, consider using a proper database (MongoDB, PostgreSQL, etc.)

## Deployment

The website is ready to deploy! See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed deployment instructions.

### Quick Deploy to Render (Recommended)

1. Push your code to GitHub
2. Go to https://render.com and create a free account
3. Click "New +" → "Web Service"
4. Connect your GitHub repository
5. Configure:
   - **Build Command:** `cd backend && npm install`
   - **Start Command:** `node backend/server.js`
6. Click "Create Web Service"
7. Your site will be live in minutes!

For other deployment options (Railway, Heroku, Vercel), see [DEPLOYMENT.md](DEPLOYMENT.md).

## License

This project is open source and available for educational purposes.
