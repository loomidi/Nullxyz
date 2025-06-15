# 🌐 Dynamic HTML (DHTML) 3D/4D Geometry Visualization

A dynamic HTML project exploring the visualization of higher-dimensional geometric shapes (specifically a 3D Cube, with potential for a 4D Tesseract) using D3.js for rendering and `gl-matrix` for advanced mathematical transformations. This project demonstrates interactive web graphics purely in the browser.

## ✨ Features

* **Interactive 3D Cube:** A fully rotatable 3D cube rendered in SVG, controlled by sliders for X, Y, and Z axis rotations.
* **DHTML Powered:** Leverages the power of HTML, CSS, and JavaScript for a rich, interactive user experience directly in the browser.
* **Data-Driven Visualization (D3.js):** Utilizes D3.js for efficient data binding and rendering of vertices and edges to the SVG DOM.
* **Numerical Computing (`gl-matrix`):** Employs `gl-matrix` (a high-performance JavaScript library for vector/matrix math, similar to NumPy for linear algebra) to perform 3D/4D rotations and projections.
* **SVG Rendering:** Renders the geometric shapes using Scalable Vector Graphics, ensuring crisp, scalable visuals.
* **Potential for 4D Tesseract:** The architecture is designed to be extensible to a 4D hypercube (tesseract), incorporating 4D rotations and perspective projections into 3D space.
* **Canvas Integration (Planned/Alternative):** The project is structured to easily switch to or augment with HTML Canvas rendering for potentially higher performance with more complex scenes or pixel-level manipulation.

## 🚀 Getting Started

To run this project locally:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-project-name.git](https://github.com/your-username/your-project-name.git)
    cd your-project-name
    ```
2.  **Open `index.html`:** Simply open the `index.html` file in your web browser. There's no server required for the basic functionality.

## 💻 Code Structure

* `index.html`: The main HTML file that sets up the page, includes D3.js and `gl-matrix` from CDNs, and links to custom CSS and JavaScript.
* `css/style.css`: Contains the styling for the page and the SVG elements.
* `js/main.js` (or `cube.js`/`tesseract.js`): The core JavaScript logic for defining the geometric shape, performing transformations, handling user input, and rendering with D3.js.

## 📐 Mathematical Foundations

The visualization relies on:

* **Linear Algebra:** Representing vertices as vectors and transformations (rotations, projections) as matrices.
* **Matrix Multiplication:** Applying transformations to vertices by multiplying them with rotation and projection matrices.
* **Projection:** Transforming 3D (or 4D) coordinates onto a 2D plane for display. For the cube, this is typically an orthographic or simple perspective projection. For the tesseract, it involves a 4D-to-3D projection followed by a 3D-to-2D projection.

## 🌐 DHTMLX Integration (Future Consideration)

While the current visualization focuses on raw D3.js and `gl-matrix` for geometric rendering, `dhtmlx` is a comprehensive UI library. Should the project evolve to include more complex dashboard elements, data grids, charts (beyond pure D3.js), or other rich UI components, `dhtmlx` could be integrated for:

* **Layout Management:** Building sophisticated panel layouts to contain the SVG visualization alongside other controls or data displays.
* **Rich UI Controls:** Adding advanced buttons, forms, trees, or sidebars.
* **Data Handling:** If the geometric visualization were ever driven by larger datasets that need to be filtered or managed in a structured way.

*Note: The current version does not include DHTMLX. Its integration would be for expanding the broader UI/application context around the visualization.*

## 🎨 Canvas vs. SVG

The initial implementation uses **SVG** for rendering because:

* **Ease of Use with D3.js:** D3.js excels at manipulating SVG elements, making it straightforward to bind data to shapes.
* **Scalability:** SVG graphics are resolution-independent, meaning they look crisp at any zoom level.
* **DOM Access:** Each vertex and edge is a distinct DOM element, which can be useful for debugging or simple event handling.

For future enhancements or when dealing with a very large number of vertices/edges or pixel-level effects, transitioning to or augmenting with **HTML Canvas** rendering would be considered. Canvas provides:

* **Performance:** Generally faster for complex, constantly updating graphics as it's a pixel-based drawing surface.
* **Direct Pixel Control:** Ideal for shader-like effects or image processing.

## 🤝 Contributing

Feel free to fork this repository, open issues, or submit pull requests. Contributions are welcome!

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
