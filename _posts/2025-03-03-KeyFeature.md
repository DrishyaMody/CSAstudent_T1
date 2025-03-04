---
layout: post
title: KeyFeature
comments: True
type: ccc
permalink: /keyfeature
---
## CRYPTO FUNCTIONALITY DIAGRAM

<img src="/CSAstudent_T1/images/draw.io.png" width="600">

# **Investment Portfolio System**

## **Key Features**
### **1. Fetching Live Crypto Data**
- The system **connects to a third-party API** to fetch **real-time cryptocurrency prices** and market data.
- Updates the **crypto portfolio** dynamically based on the latest market trends.
- Ensures accurate valuation of investments by retrieving **price changes in real time**.

### **2. Buy/Sell Functions**
- Allows users to **buy or sell crypto assets** through a secure transaction system.
- Automatically **adjusts the user’s balance** after each trade.
- Transactions are validated before execution to ensure sufficient funds are available.
- Provides a **confirmation message and transaction summary** after every trade.

### **3. Fetching Balance from Person API**
- The system **synchronizes with a personal banking API controller** to:
  - Retrieve the **user’s available balance** before executing trades.
  - Ensure that buy transactions **do not exceed the available funds**.
  - Update the bank balance **after every transaction** for real-time tracking.

### **4. Transaction History**
- Maintains a **detailed log of all past trades**, including:
  - Buy/Sell orders
  - Trade execution time
  - Price at the time of purchase/sale
  - Updated balance after each transaction
- Helps users track **investment patterns and performance** over time.

### **5. Balance History Graph**
- Uses **Chart.js** to generate an **interactive balance history graph**.
- Provides a **visual representation of financial performance** over time.
- Updates dynamically based on:
  - New crypto transactions
  - Fluctuations in market value
  - Deposits or withdrawals from the banking API

---

1. **User views live crypto data** → Market prices are fetched from the API.
2. **User places a Buy/Sell order** → Transaction is executed, and balance is updated.
3. **System updates portfolio** → The investment value is recalculated.
4. **Person API fetches updated balance** → Ensures accurate financial tracking.
5. **Transaction history is recorded** → User can review past transactions.
6. **Balance history graph updates** → Provides a visual insight into portfolio growth.

---


- **Third-Party API Integration** → Fetches real-time crypto data.
- **Person API** → Fetches and updates personal balance.
- **Secure Buy/Sell System** → Manages transactions and updates financial records.
- **Chart.js** → Generates a balance history graph with real-time updates.
- **Database Logging** → Stores transaction history and investment records.

---

## **Conclusion**
The Investment Portfolio System provides a **seamless and automated experience for tracking crypto investments**. With **real-time API integration, secure transactions, and interactive financial insights**, users can make informed decisions and monitor their portfolio’s performance effectively.
