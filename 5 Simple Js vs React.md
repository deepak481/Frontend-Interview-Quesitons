### Interface Creation

- **Vanilla JavaScript:**
  - Interface is created on the HTML server.
  - HTML is sent directly to the server with no JavaScript needed.

- **React:**
  - Uses a fixed HTML file with a blank container (`<div id="root"></div>`).
  - UI is defined in the browser using JSX and components.
  - Components are mounted into the container via ReactDOM.

### Separation of Concerns and Splitting Functionality in React

- **Vanilla JavaScript:**
  - No strict requirements for splitting functionality.
  - HTML (markup) and JavaScript (functionality) are separate.
  - Code that updates HTML can be scattered across multiple JS files.
  - Leads to complex and hard-to-track codebases.

- **React:**
  - App is split into components.
  - Each component contains both display and update code.
  - Keeps related code together, making complex apps easier to understand.

### Data Storage

- **Vanilla JavaScript:**
  - Data is stored in the DOM.
  - Developers manually extract data from DOM nodes (e.g., form inputs).
  - Can be tedious and error-prone.

- **React:**
  - Uses controlled components to store data in JavaScript objects.
  - Example: `const [input, setInput] = useState("")` for managing input state.
  - Makes data handling easier and more dynamic.
  - Allows easy data passing to other UI elements.

### UI Updates

- **Vanilla JavaScript:**
  - Requires manual DOM manipulation for updates.
  - Example: Adding an item to a list requires finding the DOM element and appending the new item.

- **React:**
  - Keeps the state in JavaScript variables.
  - Uses functions like `setItems` to update the state.
  - Automatically updates the UI when state changes.
  - Simplifies code by abstracting DOM manipulation.

### Example Comparison

**Vanilla JavaScript:**

```javascript
let items = [];
function addItem() {
  const newItem = document.createElement('li');
  newItem.textContent = 'New Item';
  document.getElementById('list').appendChild(newItem);
}
```

**React:**

```javascript
function App() {
  const [items, setItems] = useState([]);
  const addItem = () => setItems([...items, 'New Item']);

  return (
    <div>
      <ul>
        {items.map((item, index) => (
          <li key={index}>{item}</li>
        ))}
      </ul>
      <button onClick={addItem}>Add Item</button>
    </div>
  );
}
```

### Summary

- **Vanilla JavaScript:**
  - Creates UI on the server.
  - Requires manual DOM manipulation and separation of HTML and JavaScript.
  - Stores data in the DOM, making updates cumbersome.

- **React:**
  - Defines UI in the browser with JSX.
  - Splits functionality into components, keeping code organized.
  - Uses controlled components for easier data management.
  - Simplifies UI updates with state management, avoiding manual DOM manipulation.