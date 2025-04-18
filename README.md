# 🧠 AI Marketplace Simulator (Flask + Gemini AI)

Welcome to the **AI Marketplace Simulator** — a fun and strategic trading game powered by **Flask** and **Gemini AI**. In this simulation, users can negotiate with **intelligent AI shopkeepers**, buy and sell electronic components, and aim to maximize their **profit** in a dynamic, ever-changing market.

---

## 🚀 Features

- 🧾 **User Wallet & Inventory** management  
- 🤖 **Three AI-powered shopkeepers**, each with their own specialty and personality  
- 📉 **Live Market Prices** that fluctuate over time (volatility + demand-based)  
- 📈 **Negotiation via Chat** using Google Gemini AI (Smart deals, emotions, competition)  
- 📊 **Transaction History** and **Profit/Loss Tracking**  
- 🔁 Accept or reject AI-generated trade offers  
- 📉 Randomized **Market Trend Data** for charts/visuals  
- 🔄 **Reset Game** anytime to start fresh

---

## 🏪 The AI Shopkeepers

| Shop Name     | Specialty    | Discount Rate | Personality Traits |
|---------------|--------------|----------------|--------------------|
| ElectroMart   | Bulbs        | 5% off         | Competitive, Cunning |
| CircuitWorld  | Resistors    | 10% off        | Strategic, Bold      |
| WireHub       | Wires        | 7% off         | Generous, Jealous    |

Each shopkeeper uses a **Gemini AI model** and has access to **market data**, recent transactions, and competing shop behavior. They adapt and respond accordingly.

---

## 🛠️ Tech Stack

- **Backend**: Flask (Python)
- **AI Model**: Google Gemini (via `google.generativeai`)
- **Frontend**: HTML (with `index.html`), AJAX (for chat)
- **Session Management**: Flask Session
- **Price Engine**: Randomized market simulation

---

## 📂 Project Structure
```
 your-project/ 
   ├── app.py #Main Flask App 
   ├── templates/ 
     │ 
     └── index.html # Main frontend 
     └── static/ # (Optional) For JS/CSS/Images
```

---

## 🧪 API Routes Summary

| Route                | Method | Description                                      |
|----------------------|--------|--------------------------------------------------|
| `/`                  | GET    | Home page, initializes user session             |
| `/inventory`         | GET    | Returns inventory, wallet, profit/loss          |
| `/market`            | GET    | Returns current market prices                   |
| `/market-trend`      | GET    | Returns fake historical trend data              |
| `/transaction-history` | GET  | Returns user's past trades                      |
| `/chat`              | POST   | Handles AI negotiation, buy/sell commands       |
| `/reset`             | GET    | Resets game state                               |

---

## 💬 Chat Format Guidelines

Use natural language or these patterns for accurate parsing:

- Buying:  
  `"buy 5 bulbs at ₹40"`  
  `"purchase 2 resistors for ₹15"`

- Selling:  
  `"sell 3 wires at ₹22"`  
  `"offer 1 capacitor for ₹28"`

- Accepting AI Deals:  
  `"accept"`, `"okay"`, `"deal done"`, `"yes"`

---

## 🧠 AI Behavior

Each AI has:
- Access to **market conditions**
- Memory of **recent transactions**
- Emotional traits like **jealousy, competitiveness, or generosity**
- Ability to **refuse bad deals** or offer better prices on specialty items
- Negotiation style that varies per shop

---

## 🎯 Objective

> **Buy low, sell high, and build the biggest profit!**

---

## 🧹 Reset Game

To reset your session and start over:

---

## ⚠️ Notes

- Prices update every **30 seconds** based on **volatility & demand**.
- AI deal validation happens only if the message includes specific formats or confirmation phrases.
- Data is stored in **Flask session** only (not persistent after server restarts).

---

## 📌 Future Ideas

- 📉 Real-time trend charts using Chart.js
- 🧑‍🤝‍🧑 Multiplayer mode with leaderboards
- 🏴‍☠️ Black market system with higher risk/reward
- 🧾 Loan or banking system
- 💼 Inventory storage limits or dynamic demand events

---

## 🙌 Author

Made with ❤️ by **Harsimran**  
Assisted by your friendly AI sidekick 😎

---

> **"Why just play games, when you can build them with AI?"**

