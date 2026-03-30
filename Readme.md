# Pipo Automatic Budgeting Assistant 💸🤖

Pipo is an intelligent, automated personal finance assistant designed to help users seamlessly track, categorize, and optimize their daily expenses. By leveraging Open Banking APIs and Machine Learning, Pipo transforms raw transactional data into actionable financial insights.

## 🎯 Project Overview

Managing personal finances shouldn't be a manual, tedious task. Pipo automates the budgeting process through a two-phased approach:

* **Phase 1: Open Banking Integration (Data Ingestion)**
    Securely connects to user bank accounts via PSD2-compliant Open Banking APIs. It fetches transactional data and normalizes it into a unified, structured local dataset (e.g., CSV/JSON/Database), ensuring the user has a complete and up-to-date ledger of their expenses without manual data entry.
* **Phase 2: Smart Budgeting Model (Machine Learning)**
    Utilizes a lightweight Machine Learning model trained on the user's transactional history. The model automatically categorizes new expenses, identifies spending anomalies, predicts future cash flow trends, and provides personalized budgeting recommendations to help the user save money.

## ✨ Features

* **Automated Sync:** Real-time or scheduled fetching of bank transactions.
* **Data Normalization:** Standardizes data from multiple banking providers into a single schema.
* **AI-Powered Categorization:** Automatically assigns categories (e.g., Groceries, Utilities, Entertainment) to raw transaction strings using NLP/ML.
* **Budget Forecasting:** Predictive analytics to warn users before they overspend in specific categories.
* **Privacy-First:** Designed to keep sensitive financial data secure, processing ML insights locally where possible.

## 🏦 Open Banking Integration & PSD2 Compliance

**Pipo Automatic Budgeting Assistant** leverages Open Banking APIs to securely fetch real-time financial data. This integration is strictly compliant with the European **PSD2 (Payment Services Directive 2)**, ensuring the highest standards of data security and user privacy.

### How It Works:

Our architecture relies on a secure, token-based flow mediated by an authorized Account Information Service Provider (AISP):

1. **User Consent & OAuth2:** The user explicitly grants Pipo read-only access to their bank account. Pipo initiates a secure OAuth2 flow.
2. **Strong Customer Authentication (SCA):** The user is redirected to their own bank's official portal or app to authenticate (e.g., via biometrics or OTP). **Pipo never sees, intercepts, or stores the user's banking credentials (username/password).**
3. **Encrypted Token Exchange:** Once the user authorizes the connection, the bank issues a secure, time-limited, and revocable access token to the AISP.
4. **Data Retrieval:** Pipo uses this token to securely retrieve raw transaction data and account balances. The data is then processed through our normalization and categorization algorithms to generate automated budgeting insights.

**Official Resource:** For more detailed information on the regulatory framework ensuring the security of this process, please refer to the [Official European Commission documentation on the Payment Services Directive (PSD2)](https://finance.ec.europa.eu/consumer-finance-and-payments/payment-services/payment-services_en).

## 🔒 Security & PSD2 Compliance

Handling financial data requires strict adherence to security protocols. Pipo is designed with the following principles:
* **Read-Only Access:** The application strictly uses read-only API scopes. It cannot move funds or initiate payments.
* **Token Management:** Secure handling of OAuth2 tokens with automatic rotation and encrypted storage.
* **Data Privacy:** Minimal data retention. The ML model is trained on anonymized or strictly local data to ensure user privacy.

## 🚀 Getting Started

### TBD : Prerequisites



### TBD: Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/pipo-budgeting-assistant.git](https://github.com/yourusername/pipo-budgeting-assistant.git)
   cd pipo-budgeting-assistant
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `.env` file in the root directory and add your API credentials:
   ```env
   OPEN_BANKING_CLIENT_ID=your_client_id
   OPEN_BANKING_SECRET=your_client_secret
   ENVIRONMENT=sandbox
   ```


## 🛣️ Roadmap
- [ ] Phase 1: Implement basic OAuth2 flow and API data fetching.
- [ ] Phase 1: Create the data normalization pipeline.
- [ ] Phase 2: Build and train the transaction categorization model.
- [ ] Phase 2: Implement the budgeting recommendation engine.
- [ ] Integration: Connect the ML pipeline to live Open Banking data.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
