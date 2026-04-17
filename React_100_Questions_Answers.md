# React: 100+ Questions and Answers

## 1. REACT INTRODUCTION AND INSTALLATION

### Q1: What is React?
**A:** React is a JavaScript library developed by Facebook for building user interfaces with reusable components. It uses a virtual DOM to efficiently update the UI and follows a component-based architecture.

### Q2: Why use React?
**A:** 
- Improves application performance (Virtual DOM)
- Easy to learn and use
- Reusable components
- Strong community support
- SEO friendly
- One-way data binding
- Can be used with other libraries

### Q3: What are the prerequisites for installing React?
**A:**
- Knowledge of JavaScript (ES6+)
- Understanding of HTML and CSS
- Node.js installed on your system
- npm (Node Package Manager) or yarn
- A code editor (VS Code, etc.)

### Q4: What is Node.js?
**A:** Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine. It allows you to run JavaScript outside the browser and is essential for installing and managing React packages.

### Q5: What is npm?
**A:** npm (Node Package Manager) is the default package manager for Node.js. It is used to install, manage, and share JavaScript packages. It comes with Node.js.

### Q6: How do you install Node.js?
**A:** 
- Visit nodejs.org
- Download the LTS (Long Term Support) version
- Run the installer
- Verify installation: `node --version` and `npm --version`

### Q7: How do you create a React application?
**A:** Using Create React App:
```bash
npx create-react-app my-app
cd my-app
npm start
```

### Q8: What is Create React App?
**A:** Create React App is a tool by Facebook that sets up a new React project with a good default configuration. It handles build configuration, manages dependencies, and provides a development server.

### Q9: What are the folders in a React project?
**A:**
- **node_modules**: Contains all installed packages
- **public**: Static files (index.html, favicon)
- **src**: Source code (components, CSS, JS)
- **.gitignore**: Files to ignore in git
- **package.json**: Project metadata and dependencies
- **package-lock.json**: Lock file for exact versions

### Q10: What is index.js in React?
**A:** Index.js is the entry point of a React application. It renders the root component (App) into the root DOM element (div#root) in index.html.

### Q11: What is the purpose of public folder?
**A:** The public folder contains static files that don't go through webpack. It includes index.html, favicon.ico, and manifest.json.

### Q12: What is the purpose of src folder?
**A:** The src folder contains all your React components, CSS files, images, and other source code that will be processed by webpack.

### Q13: How do you run a React application?
**A:** Use the command:
```bash
npm start
```
This starts the development server at http://localhost:3000

### Q14: How do you build a React application for production?
**A:** Use the command:
```bash
npm run build
```
This creates an optimized production build in the `build` folder.

### Q15: What is the difference between development and production builds?
**A:**
- **Development**: Larger file size, includes source maps, fast compilation, better error messages
- **Production**: Smaller file size (minified), optimized, no source maps, faster execution

---

## 2. REACT ES6 (ECMAScript 2015)

### Q16: What is ES6?
**A:** ES6 (ECMAScript 2015) is a major update to JavaScript that introduced many new features and syntax improvements. It's the standard for modern JavaScript development.

### Q17: What are the key features of ES6?
**A:**
- Let and const declarations
- Arrow functions
- Template literals
- Classes
- Destructuring
- Default parameters
- Spread operator
- Promises
- Modules (import/export)

### Q18: What is the difference between var, let, and const?
**A:**
| Feature | var | let | const |
|---------|-----|-----|-------|
| Scope | Function | Block | Block |
| Reassign | Yes | Yes | No |
| Redeclare | Yes | No | No |
| Hoisting | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |
| Initial Value | Optional | Optional | Required |

### Q19: What are arrow functions?
**A:** Arrow functions are a concise way to write functions introduced in ES6:
```javascript
// Traditional function
function add(a, b) {
  return a + b;
}

// Arrow function
const add = (a, b) => a + b;
```

### Q20: What are the advantages of arrow functions?
**A:**
- More concise syntax
- Implicit return (if single expression)
- No binding of `this` (lexical this)
- Cannot be used as constructors
- No `arguments` object

### Q21: What are template literals?
**A:** Template literals use backticks to create strings with interpolation:
```javascript
const name = "John";
const age = 25;
const message = `My name is ${name} and I am ${age} years old`;
```

### Q22: What is destructuring?
**A:** Destructuring allows you to extract values from objects or arrays and assign them to variables:
```javascript
// Array destructuring
const [a, b] = [1, 2];

// Object destructuring
const { name, age } = { name: "John", age: 25 };
```

### Q23: What are default parameters?
**A:** Default parameters provide default values for function parameters:
```javascript
const greet = (name = "Guest") => {
  console.log(`Hello, ${name}`);
};
greet(); // Hello, Guest
```

### Q24: What is the spread operator?
**A:** The spread operator (...) expands iterable objects:
```javascript
// Array
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]

// Object
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 }; // { a: 1, b: 2, c: 3 }
```

### Q25: What are rest parameters?
**A:** Rest parameters (...) collect remaining arguments into an array:
```javascript
const sum = (...nums) => {
  return nums.reduce((a, b) => a + b, 0);
};
sum(1, 2, 3, 4); // 10
```

### Q26: What are ES6 classes?
**A:** Classes provide a cleaner syntax for creating objects:
```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
  
  greet() {
    console.log(`Hello, I'm ${this.name}`);
  }
}
```

### Q27: What is inheritance in ES6 classes?
**A:** Inheritance is achieved using the `extends` keyword:
```javascript
class Student extends Person {
  constructor(name, grade) {
    super(name);
    this.grade = grade;
  }
}
```

### Q28: What is the super keyword?
**A:** The `super` keyword calls the parent class constructor and methods:
```javascript
super(name); // Call parent constructor
super.greet(); // Call parent method
```

### Q29: What are modules in ES6?
**A:** Modules allow you to organize code into separate files and reuse them. They use `import` and `export`:
```javascript
// export.js
export const myFunction = () => {};

