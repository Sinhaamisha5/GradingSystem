Project Overview: Grade Equivalency Lookup System
Build a Flask + React web app to look up US grade point equivalents for universities across countries (Ghana, China, etc.) based on Excel data.

🧱 1. Project Structure
bash
Copy
Edit
clgproj/
├── app.py                      # Flask backend entry point
├── ghana.py                   # Grade logic for Ghana
├── china.py                   # Grade logic for China
├── University List.xlsx       # Excel file with grading data
└── grade-lookup/              # React frontend project
⚙️ 2. Backend Setup (Python + Flask)
🔹 Required Python Packages
Install via pip:

bash
Copy
Edit
pip install flask flask-cors pandas openpyxl
📦 Packages Used:
Package	Purpose
flask	Web server framework
flask-cors	Enable frontend-backend communication (CORS)
pandas	Load and manipulate Excel files
openpyxl	Excel file engine for .xlsx support
🔹 Running the Backend
bash
Copy
Edit
python app.py
Flask runs on http://localhost:5000
API Endpoints:
GET /get_grade_point → Ghana
GET /get_China_grade_point → China
💻 3. Frontend Setup (React)
🔹 Initialize React App
Navigate to your folder and run:

bash
Copy
Edit
npx create-react-app grade-lookup
cd grade-lookup
🔹 Run the React App
bash
Copy
Edit
npm start
React runs on http://localhost:3000
🔧 4. Frontend: API Integration and Encoding Fix
✨ Packages Used:
Package	Purpose
react	UI library
fetch API	Send GET requests to Flask API
No additional packages were installed — pure React + Fetch was used.

🔹 Encoding Fix for A+ Grade
Used encodeURIComponent(grade) in React to convert A+ to A%2B.
Flask backend modified to interpret both A+ and A%2B.
🗂️ 5. Excel File Structure (University List.xlsx)
Sheet: Ghana University List
University List	Format
Academic City University College	Format 22 / Format 23
Sheet: Ghana Formats
Format	A+	A	B+	B	...
Format / US Grade Points	4.0	3.75	...	...	
Format 22	A+	A	B+	B	...
Format 23	100	90	80	75	...
🔐 6. CORS Configuration (Backend)
python
Copy
Edit
from flask_cors import CORS

app = Flask(__name__)
CORS(app)  # Enable CORS for all routes
🧩 7. Key Fixes Implemented
Fix	Description
Grade encoding (A+)	Encoded A+ as A%2B in frontend, decoded in backend
Excel reading without headers	Handled with header=None for format sheet
Grade normalization	Removed spaces, normalized ＋ to +, and compared case-insensitive
Multiple API endpoints	Supported different countries via modular routes
Dynamic frontend switching	Frontend buttons to switch between countries and APIs
📦 Summary of Installed Tools
Tool/Package	Installed With
Python 3.x	Your local environment
Flask	pip install flask
Flask-CORS	pip install flask-cors
pandas	pip install pandas
openpyxl	pip install openpyxl
React App	npx create-react-app
