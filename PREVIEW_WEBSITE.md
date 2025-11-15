# 🌐 View Your Restaurant Website

## Quick Start - See It Live!

### Option 1: Run Locally (5 minutes)

1. **Open Terminal/Command Prompt in your project folder**

2. **Install dependencies:**
   ```bash
   cd backend
   npm install
   ```

3. **Start the server:**
   ```bash
   npm start
   ```

4. **Open your browser and visit:**
   - **Customer Page:** http://localhost:3000
   - **Admin Panel:** http://localhost:3000/admin

5. **You'll see:**
   - Beautiful restaurant menu with food images
   - Shopping cart on the right (desktop) or bottom (mobile)
   - Menu items: Idly, Puttu, Poori, Dosa, Coffee, Tea, Vada
   - Each item with image, description, price, and "Add to Cart" button

---

## Website Layout Preview

### Customer Page (index.html)

```
┌─────────────────────────────────────────────────────┐
│  🍽️ South Indian Restaurant                        │
│                    Menu  |  Admin                   │
├─────────────────────────────────────────────────────┤
│                                                     │
│  Our Menu                                           │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐                  │
│  │Idly │ │Puttu│ │Poori│ │Dosa │  ┌──────────┐    │
│  │₹30  │ │₹40  │ │₹50  │ │₹60  │  │ Your Cart│    │
│  │[Img]│ │[Img]│ │[Img]│ │[Img]│  ├──────────┤    │
│  │[Add]│ │[Add]│ │[Add]│ │[Add]│  │          │    │
│  └─────┘ └─────┘ └─────┘ └─────┘  │  Empty   │    │
│  ┌─────┐ ┌─────┐ ┌─────┐          │          │    │
│  │Coffee│ │Tea │ │Vada │          ├──────────┤    │
│  │ ₹20 │ │ ₹15│ │ ₹25│          │ Total: ₹0 │    │
│  │[Img]│ │[Img]│ │[Img]│          │ [Pay Now]│    │
│  │[Add]│ │[Add]│ │[Add]│          │[Print Bill]│  │
│  └─────┘ └─────┘ └─────┘          │[Clear Cart]│  │
│                                    └──────────┘    │
└─────────────────────────────────────────────────────┘
```

### Admin Panel (admin.html)

```
┌─────────────────────────────────────────────────────┐
│  👤 Admin Panel                                     │
│                    Menu  |  Admin                   │
├─────────────────────────────────────────────────────┤
│                                                     │
│  Menu Management      │   Monthly Sales Report      │
│  ┌─────────────────┐  │   ┌─────────────────────┐  │
│  │ Add New Item    │  │   │ Year: [2024] ▼      │  │
│  │                 │  │   │ Month: [All] ▼      │  │
│  │ Name: [_____]   │  │   │ [Generate Report]   │  │
│  │ Price: [____]   │  │   │                     │  │
│  │ Image: [_____]  │  │   │ Total Revenue: ₹0   │  │
│  │ Desc: [_____]   │  │   │ Total Orders: 0     │  │
│  │ [Add Item]      │  │   └─────────────────────┘  │
│  └─────────────────┘  │                            │
│                       │                            │
│  Current Menu Items   │                            │
│  ┌─────────────────┐  │                            │
│  │ [Img] Idly ₹30  │  │                            │
│  │      [Edit][Del]│  │                            │
│  │ [Img] Puttu ₹40 │  │                            │
│  │      [Edit][Del]│  │                            │
│  └─────────────────┘  │                            │
└─────────────────────────────────────────────────────┘
```

---

## Visual Features

### 🎨 Color Scheme
- **Header:** Orange-Red gradient background
- **Menu Items:** White cards with images
- **Buttons:** Red/Primary color for actions
- **Cart:** White sidebar with orange accents

### 📱 Mobile View
- **Menu Grid:** 2 columns on mobile, 1 on small screens
- **Cart:** Bottom sheet that slides up from bottom
- **Floating Cart Button:** Shows item count at bottom

### 🖼️ Images
- All menu items display beautiful Unsplash food images
- Images are 400x300px, optimized for web
- Fallback to placeholder if image fails to load

### ✨ Interactive Features
- **Click menu item** → Adds to cart
- **Cart shows:** Item name, quantity, price, total
- **Pay Now button** → Shows QR code modal
- **Print Bill** → Prints formatted receipt
- **Admin panel** → Full CRUD for menu management

---

## To Capture Screenshot

1. **Run the website locally** (instructions above)
2. **Open browser developer tools:** F12
3. **Use browser extension:**
   - Chrome: "GoFullPage" or "Awesome Screenshot"
   - Firefox: Built-in screenshot tool
4. **Or use Windows Snipping Tool / Mac Screenshot**

---

## Live Preview URLs (After Deployment)

Once deployed, your site will be at:
- **Customer Page:** `https://your-app.onrender.com`
- **Admin Panel:** `
`

---

**Run `cd backend && npm install && npm start` to see it now!**

