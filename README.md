# Grocery Store Management System

A comprehensive **Grocery Store Management System** developed as a Semester 3 **Object-Oriented Programming (OOP)** project in C++. The project combines a functional console-based application with web-based GUI templates to demonstrate both backend business logic and frontend interface design.

The system allows store owners to manage inventory, purchase stock, sell products, track transactions, monitor profits, and maintain financial records through an interactive menu-driven interface.

---

## Project Overview

This project was developed to apply Object-Oriented Programming concepts in a real-world business scenario. It simulates the daily operations of a grocery store by providing inventory control, transaction tracking, and financial management features.

The repository contains:

- A C++ console-based management system
- Transaction logging using file handling
- Inventory and sales management modules
- Financial tracking and profit calculation
- HTML-based GUI templates for future web integration

---

## Features

### Inventory Management
- Add grocery items to the system
- Purchase stock for existing items
- View available inventory
- Track product quantities

### Sales Management
- Sell products from inventory
- Automatically update stock quantities
- Prevent sales when stock is unavailable

### Transaction Management
- Record stock purchases
- Record product sales
- View complete transaction history
- Save transaction records to a log file

### Financial Management
- Maintain available store funds
- Deduct purchasing costs
- Add sales revenue
- Calculate total profit

### File Handling
- Store transaction records in a text file
- Load existing transaction history (Final Project version)
- Maintain persistent transaction logs

### User Interface
- Interactive console menu
- Tabular display of inventory and transactions
- Clear navigation and user feedback

### Web-Based GUI Templates
- HTML templates for a graphical user interface
- Dashboard-style layouts
- Inventory and transaction screens
- Foundation for future web application development

---

## Object-Oriented Programming Concepts Used

### Encapsulation
The `GroceryStore` class encapsulates all inventory, transaction, and financial management operations.

### Abstraction
Complex internal operations are hidden behind simple public methods such as:

- `addStock()`
- `sellItem()`
- `viewStock()`
- `viewTransactions()`
- `viewProfit()`

### Classes and Objects
The system is built around the `GroceryStore` class and supporting data structures.

### Data Structures
The project utilizes:

- Vectors (`vector<Item>`)
- Structures (`Item`, `Transaction`)
- Dynamic memory management through STL containers

### File Handling
The system uses:

- `ifstream`
- `ofstream`

for transaction logging and data persistence.

---

## Project Structure

```text
OOP-Project-S3/
│
├── Final Project.cpp
│   ├── GroceryStore implementation
│   ├── Transaction logging
│   ├── Transaction loading
│   └── Inventory management
│
├── OOP Project.cpp
│   ├── Core GroceryStore implementation
│   ├── Sales and inventory functions
│   └── Financial management
│
├── transaction_log.txt
│   └── Generated transaction records
│
├── HTML Templates/
│   ├── index.html
│   ├── dashboard.html
│   ├── inventory.html
│   ├── transactions.html
│   └── Other UI templates
│
└── README.md
```

---

## Class Design

### Item Structure

Represents a grocery product.

```cpp
struct Item {
    string name;
    double buyPrice;
    double sellPrice;
    int quantity;
};
```

#### Attributes

| Attribute | Description |
|------------|-------------|
| name | Product name |
| buyPrice | Purchase price |
| sellPrice | Selling price |
| quantity | Available stock |

---

### Transaction Structure

Represents a store transaction.

```cpp
struct Transaction {
    string type;
    string itemName;
    int quantity;
    double totalAmount;
};
```

#### Attributes

| Attribute | Description |
|------------|-------------|
| type | Add or Sell |
| itemName | Product name |
| quantity | Quantity involved |
| totalAmount | Total transaction value |

---

### GroceryStore Class

The main class responsible for managing the entire system.

#### Responsibilities

- Inventory management
- Stock purchasing
- Product sales
- Profit calculation
- Financial tracking
- Transaction recording
- File handling

---

## Available Menu Options

```text
----------------------------------------
        Grocery Store Menu
----------------------------------------

1. View Stock
2. Add Stock
3. Sell Item
4. View Transactions
5. View Profit
6. View Money
7. Exit
```

---

## Default Products

The application initializes with the following products:

| Product | Buy Price | Sell Price |
|----------|------------|-------------|
| Apple | 2.00 | 3.00 |
| Banana | 1.50 | 2.50 |
| Milk | 10.00 | 12.00 |
| Bread | 5.00 | 7.00 |
| Eggs | 0.50 | 1.00 |
| Burger | 10.00 | 15.00 |

---

## Transaction Logging

Every stock purchase and sale is automatically recorded.

### Example

```text
Add, Apple, 10, 20
Sell, Apple, 5, 15
Add, Bread, 4, 20
Sell, Bread, 2, 14
```

The records are stored in:

```text
transaction_log.txt
```

---

## Financial System

The application starts with:

```cpp
1000.0
```

units of currency.

### Stock Purchase

When stock is added:

```text
Money = Money - Purchase Cost
```

### Product Sale

When products are sold:

```text
Money = Money + Revenue
```

### Profit Calculation

Profit is calculated as:

```text
Revenue - Cost Price
```

for all sold products.

---

## Web GUI Templates

In addition to the C++ implementation, this project includes web-based interface templates.

### Purpose

The templates demonstrate how the Grocery Store Management System could be transformed into a web application.

### Possible Screens

- Dashboard
- Inventory Management
- Sales Records
- Transaction History
- Profit Reports

### Technologies

- HTML
- CSS
- Responsive Layout Design

> Note: The GUI templates are currently frontend-only and are not connected to the C++ application.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/ZafarAbdulAziz/OOP-Project-S3.git
```

### Navigate to Project Directory

```bash
cd OOP-Project-S3
```

---

## Compilation

### Using GCC

Compile the main project:

```bash
g++ "OOP Project.cpp" -o GroceryStore
```

or

```bash
g++ "Final Project.cpp" -o GroceryStore
```

### Run

Windows:

```bash
GroceryStore.exe
```

Linux/macOS:

```bash
./GroceryStore
```

---

## Sample Workflow

### Add Stock

```text
Enter item name: Apple
Enter quantity: 20
```

### Sell Product

```text
Enter item name: Apple
Enter quantity: 5
```

### View Profit

```text
Total Profit: 5
```

---

## Learning Outcomes

This project demonstrates practical implementation of:

- Object-Oriented Programming
- Classes and Objects
- Encapsulation
- Data Structures
- File Handling
- Inventory Management Systems
- Financial Tracking Systems
- Console Application Development
- Software Design Principles

---

## Future Improvements

- Database integration (MySQL/PostgreSQL)
- User authentication
- Product categories
- Search functionality
- Low-stock alerts
- Receipt generation
- Sales analytics
- Web application backend integration
- REST API support
- Graphical desktop interface

---

## Screenshots

Add screenshots of:

- Main Menu
- Inventory View
- Transaction Records
- Profit Report
- Web GUI Templates

Example:

```markdown
![Main Menu](screenshots/menu.png)
![Inventory](screenshots/inventory.png)
```

---

## Contributors

### Project Developer

**Zafar Abdul Aziz**

Semester 3 – Object-Oriented Programming Project

---

## Course Information

| Field | Information |
|---------|-------------|
| Course | Object-Oriented Programming |
| Semester | S3 |
| Project Type | Academic Semester Project |
| Language | C++ |
| Interface | Console + Web Templates |

---

## License

This project was developed for educational and academic purposes.

Feel free to use, modify, and extend the project for learning and personal development.
