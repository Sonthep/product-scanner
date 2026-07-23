# Sevenfive Product Scanner

A modern, high-performance web-based product scanner designed for looking up commercial kitchen equipment details instantly. Users can scan barcodes/QR codes using their device's camera, upload image files, or perform a manual lookup using SKU codes.

The system retrieves live data from a Google Sheets database via a Google Apps Script API.

---

## 🚀 Features

*   **Dual Scan Modes**:
    *   **Camera Scanner**: Real-time barcode & QR code decoding (supports QR_CODE, CODE_128, EAN_13, UPC_A, and more) powered by `html5-qrcode`. Includes flash/torch toggle controls.
    *   **Manual Input**: Direct SKU lookup with instant input formatting.
*   **File Scan Option**: Upload an image containing a barcode/QR code to decode it automatically.
*   **Premium UI/UX**:
    *   Sleek glassmorphism header & cards.
    *   Fully responsive layout designed for both desktop and mobile warehouse use.
    *   Interactive animations: floating box and rotating gears for the idle state, live pulsing dot on success badges, and hover lift effects.
*   **Integrated Copy Utility**: One-click clipboard copy for product SKUs.
*   **Firebase Ready**: Preconfigured with `firebase.json` for rapid Firebase Hosting deployment.

---

## 🛠️ Tech Stack

*   **Core**: HTML5, Vanilla JavaScript, CSS3 variables.
*   **Libraries**: `html5-qrcode` (2.3.8) for camera decoding.
*   **Backend Database**: Google Sheets + Google Apps Script Web App API.
*   **Hosting**: Firebase Hosting.
*   **Typography**: Plus Jakarta Sans & Noto Sans Thai (Google Fonts).

---

## 📦 Getting Started

### 1. Local Development
To run the server locally, open the project directory in your terminal and run:

```bash
# Using npx to serve the public folder
npx serve public
```

Then visit [http://localhost:3000](http://localhost:3000) in your web browser.

### 2. Configuration
To link the frontend to your database, replace the `API_URL` variable in [public/index.html](public/index.html) with your Google Apps Script Web App executable URL:

```javascript
const API_URL = "https://script.google.com/macros/s/.../exec";
```

### 3. Deploying to Firebase
If you have the Firebase CLI installed, deploy the application using:

```bash
# Login and deploy
firebase login
firebase deploy
```

---

## 📁 File Structure

```text
product-scanner/
├── .firebase/            # Firebase cache
├── public/
│   ├── logo/
│   │   └── CI_logo_75_2026-01.avif   # Official Sevenfive Logo
│   ├── index.html        # Main application page (HTML, CSS, JS)
│   └── 404.html          # Custom Page Not Found handler
├── .firebaserc           # Firebase project associations
├── .gitignore            # Git exclusion rules
├── firebase.json         # Firebase deployment config
└── README.md             # Project documentation (this file)
```
