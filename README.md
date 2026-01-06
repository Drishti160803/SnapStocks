# 📈 SnapStocks - Full-Stack Trading Simulator

SnapStocks is a comprehensive virtual trading platform designed to simulate real-world stock market interactions. It allows users to manage a virtual portfolio, track live market data, and execute trades without financial risk.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

## 🌟 Key Features

* **Real-Time Market Data:** Integrated with the Finnhub API to fetch live stock prices from global exchanges.
* **Virtual Wallet:** Each new user starts with $100,000 in virtual currency.
* **Portfolio Management:** Tracks average purchase price, total quantity, and real-time holdings.
* **Secure Authentication:** Protects user data and balances using JWT (JSON Web Tokens) and Bcrypt password hashing.
* **Responsive Dashboard:** A modern, dark-themed UI built with React and CSS Grid for a professional trading feel.

## 🏗️ Technical Architecture



* **Frontend:** React.js, Axios, Styled Components / CSS3.
* **Backend:** Node.js, Express.js.
* **Database:** MongoDB (NoSQL) for flexible portfolio storage.
* **External API:** Finnhub.io for live market quotes.

---

## 🚀 Getting Started

### Prerequisites
* Node.js (v16 or higher)
* MongoDB (Local or Atlas)
* A Finnhub API Key (Free at [finnhub.io](https://finnhub.io))

### Installation

1.  **Clone the repo:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/snap-stocks.git](https://github.com/YOUR_USERNAME/snap-stocks.git)
    cd snap-stocks
    ```

2.  **Setup Backend:**
    ```bash
    cd backend
    npm install
    ```
    *Create a `.env` file in the `backend` folder and add:*
    ```text
    PORT=5000
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_secret_key
    FINNHUB_KEY=your_api_key
    ```
    *Start server:* `npm run dev`

3.  **Setup Frontend:**
    ```bash
    cd ../frontend
    npm install
    npm start
    ```

---

## 🧠 Deep Analysis

### Atomic Transactions
The platform ensures data integrity by performing balance checks on the **server side**. The transaction logic is designed so that a user can never spend more than their available virtual balance, preventing "race conditions" in buying stocks.

### Security
Passwords are never stored in plain text. We utilize **Bcrypt** with a salt factor of 10 to ensure that user credentials remain secure even in the event of a database breach.

## 📄 License
Distributed under the MIT License.

---
**Developed by [Your Name]**
