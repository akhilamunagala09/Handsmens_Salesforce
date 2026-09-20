# HandsMen Threads: Elevating the Art of Sophistication in Men's Fashion

## 📌 Project Overview

HandsMen Threads is a Salesforce CRM project developed for a men's fashion business to manage customers, products, orders, inventory, and loyalty activities in a centralized system.

The project uses Salesforce declarative automation and Apex programming to automate business processes, improve data accuracy, and reduce manual work.

## 🎯 Objectives

- Manage customer, product, order, and inventory information.
- Automate order confirmation notifications.
- Generate low-stock alerts.
- Automatically update customer loyalty status.
- Validate business data using Salesforce Validation Rules.
- Implement Salesforce Flows for business automation.
- Use Apex, Batch Apex, and Scheduled Apex for customized and recurring operations.
- Improve operational efficiency and data visibility.

## 🛠️ Technologies Used

- Salesforce CRM
- Salesforce Lightning App
- Custom Objects
- Custom Fields
- Validation Rules
- Email Templates
- Email Alerts
- Salesforce Flows
- Apex
- Batch Apex
- Scheduled Apex
- Profiles and Roles
- Permission Sets

## 📦 Custom Objects

The project includes the following custom objects:

- **HandsMen Customer**
- **HandsMen Product**
- **HandsMen Order**
- **Inventory**
- **Marketing Campaign**

Important fields include:

- `Total_Purchases__c`
- `Loyalty_Status__c`
- `Stock_Quantity__c`
- `Total_Amount__c`

## ⚙️ Key Features

### 1. Customer Management

Customer records can be created and managed in Salesforce along with purchase information and loyalty status.

### 2. Product & Inventory Management

Products and stock quantities are maintained in Salesforce. Low-stock products can be identified automatically.

### 3. Order Management

Orders contain customer, product, quantity, status, and total amount information.

### 4. Order Confirmation Flow

A Record-Triggered Flow automatically sends an Order Confirmation Email when an order status changes to **Confirmed**.

### 5. Low Stock Alert

The Stock Alert Flow monitors inventory and sends a Low Stock Alert when stock falls below the configured threshold.

### 6. Loyalty Status Automation

The Loyalty Status Update Flow evaluates customer purchases and assigns:

- **Gold** – More than 1000
- **Silver** – Between the defined limits
- **Bronze** – Less than 500

### 7. Inventory Batch Processing

`InventoryBatchJob` uses Batch Apex and Scheduled Apex to process low-stock products and apply the project's inventory restocking logic.

The job is scheduled to run daily at **2:00 AM**.

### 8. Loyalty Points Processing

`LoyaltyPointsBatch` is used for loyalty-related batch processing.

`LoyaltyPointsScheduler` launches the loyalty batch process on a weekly schedule.

**Schedule:** Every Sunday at 12:00 AM.

## 🔄 Project Workflow

```text
Customer Registration
        ↓
Product Management
        ↓
Order Creation
        ↓
Order Confirmation
        ↓
Confirmation Email
        ↓
Inventory Update
        ↓
Low Stock Alert
        ↓
Loyalty Status Update
        ↓
Scheduled Apex Processing
