Sure! Here's a more detailed `README.md` that includes descriptions of all key features and functions in your COVID-19 Patient Management System project:

---

# COVID-19 Patient Management System

A desktop application built with **Tkinter** and **MySQL** to manage COVID-19 patient data. The system provides functionalities for adding, updating, deleting, and tracking patients' health status in real time.

---

## 💡 Features

### 🧑‍💻 Admin Login

* **Login interface** with username and password validation.
* Credentials are verified from the `login` table in the MySQL database.

### ➕ Add Patient

* Input fields for:

  * Name
  * Age
  * Gender
  * Contact
  * Address
  * City
  * Aadhar Number
* Automatically assigns a unique patient ID.
* Saves the record into the `patients` table.

### 📄 View Patients

* Lists all patient records in a treeview.
* Columns include: ID, Name, Age, Gender, Contact, Address, City, Aadhar.

### ✏️ Update/Delete Patient

* Select a patient from the list and:

  * Update patient information
  * Delete the patient from the database

### ⚰️ Mark as Deceased

* Change a patient's status to "Deceased".
* Updates the patient’s status in the database.

### 💚 Mark as Cured

* Marks a patient as "Cured".
* Useful for tracking recoveries.

### 📊 Statistics

* Displays:

  * Total patients
  * Active cases
  * Cured patients
  * Deceased patients

---

## 🗃️ Database Tables

### `login`

| Field    | Type        |
| -------- | ----------- |
| username | VARCHAR(50) |
| password | VARCHAR(50) |

### `patients`

| Field   | Type         |                   |
| ------- | ------------ | ----------------- |
| id      | INT (PK)     |                   |
| name    | VARCHAR(100) |                   |
| age     | INT          |                   |
| gender  | VARCHAR(10)  |                   |
| contact | VARCHAR(15)  |                   |
| address | TEXT         |                   |
| city    | VARCHAR(50)  |                   |
| aadhar  | VARCHAR(20)  |                   |
| status  | VARCHAR(20)  | (Default: Active) |

---

## 🛠️ Installation & Setup

### Prerequisites

* Python 3.x
* MySQL Server
* MySQL Connector for Python

### Install Dependencies

```bash
pip install mysql-connector-python
```

### Setup Instructions

1. Create the required database and tables in MySQL (see schema above).
2. Update the database connection details (`host`, `user`, `password`, `database`) in the code.
3. Run the application:

```bash
python main.py
```

---

## 📸 Screenshots (Optional)

*Add screenshots here to show GUI screens like login, dashboard, stats, etc.*

---

## 📌 License

This project is licensed under the MIT License.

---

Let me know if you want to include mock data, SQL schema files, or an ER diagram!
