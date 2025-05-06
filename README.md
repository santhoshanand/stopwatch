
# Stopwatch with records

A simple, single-file stopwatch web app built for the JCOM Kallakurichi 1.0 business meeting. It allows users to time speeches, log roster entries, and generate a color-coded report that can be exported as an image.

---

## 📑 Table of Contents

- [Features](#features)
- [Installation](#installation)
- [How to Use](#how-to-use)
- [Source Code Explanation](#source-code-explanation)
- [Technologies Used](#technologies-used)
- [License](#license)

---

## ✅ Features

- **Set Time Limit:** Configure a maximum time limit (in seconds) for speeches.
- **Stopwatch:** Start and stop a timer that shows time in seconds and hundredths of a second.
- **Roster Entry:** Input a roster number or speaker name during timing.
- **Report Generation:** Automatically logs the time and speaker info into a report table.
- **Color-Coded Report:**
  - 🟢 **Green** – Within or equal to time limit.
  - 🟡 **Yellow** – Exceeds time limit.
- **Export Report:** Save the report as a PNG image with a white background.

---

## ⚙️ Installation

This application is delivered as a **single HTML file**, requiring only a modern web browser.

1. **Obtain the Code:** Copy or clone the HTML file.
2. **Create a File:** Use a code editor (e.g., VS Code, Sublime, Notepad).
3. **Paste and Save:** Save the HTML code with a `.html` extension (e.g., `index.html`).
4. **Run It:** Open the file in any browser to start using the stopwatch.

*Tip:* To make it accessible from multiple devices or extend it as a PWA, host it using a simple web server (like `python -m http.server`).

---

## ▶️ How to Use

### 1. Set the Maximum Time Limit
- Enter the time in seconds under **"Set Time Limit (Seconds)"**.
- Click **"Confirm"** — the set limit will display.

### 2. Start Timing a Speech
- Click the **Start** button.
- A timer begins, and the roster input field appears.

### 3. Enter Roster Information
- Type the **speaker’s name or sheet number** while the timer is running.

### 4. Stop the Timer
- Click **Stop**.
- Timer halts and displays final time.
- The background color indicates if the speaker went over time.

### 5. Record to Report
- If roster info was provided, it logs the data in the report table.

### 6. Export the Report
- Click **"Export Report as Image"** to download a PNG of the report.

---

## 🧠 Source Code Explanation

### 📄 HTML Structure

- **Tailwind CSS** and **html2canvas** are included via CDN.
- Three major sections:
  1. **Time Limit Form**
  2. **Stopwatch Section**
  3. **Report Table**

### 🎨 CSS Styling

- Uses Tailwind utility classes.
- Custom CSS for:
  - Report table borders
  - Green/yellow text colors for times
  - `.hidden` class to show/hide elements

### 📜 JavaScript Logic

- DOM references via `getElementById` / `querySelector`
- State management with variables: `startTime`, `maxTimeLimit`, etc.
- **`formatTime(ms)`** – Formats milliseconds to `SS.ms`
- **`updateTimer()`** – Timer logic with background color updates
- Event listeners for start, stop, confirm, and export actions

---

## 🛠 Technologies Used

- **HTML5**
- **Tailwind CSS** (CDN)
- **JavaScript (Vanilla)**
- **html2canvas** (for exporting the report)

---

## 🪪 License

This project is licensed under the **GPL-3.0 license**.  
Feel free to use, modify, and share — just include the original license and credit.

