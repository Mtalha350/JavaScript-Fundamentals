# JavaScript Introduction Summary

## Writing JavaScript Code

- JavaScript code is typically written in a `.js` file and executed in the browser.
- To start, download the starter code from the provided GitHub repository.
- Click the **green button** > **Download ZIP** to get the files.
- If the button is not visible, check the FAQ section for an alternative download link.

## Extracting and Organizing Files

- After downloading, extract the ZIP file.
- The starter code includes folders for each section or project.
- Each folder contains a `final` and `starter` version:
  - `final`: The completed version of the project.
  - `starter`: The initial setup for each project.
- Use the `starter` folder as the project folder in VS Code.

## Setting Up in VS Code

- Open VS Code and select **Open Folder**.
- Navigate to the extracted `starter` folder and open it.
- Inside, you will find an `index.html` file where JavaScript is linked.

## Adding JavaScript to HTML

- JavaScript can be written inside an HTML file using a `<script>` tag.
- Example:
  ```html
  <script>
    let js = "amazing";
    alert("JavaScript is fun!");
  </script>
  ```
- JavaScript is usually attached to an HTML document for frontend applications.

## Executing JavaScript in the Browser

- Open `index.html` in the browser.
- The alert box should pop up with the message `JavaScript is fun!`.
- Reloading the page will execute the script again.

## Viewing JavaScript Output

- JavaScript output does not automatically appear in the console unless explicitly logged.
- Use `console.log()` to print output to the browser console:
  ```javascript
  console.log(40 + 8 + 23 - 10);
  ```
- Open the **Developer Console** (`Inspect > Console`) to view the output.

## Moving JavaScript to an External File

- Inline scripts (`<script>` in HTML) mix content and logic, which is not ideal.
- Create a separate `script.js` file:
  ```javascript
  let js = "amazing";
  alert("JavaScript is fun!");
  console.log(40 + 8 + 23 - 10);
  ```
- Link it in `index.html`:
  ```html
  <script src="script.js"></script>
  ```
- This approach keeps the code organized and maintainable.

## Conclusion

- JavaScript is essential for frontend web development.
- Using separate `.js` files ensures better project structure.
- The `console.log()` function helps debug and view output.
- Practice by writing, executing, and debugging JavaScript in the browser console.
