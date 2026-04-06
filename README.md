# 📦 Stock Management System — Python

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)

A console-based **Stock Management System** built with Python that helps businesses efficiently track, manage, and report on their inventory. The system provides a simple yet powerful interface for adding products, updating stock quantities, monitoring low-stock alerts, recording sales, and generating inventory reports — all stored persistently using file-based or database storage.

---

## 📋 Table of Contents

- [Description](#-description)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 📖 Description

The **Stock Management System** is a Python application designed for small businesses, retail shops, and academic projects. It provides a menu-driven interface to manage product inventory end-to-end — from adding new items to recording sales and viewing stock reports.

The system is ideal for:
- Retail shops needing a lightweight inventory tool
- Students learning Python with real-world CRUD applications
- Businesses that want a simple, offline stock tracker

---

## ✨ Features

| Feature | Description |
|---|---|
| ➕ Add Products | Add new items with name, category, price, and quantity |
| ✏️ Update Stock | Modify product details or restock quantities |
| 🗑️ Delete Products | Remove discontinued or outdated products |
| 🔍 Search | Search products by name, ID, or category |
| 📉 Low Stock Alerts | Automatically flags items below a defined threshold |
| 🛒 Record Sales | Deduct sold quantities and maintain a sales log |
| 📊 Reports | View full inventory summary and sales history |
| 💾 Data Persistence | All data is saved and reloaded across sessions |

---

## 🛠️ Tech Stack

- **Language:** Python 3.8+
- **Storage:** CSV files / SQLite (file-based, no external DB required)
- **Libraries:** `os`, `csv`, `sqlite3`, `datetime`, `tabulate`
- **Interface:** Command-line (Menu-driven)

---

## ⚙️ Installation

Follow these steps to set up the project on your local machine.

### Prerequisites

Make sure you have **Python 3.8 or higher** installed.

```bash
python --version
```

### Step 1 — Clone the Repository

```bash
git clone https://github.com/niran-123/Stock_Management_System_python.git
cd Stock_Management_System_python
```

### Step 2 — (Optional) Create a Virtual Environment

```bash
python -m venv venv

# Activate on Windows
venv\Scripts\activate

# Activate on macOS/Linux
source venv/bin/activate
```

### Step 3 — Install Dependencies

```bash
pip install tabulate
```

> All other libraries (`os`, `csv`, `sqlite3`, `datetime`) are part of Python's standard library — no extra installation needed.

### Step 4 — Run the Application

```bash
python main.py
```

---

## 🖥️ Usage

Once the application starts, you will see a menu like this:

```
╔══════════════════════════════════╗
║    STOCK MANAGEMENT SYSTEM       ║
╠══════════════════════════════════╣
║  1. Add Product                  ║
║  2. View All Products            ║
║  3. Update Product               ║
║  4. Delete Product               ║
║  5. Search Product               ║
║  6. Record a Sale                ║
║  7. View Low Stock Alerts        ║
║  8. Generate Inventory Report    ║
║  9. Exit                         ║
╚══════════════════════════════════╝
Enter your choice:
```

### Example — Adding a Product

```
Enter your choice: 1

Enter Product Name   : Wireless Mouse
Enter Category       : Electronics
Enter Price (₹)      : 799
Enter Quantity       : 50

✅ Product added successfully!
```

### Example — Viewing All Products

```
Enter your choice: 2

+----+----------------+-------------+--------+----------+
| ID | Name           | Category    | Price  | Quantity |
+----+----------------+-------------+--------+----------+
|  1 | Wireless Mouse | Electronics | ₹799   | 50       |
|  2 | Notebook A4    | Stationery  | ₹45    | 200      |
|  3 | USB-C Cable    | Electronics | ₹299   | 15       |
+----+----------------+-------------+--------+----------+
```

### Example — Low Stock Alert

```
Enter your choice: 7

⚠️  LOW STOCK ALERT — Items below threshold (20 units):

+----+-------------+-------------+-------+----------+
| ID | Name        | Category    | Price | Quantity |
+----+-------------+-------------+-------+----------+
|  3 | USB-C Cable | Electronics | ₹299  | 15       |
+----+-------------+-------------+-------+----------+
```

### Example — Recording a Sale

```
Enter your choice: 6

Enter Product ID    : 1
Enter Quantity Sold : 5

✅ Sale recorded! Remaining stock for "Wireless Mouse": 45 units.
```

---

## 📁 Project Structure

```
Stock_Management_System_python/
│
├── main.py               # Entry point — main menu loop
├── products.py           # Product CRUD operations
├── sales.py              # Sales recording and history
├── reports.py            # Inventory & sales report generation
├── database.py           # Data persistence (CSV / SQLite)
├── utils.py              # Helper functions (validation, formatting)
├── data/
│   ├── products.csv      # Product records (auto-generated)
│   └── sales.csv         # Sales log (auto-generated)
└── README.md             # Project documentation
```

---

## 🤝 Contributing

Contributions are welcome and greatly appreciated! Here's how you can help:

### Steps to Contribute

1. **Fork** the repository by clicking the "Fork" button on GitHub
2. **Clone** your forked copy:
   ```bash
   git clone https://github.com/your-username/Stock_Management_System_python.git
   ```
3. **Create a new branch** for your feature or fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Make your changes** and commit with a clear message:
   ```bash
   git commit -m "Add: feature description"
   ```
5. **Push** to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
6. **Open a Pull Request** on the original repository describing your changes

### Contribution Ideas
- Add a GUI using **Tkinter** or **PyQt5**
- Integrate a **MySQL / PostgreSQL** database backend
- Add **barcode scanning** support
- Export reports to **PDF or Excel**
- Add **user authentication** (admin/staff roles)
- Write **unit tests** using `pytest`

### Code Style
- Follow **PEP 8** Python coding standards
- Write clear comments and docstrings for all functions
- Keep functions small and focused on a single responsibility

---

## 📄 License

This project is licensed under the **MIT License** — you are free to use, modify, and distribute it for personal or commercial purposes with attribution.

```
MIT License

Copyright (c) 2024 Niranjan (niran-123)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.
```

See the full [LICENSE](LICENSE) file for details.

---

## 📬 Contact

Have a question, found a bug, or want to collaborate? Feel free to reach out!

- **GitHub:** [@niran-123](https://github.com/niran-123)
- **Issues:** [Open an Issue](https://github.com/niran-123/Stock_Management_System_python/issues)

> For bugs or feature requests, please open a GitHub Issue with a clear title and description. For general questions, reach out via GitHub profile.

---

## 🙌 Acknowledgements

- [Python Documentation](https://docs.python.org/3/)
- [Tabulate Library](https://pypi.org/project/tabulate/) — for clean table formatting in the console
- Inspired by real-world inventory management needs in small businesses

---

<p align="center">Made with ❤️ by <a href="https://github.com/niran-123">Niranjan</a></p>
