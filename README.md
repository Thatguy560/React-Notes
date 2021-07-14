# React Notes 

## Sources

[Top 40 ReactJS Interview Questions and Answers in 2021](https://www.simplilearn.com/tutorials/reactjs-tutorial/reactjs-interview-questions)

[React Functional Components VS Class Components](https://medium.com/wesionary-team/react-functional-components-vs-class-components-86a2d2821a22)

[React Class features vs. Hooks equivalents](https://medium.com/soluto-engineering/react-class-features-vs-hooks-equivalents-745368dafdb3)


[Understanding Functional Components vs. Class Components in React](https://www.twilio.com/blog/react-choose-functional-components)

## Index 

[React-Interview-Questions](#React-Interview-Questions)

[Class-Based-Components](#Class-Based-Components)

[Functional-Components](#Functional-Components)

[React Class features vs. Hooks equivalents](#React-Class-features-vs-Hooks-equivalents)


# React-Interview-Questions

## 1. What are the benefits of a single page application?

- Battery reusability
- Optimization 
- Client-side rendering
- User experience
- Easy debugging
- Performance
- Performance
- Less complex implementation 
- Better Caching
- Better SEO Optimization 

An important feature of single-page applications is performance. They get a performance boost by loading HTML, CSS, and JavaScript resources as soon as the website is loaded.

The reason is that when users come to an application, they need the shortest possible wait time so that they can do their work and leave. The performance reflects the demand for the application. 

If the application does not provide the necessary performance, users may leave that app and choose another platform. That's one of the primary reasons developers choose single-page apps nowadays. 

## 2. What is the difference between between state and props?

![StateVsProps](./assets/Screenshot%202021-07-13%20at%2014.03.33.png)

- State can be used to hold information about the components.Whilst Props are used to pass data from one component to other components as arguments.
- State is mutable (can be changed) whilst Props are immutable (can't be changed).
- Child components can't be accessed in the state. Whilst with props Child components can be accessed. 
- Stateless components cannot have state. Whilst props have props.

## 3. What are the components in React?

Components are the building blocks of any React application, and a single page app usually consists of multiple components. A component is essentially a piece of user interface. It splits the user interface into independent, re-usable parts that can be processed separately.  

There are two types of Components in React:

![Components](https://www.simplilearn.com/ice9/free_resources_article_thumb/react-component.JPG)

- **Functional Components** - These types of components have no state of their own and only contain render methods, and therefore are only called **stateless components.** They may derive data from other components as props (properties).

```JavaScript
function Greeting(props) {
    return <h1>Welcome to {props.name}</h1>
}
```

- **Class Components** - These type of components can hold and manage their own state and have a separate render method to return JSX on the screen. They are also called Stateful components as they can have a state. 

```JavaScript
class Greeting extends React.Component {
    render() {
        return <h1>Welcome to {this.props.name}</h1>
    }
}
```

## 4. What is the use of Render() in React?

- It is required for each component to have a render() function. This function returns the HTML which is to be displayed in the component.

- If you need to render more than one element, all of the elements must be inside one parent tag like ```<div> or <form>.```

![Rendering Components](https://www.simplilearn.com/ice9/free_resources_article_thumb/default-app.JPG)

## 5. What is a state in React?

- The state is a built-in React Object that is used to contain data or information about the component. The state in a component can change over time, and whenever it changes the component re-renders.
- The change in state can happen as a response to user action or system-generated events. It determines the behavior of the component and how it will render. 

## 6. How do you implement state in React?

![State](https://www.simplilearn.com/ice9/free_resources_article_thumb/state-holds.JPG)

- State holds the data that a component renders on the web app.
- We can access the state properties e.g. this.state.car

## 7. How do you update the state of a component?

We can update the state of a component by using the built-in **'setState()** method:

![updatingState](https://www.simplilearn.com/ice9/free_resources_article_thumb/class-app.JPG)

## 8. What is JSX?

JSX is a syntax extension of JavaScript. It is used with React to describe what the user interface should look like. By using JSX, we can write HTML structures in the same file that contains JavaScript code.

![JSX](https://www.simplilearn.com/ice9/free_resources_article_thumb/what-is-jsx.JPG)

## 8. What are Props in React?

- Props are short for Properties. It is a React built-in object that stores the value of attributes of a tag and works similarly to HTML attributes. 
- Props provide a way to pass data from one component to another component. Props are passed to the component in the same way as arguments are passed in a function. 

## 9. What is a higher order component in React?

A higher-order component acts as a container for other components. This helps to keep components simple and enables re-usability. They are generally used when multiple components have to use a common logic.

## 10. How can you embed two or more components into one?

We can embed two or more components into one using this method:

![embeddingComponents](https://www.simplilearn.com/ice9/free_resources_article_thumb/classapp-extends.JPG)

## 11. What are the differences between Class and Functional Components?

<p>
    <img src="./assets/Screenshot 2021-07-13 at 14.36.35 copy.png" width="500" height="425"/>
</p>

- State in class components can hold or manage state, whilst Functional components cannot hold or manage state.
- Class Components are more complex than stateless components (Functional components).
- Class based components will work with all lifecycle methods whilst Functional components do not work with any lifecycle methods.
- Class based components can be re-used whilst functional components can't be re-used.

- **Class Components Example:**

![Class-Component](https://www.simplilearn.com/ice9/free_resources_article_thumb/class-components.JPG)

- **Functional Components Example:**

![Functional-Component](https://www.simplilearn.com/ice9/free_resources_article_thumb/functional-components.JPG)

## 12. Explain the lifecycle methods of components. 

- **GetInitialState():** This is executed before the creation of the component. 
- **ComponentDidMount():** is executed when the component gets rendered and placed on the DOM.
- **shouldComponentUpdate():** is invoked when a component determines changes to the DOM and returns "true" or "false" value based on certain conditions.
- **ComponentDidUpdate():** Is invoked immediately after rendering takes place.
- **ComponentWillUnmount():** Is invoked immediately before a component is destroyed and unmounted permanently.

## 13. What are the features of React?

**JSX** - JSX (JavaScript XML) Is a syntax extension to JavaScript. It is used with React to describe what the user interface should look like. By using JSX, we can write HTML structures in the same file that contains JavaScript code.

**Components:** Components are the building blocks of any React application, and a single app usually consists of multiple Components. It splits the user interface into independent reusable parts that can be processed separately. 

**Virtual DOM:** React keeps a lightweight representation of the real DOM in the memory, and that is known as the virtual DOM. When the state of an object changes, virtual DOM changes only that object in the real DOM, rather than updating all the objects.

**One-way data-binding:** React's one-way data binding keeps everything modular and fast. A unidirectional data flow means that when designing a React app, you must often nest child components within parent components. 

**High Performance** - React updates only those components that have changed, rather than updating all the components at once, this results in much faster web applications.

## 14. Can web browsers read JSX directly?

- Web browsers cannot read JSX directly. This is because they are built to only read regular JS objects and JSX is not a regular JavaScript object.
- For a web browser to read a JSX file, the file needs to be transformed into a regular JavaScript object. For this, we use Babel.

![Babel](https://www.simplilearn.com/ice9/free_resources_article_thumb/babel.JPG)

## 15. What is the virtual DOM?

DOM stands for Document Object Model. The DOM represents an HTML (Hyper-Text Markup Language) document with a logical tree structure. Each branch of the tree ends in a node, and each node contains objects.

![DOM](https://www.simplilearn.com/ice9/free_resources_article_thumb/virtualdom.JPG)

React keeps a lightweight representation of the real DOM in the memory, and that is known as the virtual DOM. When the state of an object changes, the virtual DOM changes only that object in the real DOM, rather than updating all the objects.

![VirtualDOM](https://www.simplilearn.com/ice9/free_resources_article_thumb/real-dom.JPG)

## 16. Why use React instead of other Frameworks, like Angular?

**Easy creation of dynamic applications:** React makes it easier to create dynamic web applications because it provides less coding and provides more functionality, whereas with JavaScript applications, code tends to get complex very quickly.

**Improved performance:** React uses virtual DOM, which makes web applications perform faster. Virtual DOM compares it's previous state and updates only those components in the real DOM, whose states have changed, rather than updating all the components like conventional web applications.

**Re-usable Components:** Components are the building blocks of any React application, and a single app usually consists of multiple components. These components have their own logic and controls and they can be reused through the application, which in turn dramatically reduces the development time of an application. 

**Unidirectional Data Flow:** React follows a unidirectional data flow. This means that when designing a React App, we often nest child components within parent components. And since the data flows in a single direction, it becomes easier to debug errors and know where the problem occurs in an application at the moment.

**Dedicated tools for Easy Debugging:** Facebook has released a chrome extension that we can use to debug React Applications. This makes the process of debugging React to web applications faster and easier.

## 16. What is an event in React?

An event is an action that a user or system may trigger, such as pressing a key, a mouse click etc.

- **React events are named using camelCase, rather than lowercase in HTML.**
- **With JSX, you can pass a function as the event handler, rather than a string in HTML.**

```JavaScript
<Button onPress={lightUp}/>
```

## 17. What is an event in React?

A React event can be created doing the following:

![Event](https://www.simplilearn.com/ice9/free_resources_article_thumb/question-9.JPG)

## 18. What are Synthetic events in React?

- Synthetic events combine the response of different browser's native events into one API, ensuring that the events are consistent across different browsers. 
- The application is consistent regardless of the browser it is running in. Here, **preventDefault()** is a synthetic event.

![syntheticEvent](https://www.simplilearn.com/ice9/free_resources_article_thumb/function-app.JPG)

## 19. Explain how lists work in React?

- We create lists in React as we do in Regular JavaScript. Lists display data in an ordered format. 
- The traversal of lists is done using the map() function.

![List](https://www.simplilearn.com/ice9/free_resources_article_thumb/const.JPG)

## 20. Why is there a need for using keys in Lists?

Keys are very important in lists for the following reasons:

- A key is a unique identifier and it is used to identify which items have changed, been updated or deleted from lists.
- It also helps to determine which components need to be re-rendered instead of re-rendering all the components every time. Therefore, it increases performance, as only the updated components are re-rendered.

## 21. What are forms in React and how are they created?

React employs forms to enable users to interact with web applications.

- Using forms, users can interact with the application and enter the required information whenever needed. Form container certain elements, such as text fields, buttons, checkboxes and radio buttons etc.
- Forms are used for many different tasks such as user authentication, searching, filtering, indexing etc. 

We can create forms in React by doing the following: 

![Form](https://www.simplilearn.com/ice9/free_resources_article_thumb/class-name.JPG)

The above code will yield an input field with the label **Na,e** and a submit button. It will also alert the user when the submit button is pressed. 

## 22. What is an arrow function and how is it used in React?

- An arrow function is a short way of writing a function to React.
- It is unnecessary to bind **'this'** inside the constructor function when using an arrow function. This prevents bugs cause by the use of **'this'** in React callbacks.

**Without Arrow Function**

![Without](https://www.simplilearn.com/ice9/free_resources_article_thumb/arrow.JPG)

**With Arrow Function**

![With](https://www.simplilearn.com/ice9/free_resources_article_thumb/arrow.JPG)

## 23. What is React Router?

React Router is a routing library built on top of React, which is used to create routes in a React application. 

## 24. Why do we need to React Router?

- It maintains consistent structure and behavior and is used to develop single-page web applications
- Enables multiple views in a single application by defining routes in the React application.

## 25. How is React Routing different from conventional routing?

![React-Routing](./assets/Screenshot%202021-07-13%20at%2014.03.33.png)

- React Routing is a single HTML Page whilst with conventional routing each view is a new HTML file.
- React routing the user navigates multiple views in the same file whilst with conventional routing the user navigates multiple files for each view. 
- As it's a single file the page does not refresh in React Router, whilst with conventional Routing the page refreshes every time the user navigates. 
- Improved performance with React Routing compared to slower performance with conventional routing.

## 26. How do you implement React Routing?

We can implement Routing in our React application using this method: 

Considering we have the components **App, About** and **Contact** in the application

![React-Routing](https://www.simplilearn.com/ice9/free_resources_article_thumb/routing.JPG)

## 27. How do you style React Components?

- Inline Styling

![Inline](https://www.simplilearn.com/ice9/free_resources_article_thumb/class-simple.JPG)

```JavaScript
class Simple extends React.Component {
    render() {
        return (
            <div>
            <h1 style={{color: "blue"}}>Hello Simple!</h1>
            </div>
        );
    }
}
```

- JavaScript Object

![Object](https://www.simplilearn.com/ice9/free_resources_article_thumb/hello-simple.JPG)


```JavaScript
class Simple extends React.Component {
    render() {
        const simpleStyle = {
            color: "White",
            backgroundColor: "Green",
            margin: "8px",
            fontFamily: "Open Sans"
        }
        return (
            <div>
            <h1 style={simpleStyle}>Hello Simple!</h1> 
            </div>
        );
    }
}
```

## 28. What is Redux? 

Redux is an open-source, JavaScript library used to manage the application state. React uses Redux to build the user interface. It is a predictable state container for JavaScript applications and is used for the entire applications state management. 

# Functional-Components
## Introduction to Component 

- A component represent the part of user interface.
- Components are re-usable and can be used anywhere in user interface.

**Functional Components or Stateless Component**

- It is simple JavaScript functions that simply returns HTML UI.
- It is also called "stateless" components because they simply accept data and display them in some form that is they are mainly responsible for rendering UI.
- It accepts properties (props) in function and returns HTML (JSX).
- It gives solution without using state.
- There is no render method used in functional components.
- These can be typically defined using arrow functions but can also be created with the regular function keyword.

```JavaScript
// With Arrow Function

import React from "react";

const Person = (props) => (
    <div>
    <h1>Hello, {props.name}</h1>
    </div>
);

export default Person

import React from "react";

function Person(props) {
    return (
        <div>
        <h1>Hello, {props.name}</h1>
        </div>
    )
}

export default Person;
```

Lifecycle method or Lifecycle hooks in functional component. 

Component lifecycle method does not exist in functional components, because a functional component is just a plain JavaScript function, we cannot use setState() method inside a component. That's why they also get called functional stateless components. 

We can use React Hooks in functional component, useEffect() hook can be used to replicate **lifecycle behavior**, and **useState** can be used to store state in a functional component.

```JavaScript
// Example

const User = (props) => {
    const [values, setValues] = useState({
        email: "",
        password: ""
    })

    useEffect(() => {
        if (!props.fetched) {
            props.fetchData()
        }
        console.log("Mount It")
    }, [])
    // NOTE: By passing an empty array as second argument triggers the callback in useEffect only after the initial render this replicating "componentDidMount" lifecycle behavior.
    return(

     )
    } 

// useEffect can also return a function that will be run when the component is unmounted. This can be used to unsubscribe to listeners and can be used to replicate the componentWillUnmount behavior.

// E.g. componentWillUnmount

useEffect(() => {
    window.addEventListener("unhandledRejection", handler)
    return () => {
    window.removeEventListener("unhandledRejection", handler)
    }
}, [])
```
  
# Class-Based-Components

- It is regular ES6 classes that extends component class from React Library.
- Also known as "Stateful" components because they implement logic and state. 
- It must have render() method returning HTML
- It has complex UI Logic
- You pass props to class components and access them with this.props.

```JavaScript
// Example
import React, { Component } from "react"

class Person extends Component {
    constructor(props) {
        super(props);
        this.state = {
            name: "Bikash";
        }
    }

    render() {
        return (
            <div>
            <h1>Hello {this.state.name}</h1>
            </div>
        )
    }
}

export default Person;
```

**Lifecycle method or Lifecycle hooks in class Component**

***

The lifecycle hooks of class component can be classified in 4 phases.

1. **Mounting():**

- When an instance of a component is being created and inserted into the DOM.
- It has 4 method constructor(), static, getDerivedStateFromProps(), render() and componentDidMount()

**a.constructor(props)**
- A special function that will get called whenever a new component is created.
- Initializing the state binding the event handler 
- super(props) that directly over writes this.state (b.static.getDerivedStateFromProps(props, state))
- When the state of the component depends on changes c.render():
- We read props and state and return JSX (d.componentDidMount())
- Invoked immediately after a component and all it's children components have been rendered to the DOM.

2. **Updating():**

- When a component is being re-rendered as a result of change to either it's props or state.
- It has 5 lifecycle static (getDerivedStateFromProps(), shouldComponentUpdate(), render(), getSnapshotUpdate() and componentDidUpdate())

**a.getDerivedStateFromProps()**

- This is the first method that is called when a component gets updated.
- This is still the natural place to set the state object based on the initial props.
  
**b.shouldComponentUpdate()**

- In this method you can return a Boolean value that specifies whether React should continue with the rendering or not.
- The default value is true.

**c.getSnapshotBeforeUpdate()**

- The getSnapshotBeforeUpdate() method you have access to the props and state before the update, meaning that even after the update, you can check what the values were before the update.
- If the getSnapshotBeforeUpdate() method is present, you should also include the componentDidUpdate() method, otherwise you'll get an error. 

**d.ComponentDidUpdate()**

- The componentDidUpdate() method is called after the component is updated in the DOM.

3. **UnMounting**

- Used when component is being removed from the DOM.
- It has 1 lifecycle componentWillUnmount().

4. **Error Handling**

- When there is an error during rendering.
- It has 2 lifecycle static getDerivedStateFromProps() and componentDidCatch().

**Why use a functional components instead of a class component?**

Benefits you get by using functional components in React:

1) Functional components are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks.
2) It has less code which makes it more readable.
3) It will get easier to separate container and presentational components because you need to think more about your component's state if you don't have access to setState() in your component.

# React-Class-features-vs-Hooks-equivalents
 
