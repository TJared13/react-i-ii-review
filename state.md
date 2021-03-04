### Remember

Answer these on your own, then compare answers as a group

1.  What is state?

    State is an element of a Component class that is used to store data, that can then be passed to child components.  State is an object in React, so we must treat it as such (this.state.element).

2.  Where do you set initial state?

    The initial state is set in the constructor element, underneath the call of super(), of a class using 'this.state = '

3.  What method do you use to update state?
    We use the setState method to update state values.  When we call setState, we need to send in an object that specifies our target properties that need changed, along with values.  Example:
    this.setState({elem: val})

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Tim Biles</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```
This code is creating a component called LeadMentor.  LeadMentor is displaying the questions answered from its state in it's return.  It provides functionality for a user to increase the number of questions answered held in state by invoking the handleClick method.  When the state value for questions gets updated by button click, the component re-renders showing the updated number.

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked

6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.

### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?
