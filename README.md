# Persian Attendance Management System
### (سیستم مدیریت حضور و غیاب)

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![PyQt6](https://img.shields.io/badge/GUI-PyQt6-green?logo=qt&logoColor=white)](https://pypi.org/project/PyQt6/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A comprehensive desktop application for managing employee attendance, built with Python and PyQt6. This system is designed specifically for Persian-speaking users, featuring full **Right-to-Left (RTL)** support, **Jalali (Shamsi) calendar** integration, and robust reporting tools.

---

## 📑 Table of Contents
- [Features](#-features)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Technologies Used](#-technologies-used)
- [Contributing](#-contributing)

---

## 🚀 Features

### 🏢 For Administrators
*   **Dashboard:** specialized control panel to manage the entire system.
*   **Employee Management:** Add, edit, and delete employee records (Personal ID, Name, Phone).
*   **Attendance Monitoring:** View real-time attendance logs with advanced filtering (Date range, Specific worker).
*   **Manual Editing:** Ability to manually correct entry/exit times and recalculate work hours.
*   **Advanced Reporting:**
    *   Generate **Monthly Reports** with total days worked and total hours.
    *   Export data to **Excel (XLSX)**, **PDF**, and **CSV**.
    *   Direct printing support.

### 👤 For Employees
*   **Dedicated Panel:** Secure login using Personal ID.
*   **Clock In/Out:** Simple interface to record daily entry and exit times.
*   **History View:** View personal attendance history and status (Working/Completed).
*   **Real-time Clock:** Live Jalali date and time display.

### 🛠 General System
*   **Persian Localization:** Full Persian UI with B Nazanin font support and RTL layout.
*   **Jalali Calendar:** deeply integrated `JalaliDate` for all date inputs, filters, and records.
*   **Database:** Local SQLite database for reliable data storage.

---

## 📥 Installation

### Prerequisites
*   Python 3.8 or higher
*   Git

### Steps

1.  **Clone the repository**
    ```bash
    git clone https://github.com/mobinh8585/attendance-system.git
    cd attendance-system
    ```

2.  **Create a Virtual Environment (Recommended)**
    ```bash
    # Windows
    python -m venv .venv
    .venv\Scripts\activate

    # Linux/macOS
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Font Setup (Optional but Recommended)**
    For the best visual experience, ensure the **"B Nazanin"** font is installed on your system. The application will attempt to use it for a native Persian look.

---

## 🎮 Usage

### Running the Application
Execute the main script from the root directory:

```bash
python main.py
```

### Default Credentials
Upon the first run, the database is automatically created with a default admin account.

*   **Role:** Admin (مدیر)
*   **Username:** `admin`
*   **Password:** `admin123`

### Workflows
1.  **Admin Setup:**
    *   Log in as Admin.
    *   Go to the "مدیریت کارمندان" (Employee Management) tab.
    *   Click "افزودن کارمند جدید" to create new users.
2.  **Worker Attendance:**
    *   Relaunch the app (or logout).
    *   Select "کارمند" (Worker) radio button.
    *   Enter the **Personal Number** assigned by the admin to log in.
    *   Click "ثبت ورود" (Clock In) or "ثبت خروج" (Clock Out).

---

## 📂 Project Structure

```text
attendance-system/
├── database.py              # SQLite database connection and query handler
├── main.py                  # Application entry point
├── requirements.txt         # Python dependencies
├── .gitignore               # Git ignore rules
├── ui/                      # User Interface logic (PyQt6)
│   ├── __init__.py
│   ├── admin_window.py      # Admin dashboard logic
│   ├── dialogs.py           # Pop-up dialogs (Add/Edit workers)
│   ├── login_window.py      # Authentication screen
│   ├── styles.py            # CSS-like stylesheets for QWidgets
│   ├── widgets.py           # Custom widgets (Jalali DatePicker)
│   └── worker_window.py     # Employee panel logic
└── utils/                   # Utility helper functions
    ├── __init__.py
    ├── export_utils.py      # PDF, Excel, and CSV export logic
    └── persian_utils.py     # Number conversion and Date tools
```

---

## 💻 Technologies Used

*   **[PyQt6](https://pypi.org/project/PyQt6/):** Core GUI framework.
*   **[PersianTools](https://pypi.org/project/persiantools/):** Jalali date conversion and number formatting.
*   **[SQLite3](https://www.sqlite.org/):** Lightweight, serverless database engine.
*   **[Pandas](https://pandas.pydata.org/) & [OpenPyXL](https://openpyxl.readthedocs.io/):** Excel data manipulation and export.
*   **[ReportLab](https://www.reportlab.com/):** Professional PDF report generation.
*   **[Arabic-Reshaper](https://pypi.org/project/arabic-reshaper/) & [Python-Bidi](https://pypi.org/project/python-bidi/):** Correct rendering of Persian text in PDFs.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
