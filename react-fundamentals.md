### Remember

Answer these on your own, then compare answers as a group

1.  What is React?

    Developed by Facebook, React is a javascript library for frontend interface  and UI component development.  React allows for each element or 'component' to be separated into individual files of code.  This is called Component based architecture.  It utilizes its own virtual DOM for ease of development. 

2.  What is create-react-app?

    create-react-app and an included react package that allows a developer to initiate a new project using a single terminal command, as opposed to compiling the project from scratch.  It also sets up a developer server that is auto-refreshed with changes.

3.  What is Component Based Architecture?

    Component based architecture, as used in react, is a form of development structure that utilizes separate "component" files that can then link together in a parent element.

4.  What is JSX?

    JSX (Javascript xml) is a javascript extension that allows incorporation of inline javascript and html syntax.

5.  What is the virtual DOM?

    A virtual DOM is a light representation of the actual DOM. The virtual DOM only updates changes made to code, allowing faster update times as it does not have to re-render all the code.

6.  What is unidirectional (one-way) data flow?

    Unidirectional data flow is when data is passed from Parent to Child.  This Data is read only, children cannot change the data of the parent element.

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`

8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.

Data is passed from parent to child by passing props as a function parameter.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
