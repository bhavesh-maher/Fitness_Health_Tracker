# 🏋️‍♂️ Fitness Health Tracker  

A wellness web app to log meals and workouts, automatically calculate calories, track weekly progress, and estimate eco impact from walking. Built with **Python (Flask)**, **HTML (Jinja2 templates)**, and **MySQL**.

---

## ✨ Features  

- **🍎 Automatic fruit calories**  
  Enter a fruit name → get accurate calorie estimates based on per‑100g nutrition values and sensible default portions.  

- **🏃 Smart exercise tracking**  
  Calculates calories burned using standard **MET formulas** and your profile data (weight, height, age).  

- **📊 Weekly insights**  
  Total & average calories, calorie balance, workout minutes, distance walked, sessions, streaks, badges, and coaching tips.  

- **🌍 Environmental impact**  
  Estimates distance walked and CO₂ saved for walking activities.  

- **🔐 Secure authentication**  
  Register/login with hashed passwords and session‑based access.  

- **📂 Data browsing**  
  View recent entries for users and food logs.  

- **🔗 Simple REST API**  
  Fetch summary stats for external clients.  

---

## 🏗️ Architecture  

- **Backend:** Flask application with routes for landing, authentication, dashboard, logging, and API.  
- **Frontend:** Jinja2 templates for HTML pages (landing, login, register, dashboard, entries).  
- **Static assets:** CSS served via Flask’s static file support.  
- **Database:** MySQL stores users, food logs, exercise logs, and environment logs. Includes schema + optional trigger fixes.  
- **Data flow:** User actions → logs (food/exercise) → dashboard insights. Walking logs also update environmental impact.  

---

## 📂 Directory Structure  
Fitness Health Tracker/
├─ finess_health_tracker_backend/
│  ├─ app.py
│  ├─ config.py
│  ├─ static/
│  │  └─ style.css
│  ├─ templates/
│  │  ├─ index.html
│  │  ├─ login.html
│  │  ├─ register.html
│  │  ├─ dashboard.html
│  │  └─ entries.html
│  ├─ README.md
│  ├─ fix_database_triggers.py
│  └─ requirements.txt
├─ requirement.txt
├─ fitness_tracker_db.sql
├─ fix_triggers.sql
├─ fix_user_summary_error.sql
├─ Database_Flowchart*.mmd
└─ ER_Diagram.mmd



---

## ⚙️ Setup  

### Prerequisites  
- Python **3.13+**  
- MySQL Server  

### Installation  
```bash
python -m venv .venv
.\.venv\Scripts\python -m pip install -r requirement.txt


Run Server

.\.venv\Scripts\python finess_health_tracker_backend\app.py
Open http://127.0.0.1:5000/
