### React

- **Use:** To manipulate the DOM.
- **React DOM:** Used for DOM manipulation in web applications.
- **React Native:** Implementation of React for mobile applications.
- **DOM:** Tree structure of elements and tags.

### Virtual DOM
- **Website DOM:** Known as Main DOM.
- **React Virtual DOM:** React creates its own DOM to improve performance.

### JSX
- Provides programming capabilities within HTML.
- Transformed into React.createElement calls.

### react-scripts
- Injects React.js into the HTML file (`index.html`).

### Vite
- Loads JS directly using script tags.
- **Restrictions in Vite:**
  - Component names must start with a capital letter.
  - File extensions must be `.jsx`.

### Best Practices
- **File Naming:**
  - Capitalize file names.
  - Use `.jsx` for files returning JSX, otherwise use `.js`.

### How React Works
1. **JSX Code:** Written in React components.
2. **Transformation:** JSX is transformed into `React.createElement()` calls by Babel.
   ```jsx
   <div>Hello World</div>
   // Transforms to:
   React.createElement('div', null, "Hello World")
   ```
3. **React.createElement:** Produces an object.
   ```javascript
   {
     "type": "div",
     "props": {
       "children": "Hello World"
     },
     "key": null,
     "ref": null
   }
   ```
4. **Rendering:** The object is handled by React's render function, updating the virtual DOM.
5. **Diffing:** Differences between the virtual DOM and the real DOM are calculated.
6. **Update Real DOM:** Efficiently updates the real DOM.

### JSX Limitations
- **If-Else Statements:** Cannot be used directly within JSX.
  ```javascript
  var a = 10;
  <div>Hello World {a}</div>
  // a must be evaluated before rendering
  ```
- **Reason:** React.createElement does not accept if-else statements.

### The Role of Babel
- **Compiler:** Not exclusive to React.
- **Purpose:** Converts ECMAScript code into backward-compatible JavaScript.
- **Function:** Transforms JSX to JavaScript code.
- **Benefit:** Ensures code compatibility across different browsers.