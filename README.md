# Demonstration of Dynamic Vector Graphics and Transformation Pipelines

An interactive 2D shape transformation and rendering workbench built in C/C++ using the Borland Graphics Interface (`graphics.h`). Developed as an MSBTE K-Scheme Computer Graphics (CGR - 313001) micro-project.

---

## 🚀 Features
* **Interactive Configuration Menu:** Prompts the user at runtime to select a master shape, define scaling dimensions, and set a custom rotation speed multiplier.
* **Real-Time Matrix Transformation:** Utilizes polar-to-cartesian coordinate conversion and rotation matrix mathematics to render and animate shapes dynamically.
* **Custom Desktop UI Layout:** Renders a structured graphical workspace featuring an outer window border, a filled blue title banner, and central coordinate crosshair grid lines.
* **Event-Driven Controls:** Operates via a real-time rendering loop with controlled frame pacing (`delay`) and keyboard interrupt monitoring (`kbhit`).

---

## 🛠️ Tech Stack & Requirements
* **Programming Language:** C / C++
* **Graphics Library:** Borland Graphics Interface (`graphics.h`)
* **Environment / Compiler:** Turbo C++ IDE (Tested and compatible with web-based environments like [Online Turbo C++](https://sankalpsinghcoder-ai.github.io/online-c/)).

---

## 📐 Supported Shapes
1. **Equilateral Triangle ($n=3$):** Uniform angular vertex distribution.
2. **Rotating Square ($n=4$):** Uniform vertices with a 45-degree ($\pi/4$) diamond phase offset.
3. **Geometric Star ($n=5$):** Starburst index-linking pattern connecting non-adjacent vertices.

---

## ⚙️ How to Compile & Run
1. Clone or download this repository.
2. Open the source code (`code.cpp`) in **Turbo C++** or upload it to the [Online Turbo C++ Compiler](https://sankalpsinghcoder-ai.github.io/online-c/).
3. Ensure the BGI graphics path is correctly linked if running locally (`C:\TurboC3\BGI`).
4. Compile and run the program.
5. Follow the console text prompts to input your shape choice, size, and speed. Press any key while the graphics window is active to exit.

---

## 🧮 Mathematical Logic
The engine calculates vertex coordinates algorithmically on the fly using polar-to-cartesian mapping relative to screen center coordinates $(cx, cy)$:
* $\theta_i = \text{angle} + i \times \left(\frac{2\pi}{n}\right)$
* $x_i = cx + (\text{size} \times \cos(\theta_i))$
* $y_i = cy + (\text{size} \times \sin(\theta_i))$

---

## 📚 Academic Information
* **Course Name:** Computer Graphics (CGR)
* **Course Code:** 313001
* **Curriculum:** MSBTE K-Scheme Micro-Project
