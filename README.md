# Bookey - Algerian Online Bookstore (TD-TP 2 Frontend)

**Higher National School of Advanced Technologies (ENSTA)**  
**Department:** SS / IA — First Semester 2026  
**Module:** WAMD (Web and Mobile Development)  
**Lab Assignment:** TD-TP 2: Build an E-Commerce Frontend using React and Redux  
**Student Name:** [Your Name Here]

---

## 1. Project Overview
**Bookey** is an online bookstore specializing in Algerian literature, historical narratives, and essays.  
This standalone folder represents **TD-TP 2** (Frontend Only), implementing a complete client-side e-commerce web application with **React 18**, **Redux Toolkit / React-Redux**, and **Vite**.

### Key Features
* **Catalog Browsing & Search**: Search books in real time by title, author, or keywords.
* **Category Filtering**: Filter shelves by *All Books*, *Novels*, *History*, or *Essays* (accessible from the navbar and catalog toolbar).
* **Sorting Options**: Sort by Featured Classics, Chronological (Publication Year), or Price (Ascending/Descending).
* **Quick View Modal**: Click any book to view full synopsis, edition metadata, stock availability, and a quantity selector.
* **Global Shopping Cart (Redux)**: 
  * Add to cart, adjust quantities (`+` / `-`), remove items, and clear basket.
  * Live badge count and subtotal updated across navbar and cart views.
  * Free shipping calculation for Algeria's 58 Wilayas (free on orders over 4,000 DZD).
  * Slide-over cart drawer accessible from anywhere on the page.
* **Simulated Algerian Checkout**:
  * Cash on Delivery (*Paiement à la livraison*) ordering flow.
  * Complete dropdown of all **58 Algerian Wilayas** (Adrar to El Meniaa).
  * Generates an official order reference receipt (`BK-XXXXXX`) and clears the cart.
* **Aesthetic**: Warm vintage storybook design with Cormorant Garamond / Playfair Display typography, parchment tones, and clean inline SVG icons (100% emoji-free).

---

## 2. Technologies Used
* **React 18** (Functional components, Hooks: `useState`, `useEffect`)
* **Redux / React-Redux** (Global shopping cart state management: `cartReducer`, `actions`, `store`)
* **Vite 5** (High-performance build tool and local dev server)
* **CSS3** (Custom vintage storybook design system, responsive grid/flexbox layouts, keyframe animations)

---

## 3. Project Structure
```
bookey-tp2-frontend/
├── public/
│   └── favicon.svg              # Vintage Algerian bookstore seal icon
├── src/
│   ├── components/
│   │   ├── BookCard.jsx         # 3D cloth-bound book card with ribbon & quick view
│   │   ├── BookList.jsx         # Responsive grid of books with empty state
│   │   ├── Cart.jsx             # Library ledger cart & slide-over drawer
│   │   ├── CartItem.jsx         # Cart row with thumbnail, stepper, and subtotal
│   │   ├── CategoryFilter.jsx   # Vintage pill shelf filters with clean SVGs
│   │   ├── CheckoutModal.jsx    # Real Algerian e-commerce checkout form (58 wilayas)
│   │   ├── Footer.jsx           # Structured footer with customer care & store info
│   │   ├── Hero.jsx             # E-commerce hero with featured book spotlight
│   │   ├── Navbar.jsx           # Sticky nav with working category links & cart badge
│   │   ├── QuickViewModal.jsx   # Product detail popup with quantity adjuster
│   │   └── SearchBar.jsx        # Real-time search with clear button
│   ├── data/
│   │   ├── books.js             # Algerian literature catalog dataset
│   │   └── wilayas.js           # Complete list of 58 Algerian wilayas
│   ├── redux/
│   │   ├── actions.js           # Action creators (addToCart, decreaseQuantity, etc.)
│   │   ├── actionTypes.js       # Action type constants
│   │   ├── cartReducer.js       # Pure reducer function handling cart modifications
│   │   └── store.js             # Redux store configuration
│   ├── styles/
│   │   ├── global.css           # Typography, color variables, paper grain background
│   │   └── components.css       # Full styling for all e-commerce components
│   ├── App.jsx                  # Main application container & state integration
│   └── main.jsx                 # React root renderer with Redux Provider
├── index.html                   # HTML entry point with Google Fonts
├── package.json                 # Frontend dependencies & scripts
└── vite.config.js               # Vite React configuration
```

---

## 4. How to Run the Frontend

### 1. Navigate to the folder
```powershell
cd C:\Users\lenovo\Downloads\bookey\bookey-tp2-frontend
```

### 2. Install Dependencies
```powershell
npm install
```

### 3. Start Development Server
```powershell
npm run dev
```
Open `http://localhost:5173/` in your browser.

### 4. Build for Production
```powershell
npm run build
```
The production bundle will be generated in `dist/`.
