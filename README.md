# 📊 Grade Equivalency Lookup System

A full-stack web application to fetch **US grade point equivalents** for universities in **Ghana**, **China**, and **Nigeria** using Excel-based grading formats.

---

## 🗂️ Project Structure
```
clgproj/                   # Project Root
├── app.py                # Flask backend entry point
├── ghana.py              # Ghana grade logic
├── china.py              # China grade logic
├── nigeria.py            # Nigeria grade logic
├── University List.xlsx  # Excel data file (excluded from Git)
└── grade-lookup/         # React frontend app
```

---

## ⚙️ Backend Setup (Flask)

### 1. Install Dependencies
```bash
pip install flask flask-cors pandas openpyxl
```

### 2. Run Flask Server
```bash
python app.py
```
> Flask runs at: `http://localhost:5000`

### API Endpoints:
| Endpoint                                | Country  |
|----------------------------------------|----------|
| `/get_grade_point`                     | Ghana    |
| `/get_China_grade_point`               | China    |
| `/get_Nigeria_grade_point`             | Nigeria  |

---

## 💻 Frontend Setup (React)

### 1. Initialize React App
```bash
cd grade-lookup
npm install
```

### 2. Run React Server
```bash
npm start
```
> React runs at: `http://localhost:3000`

### Features:
- Buttons to select **country**
- Input fields for **University** and **Grade**
- Result display with **US GPA equivalents**

---

## 📦 Packages Used

### Backend:
| Package      | Purpose                          |
|--------------|----------------------------------|
| `flask`      | Web server framework             |
| `flask-cors` | Enable frontend-backend requests |
| `pandas`     | Excel file reading               |
| `openpyxl`   | `.xlsx` file engine              |

### Frontend:
| Tool         | Purpose                          |
|--------------|----------------------------------|
| `react`      | UI framework                     |
| `fetch API`  | API requests                     |

---

## 🧾 Notes
- **Excel File** (`University List.xlsx`) is **excluded from Git**.
- Excel sheets must include:
  - `Ghana University List`, `Ghana Formats`
  - `China University List`, `China Formats`
  - `Nigeria University List`, `Nigeria Formats`
- Special grades like `A+` should be URL-encoded as `A%2B`.

---

## 🚀 Future Enhancements
- Support for **India**
- **File upload** feature for custom Excel files
- Deployment via **Render/Netlify**

---

## 👩‍💻 Author
Developed by **Amisha Sinha**

Let me know if you need help deploying, debugging, or expanding this project! 🚀

