# MWAD-EXP_04-Simple-caluculator
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
Calculator.jsx
```
import React, { useState } from "react";

export default function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    if (value === "C") {
      setInput("");
    } else if (value === "=") {
      try {
        // eslint-disable-next-line no-eval
        const result = eval(input);
        setInput(result.toString());
      } catch (error) {
        setInput("Error");
      }
    } else {
      setInput(input + value);
    }
  };

  // Inline CSS styles
  const styles = {
    calculator: {
      width: "280px",
      margin: "100px auto",
      padding: "20px",
      backgroundColor: "#1e1e1e",
      borderRadius: "15px",
      boxShadow: "0px 0px 15px rgba(0,0,0,0.5)",
      textAlign: "center",
    },
    display: {
      width: "100%",
      height: "50px",
      fontSize: "24px",
      textAlign: "right",
      marginBottom: "15px",
      border: "none",
      borderRadius: "8px",
      padding: "5px 10px",
      backgroundColor: "#333",
      color: "white",
    },
    buttons: {
      display: "grid",
      gridTemplateColumns: "repeat(4, 1fr)",
      gap: "10px",
    },
    button: {
      padding: "15px",
      fontSize: "18px",
      borderRadius: "8px",
      border: "none",
      backgroundColor: "#61dafb",
      cursor: "pointer",
      transition: "0.2s",
    },
    operator: {
      backgroundColor: "#ffb74d",
      color: "black",
    },
    clear: {
      gridColumn: "span 4",
      backgroundColor: "#f44336",
      color: "white",
    },
    equal: {
      backgroundColor: "#81c784",
      color: "black",
    },
  };

  return (
    <div style={styles.calculator}>
      <input type="text" value={input} readOnly style={styles.display} />
      <div style={styles.buttons}>
        {/* Row 1 */}
        <button style={{ ...styles.button }} onClick={() => handleClick("7")}>7</button>
        <button style={{ ...styles.button }} onClick={() => handleClick("8")}>8</button>
        <button style={{ ...styles.button }} onClick={() => handleClick("9")}>9</button>
        <button style={{ ...styles.button, ...styles.operator }} onClick={() => handleClick("/")}>÷</button>

        {/* Row 2 */}
        <button style={{ ...styles.button }} onClick={() => handleClick("4")}>4</button>
        <button style={{ ...styles.button }} onClick={() => handleClick("5")}>5</button>
        <button style={{ ...styles.button }} onClick={() => handleClick("6")}>6</button>
        <button style={{ ...styles.button, ...styles.operator }} onClick={() => handleClick("*")}>×</button>

        {/* Row 3 */}
        <button style={{ ...styles.button }} onClick={() => handleClick("1")}>1</button>
        <button style={{ ...styles.button }} onClick={() => handleClick("2")}>2</button>
        <button style={{ ...styles.button }} onClick={() => handleClick("3")}>3</button>
        <button style={{ ...styles.button, ...styles.operator }} onClick={() => handleClick("-")}>−</button>

        {/* Row 4 */}
        <button style={{ ...styles.button }} onClick={() => handleClick("0")}>0</button>
        <button style={{ ...styles.button }} onClick={() => handleClick(".")}>.</button>
        <button style={{ ...styles.button, ...styles.equal }} onClick={() => handleClick("=")}>=</button>
        <button style={{ ...styles.button, ...styles.operator }} onClick={() => handleClick("+")}>+</button>

        {/* Clear Button */}
        <button style={{ ...styles.button, ...styles.clear }} onClick={() => handleClick("C")}>C</button>
      </div>
    </div>
  );
}
```
App.jsx
```
import Calculator from "./Calculator"

function App() {
  return (
    <div className="App">
      <h1>Simple Calculator</h1>
      <Calculator />
    </div>
  );
}

export default App;
```


## OUTPUT
<img width="1918" height="1035" alt="image" src="https://github.com/user-attachments/assets/ade99699-fbe8-44c9-a354-25b90017b951" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
