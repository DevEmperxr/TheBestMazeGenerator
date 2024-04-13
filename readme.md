## The Maze Generator

This JavaScript project is a maze generator and exporter built using Node.js. It allows users to create mazes of various sizes and export them to PDF files.

### Features:
- **Maze Generation**: Utilizes a depth-first search algorithm to generate mazes.
- **Export to PDF**: Offers the option to export mazes as PDF files using the PDFKit library.
- **Solution Path**: Includes functionality to find and visualize the solution path within generated mazes.

### How to Use:
1. **Clone the Repository**: Start by cloning this repository to your local machine using the following command:
```console
git clone https://github.com/yourusername/maze-generator.git
```
2. **Install Dependencies**: Navigate to the project directory and install the necessary dependencies using npm:
  ```javascript
  npm install
  ```
3. **Import the Module**: Require the `maze-generator` module in your Node.js script.
    ```javascript
    const Maze = require("./mazeGenerator")
    ```
4. **Create a Maze Instance**: Instantiate a `Maze` object with the desired dimensions and options.
    ```javascript
    const maze = new Maze(rows, columns, solve);
    ```
    - `rows`: Number of rows in the maze grid.
    - `columns`: Number of columns in the maze grid.
    - `solve` (optional): Boolean value indicating whether to generate a solution path (default: `false`).

5. **Export the Maze to PDF**: Use the `exportPDF()` method to export the maze as a PDF file.
      ```javascript
      maze.exportPDF(marginPercentage, strokeWidth, color);
      ```
      - `marginPercentage`: Percentage of the page margins.
      - `strokeWidth`: Stroke width of the maze walls.
      - `color`: Color of the maze walls.
6. **Explore Exported Files**: Check your directory for the exported maze files.
- View the PDF files using a PDF viewer or print them for physical copies.

## Example

```javascript
const Maze = require('./mazeGenerator');

// Create a 10x10 maze with solution path
const maze = new Maze(10, 10, true);

// Export the maze as a PDF with custom settings
maze.exportPDF(10, 1, '#000000');


### Dependencies:
- **fs**: File system module for Node.js.
- **pdfkit**: Library for generating PDFs in Node.js.

### License:
This project is licensed under the [MIT License](LICENSE).

### Contributing:
Contributions are welcome! If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.