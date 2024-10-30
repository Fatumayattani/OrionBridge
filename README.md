# OrionBridge

OrionBridge is a cross-border remittance platform designed to enable fast, low-cost, and transparent money transfers using stablecoins pegged to African currencies. Built on the Internet Computer (ICP) with a Motoko backend and a React.js frontend, OrionBridge aims to empower individuals and communities in Africa by simplifying the remittance process.

---

## Table of Contents

- [Problem Statement](#problem-statement)
- [Solution](#solution)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Smart Contract Development](#smart-contract-development)
- [Frontend Development](#frontend-development)
- [AI-Powered Fraud Detection](#ai-powered-fraud-detection)
- [Contributing](#contributing)
- [License](#license)

----

## Problem Statement

Traditional remittance services like Western Union are expensive and slow, making it difficult for African diaspora communities to send money home. High fees and lengthy processing times hinder financial support to families and businesses in need.

---

## Solution

OrionBridge offers a remittance platform that allows users to send stablecoins over ICP, with an option for on-demand conversion to Bitcoin or Ethereum. This solution minimizes costs and enhances the speed of transactions.

---

## Features

- **Stablecoin Remittances:** Send stablecoins pegged to local African currencies.
- **On-Chain Currency Conversion:** Convert stablecoins to Bitcoin or Ethereum seamlessly.
- **Transparent Fee Structure:** ICP dashboard provides real-time visibility of transaction fees.
- **AI-Powered Fraud Detection:** Monitor unusual activities to protect users and transactions.
- **User-Friendly Interface:** A responsive React.js frontend ensures easy navigation and transaction processing.

---

## Technologies Used
- **Internet Computer (ICP):** The underlying blockchain platform.
- **Motoko:** The programming language used for developing canisters (smart contracts) on ICP.
- **React.js:** The frontend framework for building the user interface.
- **Ethereum and Bitcoin Integration:** For seamless transactions and currency conversion.
- **AI/ML Tools:** For fraud detection and monitoring.

---

## Project Structure
```
/orionbridge
├── /backend                   # Contains Motoko canister code
│   ├── src
│   ├── dfx.json
│   └── ...
├── /frontend                  # Contains React.js application code
│   ├── public
│   ├── src
│   └── ...
├── README.md                  # This README file
└── ...
```

## Installation
To get started with OrionBridge, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Fatumayattani/OrionBridge.git
   cd OrionBridge
   ```
2. **Install the necessary tools:**
   - Make sure you have the [DFX CLI](https://internetcomputer.org/docs/developers-guide/install-dfx) installed for developing with ICP.
   - Install [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/get-npm) for React.js.
3. **Install dependencies for the frontend:**
   ```bash
   cd frontend
   npm install
   ```    

 ## Usage

### Running the Backend
1. **Navigate to the backend directory:**
   ```bash
   cd backend
   ```
2. **Deploy the Motoko canisters:**
   ```bash
   dfx deploy
   ```   
### Running the Frontend

1. **Navigate to the frontend directory:**
   ```bash
   cd frontend
   ```   
2. **Start the React application:**
   ```bash
   npm start
   ```   
3. Open your browser and go to `http://localhost:3000` to access the OrionBridge application. 

---

## Smart Contract Development

This section provides an overview of the smart contracts (canisters) developed in Motoko for OrionBridge.

- **Canister Overview:** The canisters handle stablecoin transactions, currency conversion, and user interactions.
- **Integration with Ethereum and Bitcoin:** The canisters communicate with Ethereum and Bitcoin networks to facilitate transactions and conversions.  
