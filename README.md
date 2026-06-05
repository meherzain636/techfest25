# TechFest '25 Event Portal 🚀

A modern, high-performance, and futuristic static web portal designed for **TechFest '25** hosted by the **Department of CS&IT, NED University of Engineering and Technology (NEDUET)**. 

This repository contains the complete frontend dashboard, registration system, and confirmation funnel, featuring real-time client-side interactive search/filters, webhook integration, and personalized confirmations.

---

## ✨ Features

- **Futuristic Glassmorphic Design**: Sleek, immersive dark mode utilizing premium typography (**Orbitron** for tech/headers and **Inter** for forms/content), subtle neon glow outlines, and glassmorphic backdrops.
- **Dynamic 13-Event Dashboard**: Complete event catalog representing the entire TechFest '25 schedule, with details on categories, schedules, venues, organizers, and expandable participant expectations drawers.
- **Real-time Search & Filter System**: Fuzzy searching and interactive category tabs (Competitions, Workshops, Hackathons, Talks, Ceremonies) built with pure vanilla JS.
- **Seamless Pre-selected Registration**: Auto-selection logic that pre-fills the registration dropdown automatically based on the event clicked from the dashboard (via URL query parameters).
- **n8n Webhook Integration**: Connected to a serverless n8n workflow for instant processing of registrant data.
- **Personalized Success Engine**: Extracts secure `localStorage` tokens to greet users by name and confirm their exact registered event on the confirmation page.
- **Global Assistant Integration**: Includes a global Botpress Webchat chatbot widget injected across all pages for interactive user inquiries.

---

## 📂 Project Structure

```bash
├── index.html       # TechFest '25 Homepage & Event Catalog Dashboard
├── register.html    # Registration Form with validation and n8n webhook post
├── success.html     # Personalized confirmation page (reads localStorage)
└── README.md        # Repository Documentation
```

---

## 🛠️ Tech Stack & Integrations

- **Frontend**: HTML5 (Semantic Structure), Vanilla CSS3 (Custom variables, glassmorphism, responsive grid), Vanilla JavaScript (ES6+).
- **Typography**: Google Fonts (`Orbitron`, `Inter`).
- **Webhook Endpoint**: Hosted n8n instance for form submission handling.
- **Customer Support**: Botpress Webchat Chatbot widget.

---

## 🔗 Integration Specs

### Webhook Payload Format
The registration form sends a `POST` request with a JSON payload to the n8n endpoint:

```json
{
  "name": "Zain ul Abideen",
  "email": "zain@gmail.com",
  "phone": "0300-1234567",
  "event": "TechFest 2025 - Workshop"
}
```

### Dynamic Pre-selection API
To link to a pre-selected event on the registration page, use the `event` query parameter:
```text
register.html?event=UrlEncodedEventName
```

---

## 🚀 Local Development & Usage

Since this is a client-side static application, you do not need to install heavy dependencies or compile build steps.

### Option 1: Direct File Launch
Double-click `index.html` to run the app directly in any modern browser.

### Option 2: Local Server (Recommended)
To run the project on a local server, navigate to the project directory and run one of the following commands:

**Using Python 3:**
```bash
python3 -m http.server 8000
```
*Access the site at `http://localhost:8000`.*

**Using Node.js (npx):**
```bash
npx serve .
```
*Access the site at `http://localhost:3000`.*
