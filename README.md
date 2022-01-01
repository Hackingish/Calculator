# 🧮 React Calculator Web App

A modern, responsive calculator web application built using **React.js**.
This project demonstrates clean UI design, state management using React hooks, and basic arithmetic logic implementation.

---

## 🚀 Features

* ✅ Perform basic arithmetic operations

  * Addition (+)
  * Subtraction (-)
  * Multiplication (×)
  * Division (÷)
  * Modulus (%)

* 🧠 Real-time input display

* ❌ Clear all input (AC)

* ⬅️ Delete last character (DEL)

* 🎯 Error handling for invalid expressions

* 💡 Responsive and clean UI design

* ✨ Smooth hover effects and button interactions

---

## 🛠️ Tech Stack

* **Frontend:** React.js
* **Styling:** CSS (Flexbox + Grid)
* **State Management:** React Hooks (`useState`)

---

## 📁 Project Structure

```
calculator-app/
│
├── src/
│   ├── App.jsx        # Main component (logic + UI)
│   ├── main.jsx       # React entry point
│   ├── index.css      # Global styles
│
└── package.json
```

---

## 🧠 How It Works

### 1. State Management

The calculator uses a single state variable:

```js
const [input, setInput] = useState("");
```

* Stores user input as a string (e.g., `"12+5*3"`)
* Updates dynamically on button clicks

---

### 2. Input Handling

```js
const handleClick = (value) => {
  setInput((prev) => prev + value);
};
```

* Appends numbers/operators to the current input

---

### 3. Clear & Delete

```js
const handleClear = () => setInput("");

const handleDelete = () => {
  setInput((prev) => prev.slice(0, -1));
};
```

* **AC** → resets input
* **DEL** → removes last character

---

### 4. Calculation Logic

```js
const handleCalc = () => {
  try {
    setInput(eval(input).toString());
  } catch {
    setInput("Error");
  }
};
```

* Evaluates the mathematical expression
* Handles invalid inputs safely using `try...catch`

> ⚠️ Note: `eval()` is used for simplicity. In production, a safer parser is recommended.

---

## 🎨 UI & Styling

* Built using **CSS Grid** for button layout
* Flexbox used for centering the calculator
* Smooth hover animations with scaling effects
* Color-coded buttons:

  * 🔵 Controls (AC, DEL)
  * 🟠 Operators
  * 🔴 Equals
  * 🟢 Numbers

---

## 📸 Preview

A clean and minimal calculator interface with modern UI styling and responsive layout.

---

## ⚡ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/react-calculator.git
cd react-calculator
```

---

### 2. Install dependencies

```bash
npm install
```

---

### 3. Run the app

```bash
npm run dev
```

---

## 🧩 Future Improvements

* 🔐 Replace `eval()` with a custom expression parser
* ⌨️ Add keyboard input support
* 📜 Add calculation history
* 🌙 Dark/Light theme toggle
* 📱 Improve mobile responsiveness

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository and submit a pull request.

---

## 🙌 Acknowledgements

Built as part of learning React fundamentals and UI development.

---
