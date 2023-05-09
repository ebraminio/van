# 🍦 **VanJS**: A 1.2kB Grab 'n Go Reactive UI Framework without React/JSX

**VanJS** (abbr. **Van**illa **J**ava**S**cript) is an ***ultra-lightweight***, ***zero-dependency*** and ***unopinionated*** Reactive UI framework based on pure vanilla JavaScript and DOM. Programming with **VanJS** feels a lot like React. Check-out the `Hello World` code below:

```javascript
// Reusable components can be just pure vanilla JavaScript functions.
// Here we capitalize the first letter to follow React conventions.
const Hello = () => div(
  p("👋Hello"),
  ul(
    li("🗺️World"),
    li(a({href: "https://vanjs.org/"}, "🍦VanJS")),
  ),
)

van.add(document.body, Hello())
// Alternatively, you can write:
// document.body.appendChild(Hello())
```

**VanJS** helps you manage state and UI binding as well, with a more natural API:

```javascript
const Counter = () => {
  const counter = van.state(0)
  return div(
    "❤️ ", counter, " ",
    button({onclick: () => ++counter.val}, "👍"),
    button({onclick: () => --counter.val}, "👎"),
  )
}

van.add(document.body, Counter())
```

## Why VanJS?

**VanJS** has the vision to be the [scripting language](https://vanjs.org/about#story) for UI, just like `bash` is the scripting language for terminal. **VanJS** empowers frontend engineers, backend engineers, system engineers, data scientists, and anyone else to build comprehensive user interfaces. You can code with **VanJS** anywhere, any time, and on any device – _even on your smartphone!_ 👏👏👏

### Reative Programming without React/JSX

Declarative DOM tree composition, reusable components, reative state binding - **VanJS** offers every good aspect that React does, but without the need of React, JSX, transpiling, virtual DOM, or any hidden logic. Everything is built with simple JavaScript functions and DOM.

### Grab 'n Go

***No installation***, ***no configuration***, ***no 3rd-party dependencies***, ***no transpiling***, ***no IDE setups***. Adding a line to your script or HTML file is all you need to start coding. **VanJS** allows you to focus on the business logic of your application, rather than getting bogged down in frameworks and tools.

### Ultra-Lightweight

**VanJS** is a very thin layer on top of Vanilla JavaScript and DOM, barely enough to make the DOM manipulation and state binding as ergonomic as (if not more than) React, and it delegates most of work to standard browser APIs implemented in native code. As a result, the bundled size of **VanJS** is just 1.2kB, which is **more than 100 times** smaller than most popular UI frameworks:

![Size comparison](doc/size_comp.png)

> _Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away._
>
> _-- Antoine de Saint-Exupéry, Airman's Odyssey_

### TypeScript Support

**VanJS** provides first-class support for TypeScript. Simply download the corresponding `.d.ts` file along with your `.js` file, and you'll be able to take advantage of type-checking, IntelliSense, large-scale refactoring provided by your preferred development environment. Refer to the [Download Table](https://vanjs.org/start#download-table) to find the right `.d.ts` file to work with.

### Easy to Learn

**VanJS** puts heavy emphasis on the simplicity of the framework. There are only 4 exported functions in the API and feels a lot like React. Because of that, the [walkthrough tutorial](https://vanjs.org/tutorial) is the same as the full API referrence, and can be learned within 1 hour for most developers.

## Want to Learn More?

* Download and [Get Started](https://vanjs.org/start)
* Learn from the [Tutorial](https://vanjs.org/tutorial)
* Learn by [Examples](https://vanjs.org/demo)
* Convert HTML snippet to **VanJS** code with our online [HTML to **VanJS** Converter](https://vanjs.org/convert)