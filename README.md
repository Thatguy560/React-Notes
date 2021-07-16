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

[Understanding Functional Components vs. Class Components in React](#Functional-Components-vs-Class-Components-in-React)


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
 
**Class features vs. Hooks equivalents**

**State**

```JavaScript
// Class

class CounterButton extends Component {
    constructor() {
        super();
        this.state = {
            count: 0
        }
    }

    render() {
        return <button onClick={() => this.setState({ count: this.state.count + 1})}> 
            { this.state.count }
        </button>
    }
}

// Hooks
const CounterButton = props => {
    const [count, setCount] = useState(0);

    return <button onClick={() => setCount(count + 1)}>
            { count }
    </button>
}
```

**ComponentDidMount()**

```JavaScript
// Class 
componentDidMount() {
    console.log("I just mounted")
}

// Hooks
useEffect(() => {
    console.log("I just mounted")
}, [])
```

**ComponentWillUnmount**

```JavaScript
// Class
componentWillUnmount() {
    console.log("I am un-mounting")
}

// Hooks
useEffect(() => {
    return () => console.log("I am un-mounting")
}, [])
```

**ComponentWillReceiveProps / ComponentDidUpdate**

```JavaScript
// Class
componentWillReceiveProps(nextProps) {
    if (nextProps.count !== this.props.count) {
        console.log("Count changed", nextProps.count)
    }
}

// Hooks
// Printing 1st iteration
useEffect(() => {
    console.log("Count changed", props.count)
}, [props.count])

// Skipping first iteration (Exactly like componentWillReceiveProps);
const isFirstRun = useRef(true)
useEffect(() => {
    if (isFirstRun.current) {
        isFirstRun.current = false
        return;
    }
    console.log("Count changed", props.count);
}, [props.count]);

// Class
componentDidUpdate() {
    console.log("Just updated...")
}

useEffect(() => {
    console.log("Just updated...");
})
```

**DOM Refs**

```JavaScript
// Class
class InputWithFocus extends React.Component {
    constructor() {
        super();
        this.inputRef = null;
    }
    render() {
        return 
        <div>
        <input ref={inputRef => { this.inputRef = inputRef }}/>
            <button onClick={() => this.inputRef.focus()}>
                Focus the input
            </button>
        </div>
    }
}

// Hooks
const InputWithFocus = (props) => {
    const inputRef = useRef(null);

    return 
    <div>
        <input ref={inputRef} />
        <button onClick={() => inputRef.current.focus()}>
            Focus the input
        </button>
    </div>
}
```

**this.myVar**

useRef has another cool usage besides DOM refs, it is also a generic container whose current property is mutable and can hold any value, similar to an instance property on a class.

For example, to keep an interval id:

```JavaScript
const Timer = (props) => {
    const intervalRef = useRef();

    useEffect(() => {
        const id = setInterval(() => {
            // ...
        })
    })
}
```

**Comparing with the previous state/props**

- Same lifecycle method, like componentDidUpdate, provides the previous state and props.
- If you really need the previous values for your Hooks, this can be imitated the following way (using yet again our good friend - useRef):

```JavaScript
const Counter = props => {
    const [count, setCount] = useState(0);

    const prevCountRef = useRef();
    useEffect(() => {
        prevCountRef.current = count
    })
    const prevCount = prevCountRef.current;

    return <h1>Now: {count}, before: {prevCount}</h1>
}
```

**ShouldComponentUpdate**

We gonna use memo for this one, while this is not a Hook, it's still part of the class-to-functional-component migration plan:

```JavaScript
// Class
shouldComponentUpdate(nextProps) {
    return nextProps.count !== this.props.count
}

// memo 
import React, { memo } from "react"

const MyComponent = memo(
    _MyComponent,
    // Notice condition is inversed from shouldComponentUpdate
    (prevProps, nextProps) => nextProps.count === prevProps.count
)
```

And that is React Hooks in a nutshell

# Functional-Components-vs-Class-Components-in-React

Recently functional components are becoming more and more popular so why is that?

***

**Rendering JSX**

First of all, the clear difference is the syntax. Just like in their names, **a functional component is just a plain JavaScript function that returns JSX**. A class component is a JavaScript class that extends React.Component which has a render method.

```JavaScript
import React from "react"

const FunctionalComponent = () => {
    return <h1>Hello, world</h1>;
}
```

As you can see, a functional component is a function that returns JSX. If you are not familiar with arrow functions introduced in ES6, here is an example without them.

```JavaScript
import React from "react"

function FunctionalComponent() {
    return <h1>Hello, world</h1>
}
```

Below is the same example but without destructuring. 

```JavaScript
import React from "react";

class ClassComponent extends React.Component {
    render() {
        return <h1>Hello, world</h1>
    }
}
```

**Passing Props**

Passing props can be confusing but below is how they're written in both class and functional components. 

```JavaScript
// Component to be passed in.

<Component name="Shiori"/>
```

```JavaScript
const FunctionalComponent = ({ name } => {
    return <h1>Hello, {name}</h1>;
})
```

Inside a functional component, we are passing props as an argument of the function. Note that was are using destructing here. Alternatively we can write it without too.

```JavaScript
const FunctionalComponent = (props) => {
    return <h1>Hello, {props.name}</h1>;
}
```

In this case, you have to use props.name instead of name.

```JavaScript
class ClassComponent extends React.Component {
    render() {
        const { name } = this.props;
        return <h1>Hello, { name }</h1>;
    }
}
```

Since it is a class, you need to use **this** to refer to props. And of course, we can use destructuring to get **name** inside props while utilising class-based components.

**Handling State**

Now we all know that we cannot avoid dealing with state variables in a React project. Handling state was only doable in a class component until recently. But now with React 16.8, React Hook **useState** was introduced to allow developers to write stateful functional components. Below is a simple counter that starts from 0, and one click on the button will increment the counter by 1.

**Handling State in functional Components**

```JavaScript
function FunctionalComponent() {
    const [count, setCount] = React.useState(0);

    return (
        <div>
            <p>count: {count}</p>
            <button onClick={() => setCount(count + 1)}>Click</button>
        </div>
    );
};
```

To use state variables in a functional component, we need to use a useState Hook, which takes an argument of initial state. In this case we start with 0 clicks so the initial state of the count will be 0.

Of course you can have more variety of initial state including **null, string** or even **object.** - any type that JavaScript allows! And on the left, as useState returns the current state and function that updates it, we are destructuring an the array like this. You can consider the two elements of the array the **state and the setter**. In this example we named them **Count** and **setCount** to make it easy to understand the connection between the two.

**Handling State in Class Components**

```JavaScript
class ClassComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            count: 0
        }
    }

    render() {
        return (
            <div>
                <p>count: {this.state.count} times</p>
                <button onClick={() => this.setState({ count: this.state.count + 1})}> 
                Click
                </button>
            </div>
        )
    }
}
```

The idea is still the same but a class component handles state a bit differently. Firstly, we need to understand the importance of the React.Component constructor. here is a [link](https://reactjs.org/docs/react-component.html#constructor).

**The constructor for a React component is called before it's mounted. When implementing the constructor for a React.Component subclass, you should call super(props) before any other statement. Otherwise, this.props will be undefined in the constructor, which can lead to bugs.**

Essentially, without implementing the constructor and calling super(props), all the state variables that you are trying to use will be undefined. So let's define the constructor first. Inside the constructor, you will make a state object with a state key and initial value. And inside JSX, we use **this.state.count** to access the value of the state key we defined in the constructor to display the count. Setter is pretty much the same, just different syntax.

Alternatively, you can write an **onClick** function. Remember, the **setState** function takes argument(s) of state, props(optional) if needed.

```JavaScript
onClick={() => {
    this.setState((state) => {
        return { count: state.count + 1 }
    }
}}
```

**Lifecycle Methods**

Finally, let's talk about lifecycles. As you know, lifecycles play an important role in the timing of rendering. For those who are migrating from class components to functional cpmponents, you must be wondering what could replace lifecycle methods such as componentDidMount() in a class component. And yes, there is a hook that works perfectly for that purpose.

**On Mounting (componentDidMount)**

The lifecycle method **componentDidMount** is called right after the first render completes. There used to be a componentWillMount that happens before the first render, but it is considered legacy and not recommended to use in newer versions of React.

```JavaScript
const FunctionalComponent = () => {
    React.useEffect(() => {
        console.log("Hello")
    }, []);
    return <h1>Hello, World</h1>
}
```

Replacing **componentDidMount**, we use the useEffect hook with the second argument of **[]**. The second argument of the **useState** hook is normally an array of a state(s) that changes, and **useEffect** will only be called on these selected changes. But when it's an empty array like this example, it will be called once on mounting. This is a perfect replacement for a **componentDidMount**. 

```JavaScript
class ClassComponent extends React.Component {
    componentDidMount() {
        console.log("Hello")
    }

    render() {
        return <h1>Hello, World</h1>
    }
}
```

Essentially the same thing happens here with: **componentDidMount** is a lifecycle method that is called once after the first render. 

**On Unmounting (componentWillUnmount**)

```JavaScript
const FunctionalComponent = () => {
    React.useEffect(() => {
        return () => { // Component is un-mounting.
            console.log("Bye")
        }
    }, [])
    return <h1>Bye, World</h1>
};
```

I am happy to tell you that we can also use a **useState** hook for un-mounting as well. But be careful, the syntax is a bit different. **What you need to do is return a function that runs on un-mounting** inside the **useEffect** function. This is especially useful when you have to clean up the subscriptions such as a clearInterval function, otherwise it can cause a severe memory leak on a bigger project. One advantage of using **useEffect** is that we can write functions for both mounting and un-mounting in the same place.

```JavaScript
class ClassComponent extends React.Component {
    componentWillUnmount() {
        console.log("Bye")
     }

     render() {
         return <h1>Bye, World</h1>
     }
}
```

<!-- a Functional Component is just a JavaScript function that returns some JSX -->

**Conclusion**

There are pros anc cons in both styles but Functional Components are taking over modern React in the foreseeable future.

A functional component is written shorter and simpler, which makes it easier to develop, understand, and test. Class components can also be confusing with so many uses of **this**. Using functional components can 

