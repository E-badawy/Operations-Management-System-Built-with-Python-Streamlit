# Operations-Management-System-Built-with-Python-Streamlit

A robust inventory and staff management system built for Medhal Nigeria Limited. 
The system allows role-based access (Admin, Store, Account), tracking of stock in/out,
history, and staff records with a clean, navigable sidebar interface.

## 🔹 Features
- Role-based login: **Admin**, **Store**, **Account**
- **Stock In / Stock Out** management
- **Stock History** and **Records** tracking
- **Staff Records** management
- Clean **sidebar navigation**
- Real-time updates via **database integration**
- Multi-user readiness (local and potential cloud deployment)

## 🔹 Logic & Workflow

1. **Login System**
   - Users assigned roles (Admin, Store, Account)
   - Session-state based authentication
   - Secure access to role-specific pages

2. **Inventory Management**
   - Stock In: Add items to inventory
   - Stock Out: Deduct items from inventory
   - Stock History: Track all transactions

3. **Staff Management**
   - Add, view, and edit staff details
   - Link staff actions to inventory changes

4. **Database Integration**
   - Centralized PostgreSQL/MySQL database
   - Tables: `users`, `stock_in`, `stock_out`, `staff`, `history`
   - DB connection handled in `db.py`

5. **Rerun / State Handling**
   - Session state manages logged-in users
   - `st.stop()` used to trigger safe rerun on login/logout

## 🔹 Requirements
- Python 3.10+
- Streamlit >= 1.22
- psycopg2 / mysql-connector-python (depending on DB)
- pandas
- Optional: Git for cloning

## Screenshots
![Login Page](images/login_page.png)
![Dashboard](images/oms_dashboard.png)
![Login Page](images/login_page.png)
![Dashboard](images/oms_dashboard.png)

## Setup & Run Instructions

1. **Clone the repository**
```bash
git clone https://github.com/e-badawy/superstore_offline.git
python -m venv .venv
# Windows
.venv\Scripts\activate
```
```
# macOS/Linux
source .venv/bin/activate
pip install -r requirements.txt
```

*Set up the database*

Create a PostgreSQL/MySQL database

Run db_setup.sql (if exists) to create tables

Update db.py with your connection credentials

🔹 *Project Structure*
```
superstore_offline/
│
├─ app.py                 # Main Streamlit app
├─ db.py                  # Database connection & queries
├─ requirements.txt       # Python dependencies
├─ db_setup.sql           # SQL tables creation
├─ images/                # Screenshots and GIFs
└─ other_modules/         # Optional helper scripts
```
