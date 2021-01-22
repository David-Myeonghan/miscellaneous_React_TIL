## Before React

    - radition: CSS, HTML, JS

    - JS makes change DOM 
    - DOM behaves differently in each browsers
    - jQuery make a united syntax and deal with it from DOM in each different browsers
    - jQuery makes developers to easily interact with DOM across all the browsers.

    - ## I think, jQuery is suitable for smaller projects that uses a small files##

    - jQuery is one of the Javascript library that provides:
        1. the powerful way of selecting HTML elements
        2. various methods that control efficiently the selected HTML elements.

    ```
    jQuery Basic Syntax.
    $(제어대상).method1().method2(); // keep chaining methods
    // $(Subject).Verb()
    $(.'welcome').html("Hello world!").css("backbround-color", "yellow");
    ```

    - ajax is **A**synchronous **J**avaScript *a**nd **X**ML
        - To interact with Server using JS asyncrhonous way
        - don't have to be XML, could be JSON recently.
        - The very basic API using jQuery

### JS became bigger as websites are bigger

    - Getting easy to work with DOM makes the birth of Single Page Application.
    - Instead of getting a small files(HTML, CSS, JS) for each page, now, focus less on HTML, 
    - We only load the application code once instead of us making new requests to the server where we returned a new document.
    - Now: apps acts more like a desktop app. We stay on the same page for the entire time and,
    - JS file simply changes or updates the HTML file or the DOM to display new things

    - Angular : the birth of MVC model 2010, by Google
    - Data flowing in a complex way, and imperative approach (problem of Architecture).
    - Data was flowing everywhere.

## REACT

    - React: 2013 birth by Facebook

    1. don’t touch the DOM. I’ll do it. 
        - Before React, many libraries manipulate, modify DOM directly by JS file. (Imperative approach)
        - React is Declarative approach(paradigm). Changing the DOM is heavy operation.
        - Instead of changing the DOM directly, tell the state of the app and React automatically just does it for us.

        Virtual Dom 사용,  직접적인 Dom변경 없다. Dom과 비교해 변화가 된 부분만 렌더링.
        Dom 변경 최소화.

    2. Building the website like a Lego blocks. (Reusable Components)
        - Based on the State of the App, Component are built.
        - If you are hard to make a component, copy and paste from other component.

        - 재사용 가능한 컴포넌트!

    3. Unidirectional data flow (Data flows one way).
        - State and Components are combined and this creates the Virtual DOM(Tree-like, blueprint of the real DOM) and changes the real DOM.
        - JSX: HTML-like syntax inside of JS

        - So, if you want to change something in website, the state has to be changed.
        - State moves down only. One way data flow. Easy to find and fix bugs.

        - 데이터 흐름이 한방향. 스테이트의 변경이 아래쪽으로 한방향. 버그 찾고 고치기가 쉽다.

    4. React is just UI(How to look at a JS object), the rest is up to you. Everywhere React
        - Just an UI library. Angular is the whole kitchen.
        - React Desktop, React VR, React Native, React terminal is also available. 
        - Core React Library, React Dom Library is essential.
        - Cross-platform

        - 리액트는 UI 라이브러리일 뿐.

## The Job of a React developer

1. Decide on Components (How many components do we need?)
2. Decide the State and where it lives (placing the state)
3. What changes when state changes

NPM installed when Node installed
NPX working when npm version 5.8 higher
NPX install without global version.

- Installation

1. Command + Shift + P - command: Install code command in PATH in visual studio Code
   Install nvm in terminal
2. And install Node through nvm: nvm install (-v)

YARN is the same as NPM, it’s personal choice. but in one project, use either one only.

Create-React-App = instead of using Babel and Webpack, quick way to react code.

BABEL: JS compiler. Transfer to JS that all browsers can understand. make all browsers understand React Syntax. 
Webpack: module bundler. Bundles and make smaller JS files

---

Class: has more functionality…???

When do we break things down into components?

- Reusable components - less repeat code

Functional component(Arrow function): when do not need a internal state, or lifecycle method(componentDidMount())

.bind

- A method on any function that returns a new function where context of this is set to whatever we passed to it.

arrow functions and binding in React. A good rule of thumb is this: Use arrow functions on any class methods you define and aren't part of React (i.e. render(), componentDidMount()).
Functional components are the best type of component to render if you don’t need access to state or lifecycle methods. It has benefits of being easy to test, easier to read, and easier to write.

Deploy static website using GitHub, and gh-pages

'Npm list package’
‘Nom update’ updates the packages with version ‘^’ in package.json

---

---

E-commerce Web

Default installing node-sass to React

---

Architecting components
Tree-like structure.
Easy to get lost - Refer to React developer tools on Chrome

React provide style tag to all HTML element to use css

---

Downsize of SPA
No routing function (React is just UI) -> solved by react-router-dom (by providing history api from browsers)

React-router-dom
Switch:if it sees something match the path, it just render one single route. Not two.

When it’s rendered, it gets 3 props.

1. history

- Two ways of navigate in React
  - 1.  Link (like in HTML <a>) but not re-render, just replacing what component to mount.
  - 2.  Using history. <button onClick={() => props.history.push(‘./topics’)}>Topics </button>
    - Push( ):

1. location

- Pathname: gives what the full url looks like.

1. Match

- Url: only display the url up until where it actually matched with router
- Path: the pattern that the route is looking to map.
- isExact: true if entire address is matched
- Params: an object of the url parameter(ex, ‘:id’, dynamically changing)

---

Prop tunneling (Prop drilling)

- Tunneling props to pass props to their children.

Solution: withRouter power up the component to access to prop.history, match, and location.
HOC takes a component as an argument and transform the component and return the transformed component.

---

Redux

1. Single source of truth(ons single object)
2. State is read only
3. Changes using pure functions

Redux Flow
 Action ->(middleware)-> Root reducer -> store -> DOM Changes

Flux pattern(unidirectional data flow)
Action -> Dispatcher -> Store(state) -> View

this.state used with Redux together.
Create a new object in Redux. Instead of modifying props
