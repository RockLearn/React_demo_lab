
---

### 2. **Components and Props** (`2_Components_and_Props/README.md`)

<!--```markdown-->
# 🧩 Components and Props in React

React applications are built from **components**—small, reusable pieces that define parts of a UI. **Props** allow data to be passed from one component to another, making components dynamic and versatile.

![Components Structure](https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/React.svg/1024px-React.svg.png)

---

## 📋 Types of Components

1. **Functional Components** - Simple functions that return UI elements (JSX).
2. **Class Components** - Stateful components that can manage internal data using state.

---

### 📌 Example: Functional Component with Props

Here’s an example of a functional component that uses props to display a greeting:

```jsx
import React from 'react';

function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

export default Greeting;
