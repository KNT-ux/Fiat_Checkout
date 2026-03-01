# Fiat_Checkout
#  Fiat Checkout Assignment

A fully functional Checkout Page built from Figma design as part of the Frontend Assignment.

---

## Demo

Site: fiat-checkout.netlify.app 

---

# Project Overview

This project converts the provided Figma design into a fully functional checkout application using pure HTML, CSS, and JavaScript (no UI libraries).

The application includes:
- Pixel-accurate UI implementation
- Form validation with inline error messages
- API integration using Beeceptor (mock backend)
- Success and failure flow handling
- Deployment to a live hosting platform

---

#  Project Levels Completed

##  Level 1 – UI Implementation
- Converted Figma design into responsive HTML & CSS
- Maintained layout structure, spacing, and alignment
- No external UI libraries used (No Bootstrap / MUI)

---

##  Level 2 – Form Behavior & Validation
All form fields:
- Have proper validation rules
- Show inline error messages
- Prevent submission if invalid

### Validation Includes:
- Card number validation
- Auto formatting for expiry date (MM/YY)
- CVV validation (3 digits)
- Required field checks
- Real-time error removal while typing
- Pay button disabled until form is valid

---

##  Level 3 – Payment API Integration
- Integrated Beeceptor mock API
- Sends POST request on clicking "Pay Now"
- Sends form data as JSON
- Shows loading state during request
- Disables button while processing
- Handles both success and failure responses

---

## Level 4 – Success & Failure Flow
- Redirects to success page on successful payment
- Displays error message if payment fails
- Shows success animation before redirect

---

##  Deployment
The project is deployed and publicly accessible.

Deployment platform: Netlify / Vercel / GitHub Pages  


---

#  Tech Stack

- HTML5
- CSS3 (Basic CSS, no frameworks)
- Vanilla JavaScript (ES6)
- Fetch API
- Beeceptor (Mock API Service)

---

#  Project Structure
fiat-checkout/
│
├── index.html
├── success.html
├── style.css
├── script.js
└── README.md


---

#  Architecture Explanation

This project follows a client-side modular web architecture using HTML, CSS, and JavaScript. It simulates a secure checkout flow with validation, API interaction, and dynamic success page rendering.

The application is structured into three main layers:

---

Presentation Layer (UI)

**Files:**

* `index.html`
* `success.html`
* Embedded CSS

Responsibility:

* Renders checkout form
* Displays validation errors
* Shows loading states
* Displays payment success details

Key Features:

* Responsive layout
* Form validation feedback
* Loading animation during API call
* Dynamic order and date display on success page

This layer does not handle business logic directly. It interacts with JavaScript for dynamic behavior.

---

 Business Logic Layer (Client-side JavaScript)

**File:**

* `script.js`

Responsibility:

* Form validation
* Payment simulation
* API communication
* Order ID generation
* Date generation
* Redirect logic
* URL parameter passing

 Main Flow:

1. User submits form
2. `validateForm()` checks:

   * Name format
   * 16-digit card number
   * Valid expiry date
   * 3-digit CVV
3. If valid:

   * Show loading state
   * Send POST request to mock API
4. If API success:

   * Generate dynamic Order ID
   * Generate current date
   * Redirect to success page with query parameters

Example:

```
success.html?order=FIAT-4821&date=Feb%2027,%202026
```

---

API Layer (Mock Backend)

**Service Used:**

* Beeceptor mock API endpoint

### Responsibility:

* Simulates server-side payment processing
* Receives form data via POST request
* Returns success response

This mimics real-world backend integration without requiring a full server.

---

#  Data Flow Architecture

User Input
⬇
Client-side Validation
⬇
Mock API Call (fetch POST)
⬇
Generate Order ID + Date
⬇
Redirect with URL Parameters
⬇
Success Page Reads Parameters
⬇
Display Dynamic Order Details

---

# Architectural Pattern Used

This project loosely follows:

* Separation of Concerns (UI / Logic / API)
* Client-side MVC-style flow
* Event-driven architecture (form submission events)
* Asynchronous programming using async/await

---

# Security Considerations (Simulation Context)

* Card data is validated but not stored
* No sensitive data is persisted
* API endpoint is mock only
* Order ID generated client-side for demo purposes

In a real-world application:

* Payment processing would happen server-side
* Sensitive data would never be handled in frontend
* HTTPS and tokenization would be used

---

# Scalability Potential

This architecture can be extended by:

* Adding real backend (Node.js / Express)
* Storing transactions in database
* Implementing authentication
* Adding state management
* Converting to React or other SPA framework

---

#  Key Learning Outcomes

- DOM manipulation
- Form validation techniques
- Async/Await & Fetch API
- API integration
- Error handling
- UI/UX state management
- Deployment process

---

#  Future Improvements

- Add transaction ID generation
- Improve UI responsiveness
- Add backend with Node.js + MongoDB
- Store transaction history
- Improve accessibility (ARIA labels)

---

#  Author

KHADEEJA NUSRATH T 
Frontend Developer  