// import.js
import { myFunction } from './export.js';
```

### Q30: What is the difference between named and default exports?
**A:**
```javascript
// Named export
export const func1 = () => {};
export const func2 = () => {};
import { func1, func2 } from './file';

// Default export
export default function() {}
import anyName from './file';
```

---

## 3. REACT JSX

### Q31: What is JSX?
**A:** JSX (JavaScript XML) allows you to write HTML-like code in JavaScript. It gets transpiled to JavaScript function calls by Babel.

### Q32: How does JSX work?
**A:** 
```javascript
// JSX
const element = <h1>Hello, World!</h1>;

// Transpiled to
const element = React.createElement('h1', null, 'Hello, World!');
```

### Q33: Why is JSX used in React?
**A:**
- Looks similar to HTML, making code more readable
- Easier to understand component structure
- Can embed JavaScript expressions
- Better performance (optimized by React)
- Type checking available

### Q34: Can you use HTML directly in React?
**A:** No, you must use JSX. JSX is syntactic sugar for React.createElement() calls.

### Q35: What are JSX expressions?
**A:** JSX expressions allow you to embed JavaScript inside JSX:
```javascript
const name = "John";
const element = <h1>Hello, {name}</h1>;
const age = <p>Age: {25 + 5}</p>;
```

### Q36: Can you use if-else statements in JSX?
**A:** No, you cannot use if-else directly in JSX. Use ternary operators or logical operators:
```javascript
// Ternary operator
{age > 18 ? <p>Adult</p> : <p>Minor</p>}

// Logical operator
{isLoggedIn && <Dashboard />}
```

### Q37: How do you add CSS classes in JSX?
**A:**
```javascript
// Using className (not class)
<div className="container">Content</div>

// Dynamic classes
<div className={isActive ? "active" : ""}>Content</div>
```

### Q38: Why use className instead of class in JSX?
**A:** `class` is a reserved keyword in JavaScript, so React uses `className` instead.

### Q39: How do you add inline styles in JSX?
**A:** Inline styles are JavaScript objects:
```javascript
const styles = {
  color: "red",
  fontSize: "20px",
  backgroundColor: "blue"
};
<div style={styles}>Styled content</div>
```

### Q40: How do you add comments in JSX?
**A:**
```javascript
// Inside JSX elements
<div>
  {/* This is a comment */}
  <p>Content</p>
</div>

