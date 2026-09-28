# 🌍 Wanderlust — Full-Stack Travel Accommodation & Rental Platform

**Wanderlust** is a full-stack web application inspired by Airbnb that enables users to discover, host, manage, and review travel accommodations globally. Built following the MVC (Model-View-Controller) pattern with Node.js, Express, MongoDB, and Bootstrap.

🚀 **Live Application:** [https://wanderlust-v3cg.onrender.com](https://wanderlust-v3cg.onrender.com)  
💻 **GitHub Repository:** [https://github.com/Riyamodi19/WANDERLUST](https://github.com/Riyamodi19/WANDERLUST)

---

## ✨ Features

* **Property Listings (CRUD):** Browse property listings with detailed descriptions, pricing, locations, and high-quality images. Registered users can list new properties, update details, or delete listings.
* **Interactive Maps & Geocoding:** Location geocoding and dynamic map visualization powered by **Mapbox SDK** and **Mapbox GL JS**.
* **Cloud Image Uploads:** Multi-format image file uploading and cloud hosting integrated using **Multer** and **Cloudinary**.
* **Ratings & Reviews:** Authenticated users can write comments and give 1–5 star ratings on listing pages.
* **Authentication & Security:** User authentication powered by **Passport.js** with hashed passwords. Role-based authorization ensures users can only edit or delete their own listings and reviews.
* **Input Validation:** Schema-level data validation via **Joi** to guarantee request payload integrity.
* **Session Management:** Persistent login sessions backed by **MongoDB Atlas** and `connect-mongo`.
* **Responsive UI:** Dynamic frontend views built with **EJS**, **Bootstrap 5**, FontAwesome icons, and custom CSS.

---

## 🛠️ Technology Stack

| Layer | Technologies |
| :--- | :--- |
| **Backend Runtime & Framework** | Node.js, Express.js |
| **Database & ORM** | MongoDB Atlas, Mongoose |
| **Authentication & Security** | Passport.js, Passport-Local, Express-Session, Connect-Mongo |
| **Frontend & Views** | EJS, EJS-Mate, Bootstrap 5, FontAwesome, Custom CSS |
| **Cloud Services** | Cloudinary (Image Storage), Mapbox GL JS (Geocoding & Maps) |
| **Validation & Storage** | Joi Schema Validation, Multer |
| **Deployment** | Render (PaaS) |

---

## 📂 Project Architecture

```
WANDERLUST/
├── controllers/       # Controller logic (listings, reviews, users)
├── models/            # Mongoose data models (Listing, Review, User)
├── routes/            # Express router routes (listing.js, review.js, user.js)
├── utils/             # Helper utilities (wrapAsync, ExpressError)
├── views/             # EJS view templates & layouts
│   ├── includes/      # Reusable partials (Navbar, Footer, Flash alerts)
│   ├── layouts/       # Main layout (boilerplate.ejs)
│   └── listings/      # Listing views (index, show, new, edit)
├── public/            # Static files (CSS, client JavaScript)
├── cloudConfig.js     # Cloudinary SDK storage setup
├── schema.js          # Joi input validation schemas
├── middleware.js      # Custom authentication & ownership middleware
├── app.js            # Express application entry point
└── package.json       # Project dependencies & startup scripts
```

---

## 🚀 Local Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Riyamodi19/WANDERLUST.git
   cd WANDERLUST
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the root folder:
   ```env
   ATLASDB_URL=your_mongodb_atlas_uri
   SECRET=your_session_secret
   CLOUD_NAME=your_cloudinary_cloud_name
   CLOUD_API_KEY=your_cloudinary_api_key
   CLOUD_API_SECRET=your_cloudinary_api_secret
   MAP_TOKEN=your_mapbox_access_token
   ```

4. **Run the server:**
   ```bash
   npm start
   ```
   Navigate to `http://localhost:8080` in your browser.
