# 🧾 Employee Attendance Tracker using Google Sheets

An automated, user-friendly attendance management system built entirely in **Google Sheets** – no coding required! This project demonstrates how to efficiently track and visualize employee attendance with real-time dashboards, formulas, charts, progress bars, and emoji-based performance indicators.

---

## 📌 Features

- ✅ Dropdown-based attendance marking (Present, Absent, Leave)
- 🔢 Automatic summary of attendance per employee
- 📊 Visual dashboards using charts (Pie, Bar, Line, Doughnut)
- 📈 Attendance percentage calculation
- 📎 Emoji-based performance badges (Excellent, Good, Warning, Poor)
- 🟦 Dynamic progress bars for visual feedback
- ☁️ Cloud-based & collaborative (Google Sheets)

---

## 🏗️ Sheet Structure

| Sheet Name         | Purpose                                                    |
|--------------------|------------------------------------------------------------|
| `Attendance Log`   | Raw daily entries with Date, ID, Name, and Status          |
| `Employee Summary` | Computes individual attendance stats and visual feedback   |
| `Charts`           | Dashboard with multiple interactive visual charts          |
| `Settings` (opt)   | Centralized dropdowns or employee master data (optional)   |

---

## 🧮 Key Formulas Used

- **Unique Employee List:**  
  `=UNIQUE('Attendance Log'!B2:B)`

- **Lookup Name from ID:**  
  `=VLOOKUP(A2, 'Attendance Log'!B2:C, 2, FALSE)`

- **Count Present Days:**  
  `=COUNTIFS('Attendance Log'!B:B, A2, 'Attendance Log'!D:D, "P")`

- **Count Absent Days:**  
  `=COUNTIFS('Attendance Log'!B:B, A2, 'Attendance Log'!D:D, "A")`

- **Count Leave Days:**  
  `=COUNTIFS('Attendance Log'!B:B, A2, 'Attendance Log'!D:D, "L")`

- **Attendance Percentage:**  
  `=IF(TotalDays=0, "", Present/TotalDays)`

- **Progress Bar:**  
  `=REPT("█", ROUND(Percentage*10)) & REPT("░", 10 - ROUND(Percentage*10))`

- **Emoji Performance Status:**  
  `=IF(Percentage>=0.9,"✅ Excellent", IF(Percentage>=0.75,"🟡 Good", IF(Percentage>=0.5,"⚠️ Warning","❌ Poor")))`

---

## 📊 Charts Included

- Bar Chart: Present Days per Employee  
- Pie Chart: Distribution of P/A/L
- 
---

## 💡 How to Use
1. Hit the View Button in "Employee Attendance Tracker.xlsx" file, to download in your System.
1. Or **Make a copy** of the Google Sheet template.
2. Enter data in the `Attendance Log` tab.
3. Watch the `Employee Summary` and `Charts` tabs auto-update.
4. Share the sheet or publish it as a dashboard.

---

## 📈 Future Enhancements

- 🔗 Google Forms for attendance input  
- 📤 App Script integration for automation  
- 💰 Payroll linkage  
- 👥 Employee login and self-service dashboard

---

## 📃 License

This project is open-source under the [MIT License](LICENSE).

---

## 🧑‍💻 Author

**Yash Kumar Nigam** 