// Outside JSX
// Regular JavaScript comment
```

### Q41: What are JSX attributes?
**A:** JSX attributes are similar to HTML attributes:
```javascript
<img src="image.jpg" alt="Description" />
<input type="text" placeholder="Enter name" />
```

### Q42: How do you pass multiple attributes?
**A:**
```javascript
const props = {
  type: "text",
  placeholder: "Enter name",
  className: "input-field"
};
<input {...props} />
```

### Q43: What are children in JSX?
**A:** Children are content passed between opening and closing tags:
```javascript
<div>
  <p>This is a child</p>
  <span>Another child</span>
</div>
```

### Q44: How do you access children in a component?
**A:**
```javascript
function MyComponent(props) {
  return <div>{props.children}</div>;
}
```

### Q45: What is the difference between JSX and HTML?
**A:**
| JSX | HTML |
|-----|------|
| Uses camelCase attributes | Uses lowercase attributes |
| className instead of class | class attribute |
| Inline styles are objects | Inline styles are strings |
| Can contain JavaScript expressions | Cannot contain JavaScript |
| Requires closing tags | Some tags don't require closing |
| Can be conditional | Static |

---

## 4. REACT ES6 FUNDAMENTAL / COMPONENTS

### Q46: What are React components?
**A:** Components are reusable pieces of UI. They can be functional or class-based and return JSX.

### Q47: What is a functional component?
**A:** A functional component is a JavaScript function that returns JSX:
```javascript
function Greeting() {
  return <h1>Hello, World!</h1>;
}
```

### Q48: What is a class component?
**A:** A class component extends React.Component and uses a render method:
```javascript
class Greeting extends React.Component {
  render() {
    return <h1>Hello, World!</h1>;
  }
}
```

### Q49: What are props?
**A:** Props (properties) are read-only data passed from parent to child component:
```javascript
// Parent
<Greeting name="John" />

// Child
function Greeting(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

### Q50: What are the characteristics of props?
**A:**
- Read-only (immutable)
- Passed from parent to child
- Used to configure components
- Cannot be modified by child component

### Q51: How do you use props in a class component?
**A:**
```javascript
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

### Q52: What is prop drilling?
**A:** Prop drilling is passing props through intermediate components that don't need them, just to pass them down to a child component.

### Q53: How do you avoid prop drilling?
**A:** Use Context API or state management libraries like Redux.

### Q54: What is state in React?
**A:** State is mutable data that belongs to a component. When state changes, the component re-renders:
```javascript
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }
  
  render() {
    return <p>{this.state.count}</p>;
  }
}
```

### Q55: What is the difference between state and props?
**A:**
| State | Props |
|-------|-------|
| Mutable | Immutable |
| Managed within component | Passed from parent |
| Can be changed | Cannot be changed |
| Used for dynamic data | Used for configuration |
| Causes re-render when changed | Component re-renders when parent re-renders |

### Q56: How do you update state in a class component?
**A:** Use the `setState()` method:
```javascript
this.setState({ count: this.state.count + 1 });
```

### Q57: Is setState synchronous or asynchronous?
**A:** setState is asynchronous. Multiple setState calls are batched together.

### Q58: What is the virtual DOM?
**A:** The virtual DOM is a lightweight JavaScript representation of the real DOM. React uses it to determine which elements have changed and updates only those elements.

### Q59: How does the virtual DOM improve performance?
**A:**
- Batches updates
- Calculates differences (diffing)
- Updates only changed elements
- Reduces direct DOM manipulation

### Q60: What is reconciliation?
**A:** Reconciliation is the process by which React updates the DOM. It compares the virtual DOM with the actual DOM and updates only the changed parts.

### Q61: What are controlled components?
**A:** Controlled components are form elements whose values are controlled by React state:
```javascript
function NameInput() {
  const [name, setName] = useState('');
  
  return (
    <input 
      value={name} 
      onChange={(e) => setName(e.target.value)} 
    />
  );
}
```

### Q62: What are uncontrolled components?
**A:** Uncontrolled components are form elements that manage their own state:
```javascript
function NameInput() {
  const inputRef = useRef();
  
  const handleSubmit = () => {
    console.log(inputRef.current.value);
  };
  
  return <input ref={inputRef} />;
}
```

### Q63: What is the key prop in React?
**A:** The key prop helps React identify which elements have changed. It's used in lists:
```javascript
<ul>
  {items.map((item) => (
    <li key={item.id}>{item.name}</li>
  ))}
