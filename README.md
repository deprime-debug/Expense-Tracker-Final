# Personal Expense Manager

A clean, minimalist, and privacy-first web application designed to help users seamlessly track their monthly income, monitor categorical spending, and visualize financial data in real time. Built using core web technologies, this project emphasizes intuitive user experience (UX) and high-performance client-side state management.

---

## 🚀 Features

### 1. **Financial Summary & Adaptive Budget Strip**
* **Real-time Calculations:** Dynamically updates Monthly Salary, Total Spent, and Remaining Balance fields as transactions are added or removed.
* **Visual Alert System:** Features an interactive budget progress bar that shifts from a calming green gradient to an urgent crimson tone if expenses exceed the designated salary.

### 2. **Granular Transaction Control**
* **Categorized Entry:** Allows users to log transactions under explicit categories: *Food*, *Groceries*, *Fuel*, and *Other*.
* **Data Validation:** Includes input validation with sensory UI flashing alerts on the submission button to flag invalid amounts or blank descriptions.
* **Secure Erasure:** Supports precise single-row transaction deletion alongside a global factory-reset option for data clearing.

### 3. **Dynamic Data Visualization**
* **Distribution Analysis:** Integrates a client-side `Chart.js` bar chart to illustrate absolute expenditure amounts across separate structural pillars.
* **Proportional Allocation:** Features an interactive doughnut chart tracking percent-share distribution of expenses relative to total capital output.

### 4. **Privacy-First Architecture**
* **Zero Server Footprint:** No external databases, analytical tracking, or authentication servers are used.
* **Local Persistence:** Uses native HTML5 Web Storage API (`localStorage`) to preserve transactional data across window reloads and runtime sessions securely within the client browser.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Structure:** HTML5 (Semantic document construction)
* **Styling & Theme:** Custom CSS3 variables, native layouts, and dynamic typography via Google Fonts (*Fraunces*, *Inter*, *IBM Plex Mono*).
* **Charting Core:** `Chart.js` (UMD bundle via CDN)
* **Scripting Engine:** Vanilla JavaScript (ES6+ state control, event handling, local storage synchronization, array streaming).

---

## 📁 Directory Structure

```text
├── index.html          # Monolithic application containing core UI, styles, and logic
└── README.md           # Project documentation and setup guide
```
🔧 Installation & Local Setup
Since this application runs entirely on client-side vanilla architecture, it has zero external dependencies and requires no compilation.

Clone this repository locally:

Bash
git clone [https://github.com/deprime-debug/Expense-Tracker.git](https://github.com/deprime-debug/Expense-Tracker.git)
Navigate to the project root directory:

Bash
cd Expense-Tracker
Open index.html directly in any modern standard web browser (Chrome, Safari, Firefox, Edge, Brave), or run it via a local editor extension such as Live Server in VS Code.

📊 Core JavaScript Workflows
State Aggregation: Uses centralized state objects synchronized dynamically via utility mapping arrays:

JavaScript
let state = JSON.parse(localStorage.getItem('ledger_state') || 'null') || {
  salary: 0,
  expenses: []
};
Memory Management: Implements automated runtime component destruction (chart.destroy()) on active canvases prior to recreation loops, mitigating internal rendering overhead and ghost frames.

Security Sanitization: Uses dedicated regex character mapping to escape raw input strings (<, >, &, ", ') directly inside rendering pipes to defend against Cross-Site Scripting (XSS) injection attempts.

🛡️ License
This project was built as an academic evaluation assignment. Feel free to fork, modify, and optimize it for your own personal budgeting applications.
