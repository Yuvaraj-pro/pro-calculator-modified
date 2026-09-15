# Pro Calculator — Open Source Customization

A modernized, responsive web calculator application refactored and enhanced from an open-source vanilla JavaScript project.

---

## 📌 Project Overview
* **Author:** Yuvaraj P
* **Tech Stack:** HTML5, CSS3, JavaScript, Git & GitHub

---

## 🚀 Key Modifications & Enhancements

| Feature | Original Code | Modified Enhanced Code |
| :--- | :--- | :--- |
| **Theme / UI** | Basic light theme with plain buttons | Modern Slate Dark Theme (`#0f172a` / `#1e293b`) |
| **Backspace Feature** | Missing (Full clear `C` only) | Added `DEL` button with atomic backspace logic |
| **Clear Logic** | Single clear action | Distinct `AC` (All Clear) and `DEL` (Single Clear) |
| **Keypad Grid** | Generic 4x4 matrix | Ergonomic keypad with a highlighted double-span `=` button |
| **Visual Hierarchy** | Uniform gray buttons | Semantic color-coded keys (Action, Operator, Equals) |

---

## 🛠️ Code Implementation Details

### 1. Atomic Backspace Feature (JavaScript)
The original code lacked single-digit deletion. Implemented `delChar()` utilizing JavaScript string slicing:

```javascript
function delChar() {
  screen.value = screen.value.slice(0, -1);
}

