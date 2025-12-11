# Stratum-LLC-408-Final-Roush-
My github repo for my 408 final for Tibs' class. Yeehaw space cowboy.

# Stratum LLC – Capstone Project

Stratum LLC is a secure web application that allows instructors to upload, manage, and "sell" instructional programs. The application is built with **Python, Flask, and SQLite** and emphasizes secure coding practices, database integration, and controlled environment execution.

---

## **Project Overview**

- Instructors can register, log in, and upload instructional programs.
- Programs include metadata such as title, rating, views, and upload date.
- Users can "purchase" programs to unlock downloads.
- Ratings and view counts are updated dynamically.
- Admin backdoor for site management.
- Secure coding practices: hashed passwords, parameterized queries, access control.

---

## **File Structure**

Stratum-LLC/
│
├─ app.py # Main Flask application with routes, authentication, program management, and purchase logic
├─ requirements.txt # Python dependencies for the project
├─ README.md # Project documentation (this file)
├─ database/ # Folder for SQLite database file
│ └─ stratum.db
├─ templates/ # HTML templates for frontend
│ ├─ base.html
│ ├─ login.html
│ ├─ register.html
│ ├─ dashboard.html
│ ├─ program_view.html
│ └─ admin.html
├─ static/
│ └─ style.css
├─ analysis_scripts/
│ └─ analysis_example.py
└─ uploads/

yaml
Copy code

---

## **File Summaries**

- **app.py**  
  Main Flask application file. Contains routes for login, registration, dashboard, program viewing, uploads, purchase logic, sorting, searching, ratings, and admin backdoor.

- **requirements.txt**  
  Python dependencies. Install with:
  ```bash
  pip install -r requirements.txt
database/stratum.db
SQLite database storing users, programs, and purchases.

templates/
HTML templates for frontend:

base.html – base layout with navbar

login.html – login page

register.html – registration page

dashboard.html – program dashboard with sorting and search

program_view.html – program details page with purchase wall

admin.html – admin panel

static/
CSS and images. style.css for consistent styling.

analysis_scripts/
Optional scripts demonstrating static/dynamic code analysis.

uploads/
Folder for program files. Access restricted until purchased.

Installation & Running the App
Clone the repository:

bash
Copy code
git clone https://github.com/YourUsername/stratum-llc.git
cd stratum-llc
Create a virtual environment:

bash
Copy code
python -m venv venv
source venv/bin/activate      # Linux/macOS
venv\Scripts\activate         # Windows
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Initialize the database (if not preloaded):

bash
Copy code
python app.py
Run the Flask app:

bash
Copy code
flask run
Visit http://127.0.0.1:5000/ in your browser.

Security & Notes
Passwords are hashed using werkzeug.security.

Database queries use parameterized SQL to prevent injection.

Access to uploaded files is protected by purchase logic.

Admin routes are restricted to authorized users only.

App runs in an isolated virtual environment for safety and reproducibility.
