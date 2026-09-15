

A modernized, responsive web calculator application refactored and enhanced from an open-source vanilla JavaScript project for the Pre-Open Source Formative Assessment.

---

## 📌 Project Overview

* **Course:** Pre-Open Source Formative Assessment
* **Submitted By:** Yuvaraj P
* **Tech Stack:** HTML5, CSS3, JavaScript, Git & GitHub

---

## 🎨 Semantic Color & Electric Theme System

| Role / Element | Hex Code | Visual Badge |
| :--- | :--- | :--- |
| **Canvas Background** | `#0f172a` | ![](https://img.shields.io/badge/Slate_900-0f172a?style=for-the-badge&logoColor=white) |
| **Container Surface** | `#1e293b` | ![](https://img.shields.io/badge/Slate_800-1e293b?style=for-the-badge&logoColor=white) |
| **Display Accent** | `#38bdf8` | ![](https://img.shields.io/badge/Electric_Cyan-38bdf8?style=for-the-badge&logoColor=black) |
| **Arithmetic Operators** | `#ea580c` | ![](https://img.shields.io/badge/Warning_Orange-ea580c?style=for-the-badge&logoColor=white) |
| **Action Keys (AC / DEL)** | `#dc2626` | ![](https://img.shields.io/badge/Danger_Red-dc2626?style=for-the-badge&logoColor=white) |
| **Compute Action (=)** | `#16a34a` | ![]([https://img.shields.io/badge/Success_Green-16a34a?style=for-the-badge&logoColor=white](https://img.shields.io/badge/Success_Green-16a34a?style=for-the-badge&logoColor=white)) |

---

## ⚡ System Architecture & Execution Flow

* **Key Click Event:** Intercepts user touch or click on keypad buttons.
* **Key Classification:**
  * **Digits & Decimals:** Appended directly to screen display buffer.
  * **Operators (+, -, *, /):** Buffered as active mathematical tokens.
  * **DEL Action:** Triggers atomic backspace via JavaScript `slice(0, -1)`.
  * **AC Action:** Resets screen display buffer to blank.
  * **Equal (=):** Evaluates mathematical expression via `eval()` and prints result.

---

## 🚀 Key Modifications Overview

| Feature | Original Implementation | Enhanced Implementation |
| :--- | :--- | :--- |
| **User Interface** | Basic light gray styling | High-contrast modern dark palette |
| **Backspace Feature** | Missing (Complete reset only) | Single-character rollback using slice() |
| **Clear Controls** | Single C key | Distinct AC (All Clear) and DEL (Delete) |
| **Keypad Grid** | Standard uniform grid | Visual priority layout with double-width = key |

---

## 🛠️ Feature Implementation Details

### 1. Atomic Backspace Feature (JavaScript)

The original code lacked the ability to remove a single mis-typed character. Added `delChar()` using JavaScript string slicing:

```javascript
function delChar() {
  screen.value = screen.value.slice(0, -1);
}

2. High-Contrast Styles (CSS)
Added modern styling tokens and semantic classes for interactive user feedback:
button.op { 
  background-color: #ea580c; /* Operator keys */
}

button.action { 
  background-color: #dc2626; /* Reset and backspace keys */
}

button.equal { 
  background-color: #16a34a; /* Execute result key */
  grid-column: span 2; 
}

📂 Project Structure
pro-calculator-modified/
│
├── index.html       # Combined structure, styles, and logic
└── README.md        # Technical documentation and project specification

💻 How to Run Locally
Step 1: Clone the Repository
Clone this repository using Git:
git clone https://github.com/YOUR_GITHUB_USERNAME/pro-calculator-modified.git

Step 2: Open Project Folder
Navigate into the downloaded folder:
cd pro-calculator-modified

Step 3: Launch in Browser
 * Double-click index.html to open it in your default browser.
 * Or right-click index.html and choose Open With -> Google Chrome.
