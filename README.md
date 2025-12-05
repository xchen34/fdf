# 🎯 Project Overview

The Fdf project involves reading elevation data from a file and transforming this 3D data into a 2D projection on the screen, creating a **wireframe model** of the terrain. This exercise emphasizes **data parsing**, **memory management**, and applying **basic linear algebra** for graphical rendering.

<img width="1341" height="818" alt="fdf" src="https://github.com/user-attachments/assets/f450707f-9b01-4fd4-a4fb-756b0f663c57" />


## 📄 Input File Format

The program takes a simple `.fdf` file as input, where numbers represent the elevation (Z-coordinate) at a specific (X, Y) grid point.

**Example `42.fdf`:**
```
0 0 0 5 0 1 2 0 0 0 0 0
```

## ✨ Mandatory Implemented Features

1. **Map Parsing:** Robust reading and error checking of the input `.fdf` file, handling maps of any size and dimensions.
2. **Display:** Renders the map as a 3D wireframe using lines drawn via the **miniLibX** library.
3. **Isometric Projection:** The default view must use an **isometric or dimetric projection** to simulate 3D depth.
4. **Movement & Control:** The user must be able to:
   - **Translate:** Move the entire visualization horizontally and vertically.
   - **Zoom:** Increase and decrease the scale of the model.
   - **Exit:** Close the window cleanly (e.g., using the ESC key or the red cross button).
5. **Clean Code:** Adherence to 42 Norms and strict **memory leak prevention**.

## 💻 Technical Details

- **Coordinate Transformation:** The core challenge involves implementing the mathematical formula to convert 3D Cartesian coordinates (X, Y, Z) into 2D screen coordinates (x', y').
- **miniLibX:** Utilizes miniLibX for drawing pixels, managing the window, and handling keyboard events.

## 🛠️ How to Run

1. **Compilation:**
   ```bash
   make
   ```

2. **Execution:**
   ```bash
   ./fdf <path/to/map_file.fdf>
   ```
   **Example:** 
   ```bash
   ./fdf maps/42.fdf
   ```

---
