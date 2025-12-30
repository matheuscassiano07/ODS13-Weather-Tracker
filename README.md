# 🌍 EcoSentinel: Climate Action & Intelligence (ODS 13)

![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-yellow)
![Tailwind](https://img.shields.io/badge/Style-TailwindCSS-blue)
![API](https://img.shields.io/badge/API-OpenWeatherMap-orange)
![Payment](https://img.shields.io/badge/Payment-MercadoPago-lightblue)

## 🚀 The Project
**EcoSentinel** is a web application designed to promote **Climate Action (SDG 13)** through technology. It connects users to real-time weather data, issues critical alerts for extreme conditions (heatwaves, storms), and gamifies the donation process to support environmental causes.

**Key Value Proposition:**
Unlike standard weather apps, EcoSentinel contextualizes weather data into *actionable sustainability advice* and drives engagement through a leaderboard system linked to real donations.

## ⚙️ Key Features
* **📡 Real-Time Monitoring:** Integration with **OpenWeatherMap API** (One Call 3.0) for precision forecasting.
* **🚨 Smart Alerts:** Logic that detects anomalies (e.g., Temperature > 30°C or Heavy Rain) and triggers educational alerts.
* **💸 Payment Integration:** Seamless donation flow using **Mercado Pago API** (Checkout Pro).
* **🏆 Gamification:** LocalStorage-based ranking system where financial support translates into "Resilience Points".
* **🎨 Responsive UI:** Built with **Tailwind CSS** for a modern, glassmorphism-inspired interface.

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3, JavaScript (Modules).
* **Styling:** Tailwind CSS (CDN).
* **APIs:**
    * `OpenWeatherMap` (Weather Data & Geocoding).
    * `Mercado Pago` (Payment Preferences).
* **Persistence:** Browser LocalStorage (for user session and gamification data).

## 📸 Screenshots
*(Coloque um print da tela do seu site aqui depois, cria uma pasta chamada 'screenshots' e linka a imagem)*
> The "Resilience Center" dashboard showing real-time alerts.

## 📦 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/SEU_USUARIO/EcoSentinel-Climate-Intelligence.git](https://github.com/SEU_USUARIO/EcoSentinel-Climate-Intelligence.git)
    ```
2.  Open `index.html` in your browser (or use Live Server in VS Code).
3.  **Configuration:**
    * Open `script.js` and replace `const apiKey = "YOUR_KEY"` with your OpenWeatherMap key.
    * Open `apis/payApi.js` and configure your Mercado Pago Access Token.

## 🧩 Code Highlight (Gamification Logic)
The system rewards user engagement by converting donation amounts into ranking points:

```javascript
// Example of the gamification logic interacting with the Payment API
if (linkDePagamento) {
    currentUser.pontos = (currentUser.pontos || 0) + (Number(valorCorrigido) * 10);
    localStorage.setItem('userData', JSON.stringify(currentUser));
    atualizarRanking();
}
