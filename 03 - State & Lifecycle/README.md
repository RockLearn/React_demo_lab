
---

### 3. **State and Lifecycle** (`3_State_and_Lifecycle/README.md`)

<!--```markdown-->
# ⏲️ State and Lifecycle in React

State allows a React component to keep track of data that can change over time, like user input or dynamic content. Lifecycle methods help manage what happens when a component is created, updated, or removed.

![State and Lifecycle Diagram](https://miro.medium.com/v2/resize:fit:1400/1*HeJahz1pxt_x0E14yF7QfQ.png)

---

## 🌱 Adding State to a Class Component

State is commonly used in **class components**. Initialize it in the `constructor` and update it with `setState()`.

```jsx
import React, { Component } from 'react';

class Clock extends Component {
  constructor() {
    super();
    this.state = { date: new Date() };
  }

  componentDidMount() {
    this.timerID = setInterval(() => this.tick(), 1000);
  }

  componentWillUnmount() {
    clearInterval(this.timerID);
  }

  tick() {
    this.setState({ date: new Date() });
  }

  render() {
    return (
      <div>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}

export default Clock;