</ul>
```

### Q64: Why is the key prop important?
**A:**
- Helps React match old elements with new ones
- Improves performance
- Preserves component state in lists
- Prevents bugs in dynamic lists

### Q65: What happens if you use index as a key?
**A:** Using index as a key can cause issues when the list is reordered, filtered, or has items added/removed, as the index changes.

---

## 5. REACT HOOKS

### Q66: What are hooks?
**A:** Hooks are functions that allow you to use state and other React features in functional components. They were introduced in React 16.8.

### Q67: What is useState?
**A:** useState is a hook that adds state to functional components:
```javascript
const [count, setCount] = useState(0);
```

### Q68: What is useEffect?
**A:** useEffect is a hook that runs side effects (data fetching, subscriptions, etc.):
```javascript
useEffect(() => {
  // Side effect code
  return () => {
    // Cleanup code
  };
}, [dependencies]);
```

### Q69: What is the dependency array in useEffect?
**A:** The dependency array specifies when the effect should run:
- Empty array: runs once after render
- With dependencies: runs when dependencies change
- No array: runs after every render

### Q70: What is useContext?
**A:** useContext allows you to consume context values in functional components:
```javascript
const value = useContext(MyContext);
```

### Q71: What is useReducer?
**A:** useReducer is a hook for managing complex state logic:
```javascript
const [state, dispatch] = useReducer(reducer, initialState);
```

### Q72: What is useRef?
**A:** useRef creates a mutable reference that persists across renders:
```javascript
const inputRef = useRef();
inputRef.current.focus();
```

### Q73: What is useMemo?
**A:** useMemo memoizes a value and recomputes it only when dependencies change:
```javascript
const memoizedValue = useMemo(() => expensiveCalculation(), [dependencies]);
```

### Q74: What is useCallback?
**A:** useCallback memoizes a function and returns the same function reference:
```javascript
const memoizedCallback = useCallback(() => {
  doSomething();
}, [dependencies]);
```

### Q75: What is the difference between useEffect and componentDidMount?
**A:**
- useEffect: Runs after render, can run multiple times
- componentDidMount: Runs once after component mounts

---

## 6. FORM HANDLING IN REACT

### Q76: How do you create a form in React?
**A:**
```javascript
function MyForm() {
  const [name, setName] = useState('');
  
  const handleSubmit = (e) => {
    e.preventDefault();
    console.log(name);
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <input 
        value={name} 
        onChange={(e) => setName(e.target.value)} 
      />
      <button type="submit">Submit</button>
    </form>
  );
}
```

### Q77: How do you handle form submission?
**A:**
```javascript
const handleSubmit = (e) => {
  e.preventDefault(); // Prevent default form submission
  // Process form data
};
```

### Q78: How do you handle text input?
**A:**
```javascript
const [text, setText] = useState('');
<input value={text} onChange={(e) => setText(e.target.value)} />
```

### Q79: How do you handle textarea?
**A:**
```javascript
const [message, setMessage] = useState('');
<textarea value={message} onChange={(e) => setMessage(e.target.value)} />
```

### Q80: How do you handle select dropdown?
**A:**
```javascript
const [selected, setSelected] = useState('');
<select value={selected} onChange={(e) => setSelected(e.target.value)}>
  <option value="option1">Option 1</option>
  <option value="option2">Option 2</option>
</select>
```

### Q81: How do you handle checkboxes?
**A:**
```javascript
const [checked, setChecked] = useState(false);
<input 
  type="checkbox" 
  checked={checked} 
  onChange={(e) => setChecked(e.target.checked)} 
/>
```

### Q82: How do you handle multiple checkboxes?
**A:**
```javascript
const [selected, setSelected] = useState([]);

const handleChange = (value) => {
  setSelected(prev => 
    prev.includes(value) 
      ? prev.filter(item => item !== value)
      : [...prev, value]
  );
};
```

### Q83: How do you handle radio buttons?
**A:**
```javascript
const [selected, setSelected] = useState('');
<input 
  type="radio" 
  value="option1" 
  checked={selected === 'option1'}
  onChange={(e) => setSelected(e.target.value)}
/>
```

### Q84: How do you validate a form?
**A:**
```javascript
const validateForm = (data) => {
  const errors = {};
  if (!data.name) errors.name = "Name is required";
  if (!data.email) errors.email = "Email is required";
  return errors;
};
```

### Q85: How do you display form errors?
**A:**
```javascript
{errors.name && <p className="error">{errors.name}</p>}
```

### Q86: How do you handle file input?
**A:**
```javascript
const [file, setFile] = useState(null);
<input 
  type="file" 
  onChange={(e) => setFile(e.target.files[0])} 
