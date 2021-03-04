### Remember

Answer these on your own, then compare answers as a group

1.  What are props?

    -Props is an object available to the component.
    -A parent component can add key value pairs to the props object.
    -props are data being passed into a component.

    Props, which stands for properties, are used to pass data from one component to another in a unidirectional flow.

2.  How do you pass props from a parent to a child?

    -We pass props into the child using the child's component tag.
    -We can set up these props on the child's component tag by saying <whateverPropertyName> = <hardcoded data OR a reference to existing data using curly braces>

    Props are passed to child components by passing props as a parameter and defining specific HTML attributes.

3.  How do you access props from a class based child component?

    -From within JSX, we would say {this.props.<propName>} and outside of JSX we would simply say this.props.<propName>

    {this.props.<propName>}

4.  How do you access props from a functional component?

    {props.element<propName>}

5.  How do you bind a function to a parent component so that it can be passed to a child?

1.  From within the constructor, outside of the state, we would say this.<function name> = this.<function name>.bind(this)

2. We can use lexical binding by not having to use the bind method AND by making our function an arrow function.

### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    <div className="queue-container">
      <h1>The Queue</h1>
      <h3>{this.state.questions.length}</h3>
      <h3>questions need answers</h3>
      <Student askQuestion={this.askQuestion} />
      <Mentor answerQuestion={this.answerQuestion} />
    </div>;
  }
}
```
- We are creating a component called Queue and passing down separate methods to each of Queue's children that, when the methods are fired from within the children, will either add a new question to Queue's this.state.questions, or remove the question.

### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?
