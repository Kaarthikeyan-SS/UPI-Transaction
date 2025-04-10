# UPI Flow Dashboard – Power BI Analytics Project

This Power BI project focuses on analyzing UPI (Unified Payments Interface) transaction flows from customers to merchants. The goal is to derive actionable insights about digital payment patterns, bank interactions, device usage, and customer behavior based on real transaction data.

---

## 📌 Project Objective

With UPI being a dominant digital payment method in India, understanding how transactions behave across banks, devices, and users is crucial for both financial institutions and fintech platforms.

This dashboard answers questions like:
- Which banks are most active as **senders** and **receivers**?
- What is the **success rate** of UPI transactions?
- How do customers prefer to pay — QR Code, UPI ID, or Phone Number?
- Are there noticeable trends based on **customer age, gender, and city**?
- What devices are most commonly used for digital payments?

---

## 🗂 Dataset Overview

The dataset includes 1000+ rows of UPI transaction data with the following columns:

| Column Name              | Description |
|--------------------------|-------------|
| TransactionID            | Unique transaction identifier |
| TransactionDate          | Date of transaction |
| Amount                   | Payment amount |
| BankNameSent             | Sender’s bank name |
| BankNameReceived         | Receiver’s bank name |
| RemainingBalance         | Customer’s remaining balance post-transaction |
| City                     | Customer’s city |
| Gender                   | Customer gender |
| TransactionType          | Transfer or Payment |
| Status                   | Success or Failed |
| TransactionTime          | Time of transaction |
| DeviceType               | Device used (Mobile, Tablet, Laptop) |
| PaymentMethod            | UPI ID, QR Code, or Phone Number |
| MerchantName             | Name of merchant (Amazon, Zomato, etc.) |
| Purpose                  | Purpose of payment (Food, Travel, etc.) |
| CustomerAge              | Age of the customer |
| PaymentMode              | Instant or Scheduled |
| Currency                 | Currency used |
| CustomerAccountNumber    | Obfuscated customer account number |
| MerchantAccountNumber    | Obfuscated merchant account number |

---

## 🎯 Key Features of the Dashboard

### 1. Overview Section
- Total Transactions
- Total Amount Processed
- Transaction Success Rate
- Device Usage Breakdown

### 2. Bank Relationship Analysis
- Top sending and receiving banks
- Sankey-style flow visuals (if needed) for bank connections

### 3. Payment Method & Device Trends
- Most used payment methods
- Device types and their transaction share

### 4. Customer Demographics
- Age and gender distribution
- City-wise usage and trends
- Purpose of payment insights (e.g., food, shopping, travel)

### 5. Transaction Type Comparison
- Transfer vs Payment volumes
- Scheduled vs Instant breakdown
- Failure trends by type

---

## 🧠 Notable Insights

- **Certain banks are more dominant as payment receivers**, indicating their role as merchant banks.
- **Mobile devices** lead UPI transactions by a wide margin, especially in food and travel sectors.
- **Scheduled payments** are commonly used for **peer-to-peer transfers**, while **instant payments** are preferred for purchases.
- **QR Codes and UPI IDs** are the most used payment methods.

---

## 🛠 Tools & Technologies Used

| Tool         | Purpose                      |
|--------------|-------------------------------|
| Power BI     | Data visualization and dashboard creation |
| DAX          | Custom KPIs, measures, and filtering |
| Power Query  | Data cleaning and transformation |
| Excel/CSV    | Original dataset format |

---

## 🧩 DAX Measures Used

- **Total Amount** = `SUM(Amount)`
- **Success Rate** = `DIVIDE(COUNTROWS(SuccessfulTransactions), COUNTROWS(AllTransactions))`
- **Avg Transaction by Device** = `AVERAGEX(VALUES(DeviceType), [Total Amount])`
- **Top Receiving Bank** = `CALCULATE(COUNTROWS(Transactions), ALLEXCEPT(BankNameReceived))`

---

## 📷 Dashboard Preview

![UPI Dashboard](https://github.com/user-attachments/assets/262880b8-52de-4c2c-929a-c8793c02f72d)