/>
```

### Q87: How do you submit form data to a server?
**A:**
```javascript
const handleSubmit = async (e) => {
  e.preventDefault();
  const response = await fetch('/api/submit', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(formData)
  });
};
```

### Q88: What is form validation?
**A:** Form validation checks if user input is correct before submission. It can be client-side or server-side.

### Q89: What are the types of form validation?
**A:**
- Required field validation
- Email validation
- Number validation
- Pattern matching
- Custom validation

### Q90: How do you create a reusable form component?
**A:**
```javascript
function FormInput({ label, value, onChange, error }) {
  return (
    <div>
      <label>{label}</label>
      <input value={value} onChange={onChange} />
      {error && <p className="error">{error}</p>}
    </div>
  );
}
```

---

## 7. REACT LIFECYCLE & ADVANCED CONCEPTS

### Q91: What is the component lifecycle?
**A:** The lifecycle has three phases: mounting, updating, and unmounting.

### Q92: What are lifecycle methods in class components?
**A:**
- **Mounting**: constructor, render, componentDidMount
- **Updating**: render, componentDidUpdate
- **Unmounting**: componentWillUnmount

### Q93: What is componentDidMount?
**A:** Runs after component is mounted. Used for API calls and subscriptions:
```javascript
componentDidMount() {
  // Fetch data
}
```

### Q94: What is componentDidUpdate?
**A:** Runs after component updates. Used when state or props change:
```javascript
componentDidUpdate(prevProps, prevState) {
  // Check if props changed
}
```

### Q95: What is componentWillUnmount?
**A:** Runs before component is removed. Used for cleanup:
```javascript
componentWillUnmount() {
  // Cleanup subscriptions
}
```

### Q96: What is Context API?
**A:** Context API provides a way to pass data through the component tree without prop drilling:
```javascript
const MyContext = React.createContext();
<MyContext.Provider value={data}>
  <Component />
</MyContext.Provider>
```

### Q97: How do you use Context API?
**A:**
1. Create context: `const MyContext = React.createContext()`
2. Create provider component
3. Use useContext in child components

### Q98: What is the difference between local state and Redux?
**A:**
- Local state: Managed within component
- Redux: Global state management across all components

### Q99: What are higher-order components?
**A:** HOC is a function that takes a component and returns a new component with additional functionality:
```javascript
const EnhancedComponent = withSubscription(MyComponent);
```

### Q100: What is render props pattern?
**A:** A pattern where a component accepts a function as a prop:
```javascript
<DataComponent render={data => <p>{data}</p>} />
```

### Q101: What is the difference between shallow and deep copying?
**A:**
- **Shallow copy**: Copies first level only
- **Deep copy**: Copies all nested levels
```javascript
// Shallow
const copy = {...original};
// Deep
const copy = JSON.parse(JSON.stringify(original));
```

### Q102: What are pure components?
**A:** Pure components automatically perform shallow prop and state comparison:
```javascript
class MyComponent extends React.PureComponent {
  render() {
    return <p>{this.props.name}</p>;
  }
}
```

---

## 8. BEST PRACTICES & TIPS

### Q103: What are React best practices?
**A:**
- Use functional components with hooks
- Keep components small and focused
- Use prop drilling alternatives (Context, Redux)
- Avoid mutating state directly
- Use keys in lists
- Memoize expensive computations
- Write pure components
- Use error boundaries

### Q104: What is code splitting?
**A:** Splitting code into smaller chunks that are loaded on demand:
```javascript
const Component = React.lazy(() => import('./Component'));
```

### Q105: How do you handle errors in React?
**A:** Use Error Boundaries or try-catch in event handlers:
```javascript
class ErrorBoundary extends React.Component {
  componentDidCatch(error, errorInfo) {
    console.log(error, errorInfo);
  }
  
  render() {
    return this.state.hasError ? <p>Error!</p> : this.props.children;
  }
}
```

---

## Additional Resources
- React Official Documentation: https://react.dev
- React Hooks API: https://react.dev/reference/react
- Common React Patterns: https://react.dev/learn

---

**Total Questions Covered: 105+**
