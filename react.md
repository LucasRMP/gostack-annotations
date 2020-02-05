# REACT

## WHAT IS REACT?

- React is a **library** used to build **user interfaces**
- React can be used in anywhere that has a user interfaces, such as web, mobile, IoT, etc
- Much used in single page applications (**SPA**)

## CAN WE CALL REACT A FRAMEWORK

- React has built a hole **ecosystem** around its library, that wraps a lot of platforms and techs that has born around react, so it can **yes** be called a framework

### JAVASCRIPT EVERYWHERE

## REACT / REACTJS / REACT NATIVE

- **React** is the library used in the UI construction
- **ReactJS** is react when it is operating on the browser using **ReactDOM**
- **React Native** is react when it is operating with native elements
  <br />
  <br />

This is a react **component**:

```js
import React from "react";

import "./button.css";
import icon from "./icon.png";
function Button() {
  return (
    <button>
      <img src={icon} />
    </button>
  );
}
```

## WHY USING REACT?

- Code organization
  - Component orientated interfaces
  - We split chunks of code in small components that has different functions
- Responsability division
  - The **frontend** became only responsible to the interface
  - One **API**, multiple **clients**
- Declarative programming
  - The developer describes each step that the machine has to do in order to reach the expected result

## JSX

- **JavaScript + XML**
- The abillity to write **HTML** inside **javascript** code
- Abillity to create our own elements

## BABEL / WEBPACK

- The browser doesn't understand all this modern JS features
- **Babel** converts this code to a compiled code that most browsers can read
- **Webpack** - live reload that transform the compiled code from babel into a bundle that goes to the browser
