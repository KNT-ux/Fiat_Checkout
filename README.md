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
Live Link: YOUR_DEPLOYED_LINK

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

1. User fills checkout form.
2. Client-side validation runs.
3. If valid:
   - Loading state starts
   - POST request sent to Beeceptor API
4. Based on API response:
   - Success → Redirect to success page
   - Failure → Show error message
5. Button remains disabled during request to prevent duplicate submissions.

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
