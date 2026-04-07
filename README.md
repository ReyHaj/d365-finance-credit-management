# d365-finance-credit-management
D365 Finance (X++) portfolio project focused on Credit Management (Accounts Receivable), including data modeling, business logic, and integrations.
## # 💼 D365 Finance – Credit Management System (Portfolio Project)

## 📌 Project Overview

This project simulates a real-world **Credit Management module** in Microsoft Dynamics 365 Finance (D365 F&O), focused on the **Accounts Receivable (AR)** domain.

The goal is to design and implement a system that helps finance teams monitor customer credit exposure, assess risk levels, and support financial decision-making.

---

## 🎯 Business Problem

Companies that sell on credit need to answer critical questions:

* Can this customer buy on credit?
* Has the customer exceeded their credit limit?
* What is the current outstanding balance?
* Is the customer high-risk?
* Should further transactions be blocked?

---

## 💡 Solution Approach

This project builds a simplified Credit Management system that includes:

* Customer credit data tracking
* Risk classification using Enums
* Financial metrics such as:

  * Credit Limit
  * Current Balance
  * Available Credit
  * Overdue Amount
  * Payment Delay Days

---

## 🧱 Data Model (Current Phase)

### 🔹 Table: `CustCreditLimit`

| Field                    | Type              | Description                  |
| ------------------------ | ----------------- | ---------------------------- |
| CustomerAccount          | CustAccount (EDT) | Unique customer ID           |
| CustomerName             | Name (EDT)        | Customer name                |
| CreditLimit              | real              | Maximum allowed credit       |
| CurrentBalance           | real              | Current outstanding balance  |
| AvailableCredit          | real              | Remaining credit             |
| LastTransactionDate      | TransDate         | Last activity date           |
| CreatedDate              | TransDate         | Record creation date         |
| RiskLevel                | Enum              | Customer risk classification |
| PaymentDelayDays         | int               | Delay in payments            |
| OverdueAmount            | real              | Overdue balance              |
| CreditUtilizationPercent | real              | % of credit used             |

---

### 🔹 Enum: `RiskLevel`

* Low
* Medium
* High

Used to classify customers based on financial risk.

---

## ⚙️ Business Logic (Next Phase)

Planned implementation:

* Calculate Available Credit
* Calculate Credit Utilization %
* Assign Risk Level dynamically
* Identify customers exceeding limits

---

## 🗂️ Project Structure

```
d365-finance-credit-management/
│
├── README.md
├── docs/
│   ├── architecture.png
│   ├── scenarios.md
│
├── src/
│   ├── tables/
│   ├── enums/
│   ├── extensions/
│   ├── classes/
│   ├── dataEntities/
│
├── integration/
│
└── test/
```

---

## 🚀 Development Roadmap

### Phase 1 (Current)

* X++ Basics
* Table design
* Enum usage
* Basic conditions (if)

### Phase 2

* Table Extensions
* Adding custom fields to standard tables

### Phase 3

* Business Logic in Classes
* Credit calculations

### Phase 4

* Data Entities
* Integration (OData / APIs)

### Phase 5

* Testing (SIT/UAT simulation)
* Documentation & architecture

---

## 🧠 Learning Goals

* Understand X++ fundamentals
* Apply D365 best practices (Extensions, no overlayering)
* Work with Finance domain concepts (AR, Credit, Risk)
* Build a real-world portfolio project

---

## 📈 Business Value

This system helps:

* Reduce financial risk
* Improve credit control
* Increase visibility on customer exposure
* Support finance decision-making

---

## 📌 Notes

* This is a **learning-driven project** with a real-world approach
* Development is done step-by-step to simulate real implementation

---

## 🔗 Author

Reyhaneh Hajili
Dynamics 365 Finance Functional Consultant → Future Technical Consultant 🚀

