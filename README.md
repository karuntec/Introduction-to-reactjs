# Introduction-to-reactjs

# 1. React JS
React JS is an open-source JavaScript library used to build user interfaces. It was developed by Facebook.

# Why React JS?
1.Performant websites
2.Fewer lines of code
3.Improves readability of code
4.Less time consuming
5.Open Source
6.Reusable code

# Advantages of React JS
Easy to Learn,
Large Community,
Developer Toolset,

# 2. Running JavaScript in HTML
We can run JavaScript in HTML using the HTML script element. It is used to include JavaScript in HTML.
 ``` <body>
  <div id="root"></div>
  <script type="text/javascript">
    const rootElement = document.getElementById("root");
    const element = document.createElement("h1");
    element.textContent = "Hello World!";
    element.classList.add("greeting");
    rootElement.appendChild(element);
  </script>
</body>
```
Here the type attribute specifies the type of the script.

To include an external JavaScript file, we can use the HTML script element with the attribute src. The src attribute specifies the path of an external JS file.

``` <script type="text/javascript" src="PATH_TO_JS_FILE.js"></script>   ```
### Note:
When the browser comes across a script element while loading the HTML, it must wait for the script to download, execute it, and only then can it process the rest of the page.

So, we need to put a script element at the bottom of the page. Then the browser can see elements above it and doesn’t block the page content from showing.

If more than one script elements are in the HTML, the script elements will be executed in the order they appear.

# 3. Creating Elements using React JS
## 3.1 React CDN
```
<script src="https://unpkg.com/react@17.0.0/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@17.0.0/umd/react-dom.development.js"></script>
<script src="https://unpkg.com/@babel/standalone@7.12.4/babel.js"></script> 
```
## 3.2 React.createElement()
The React.createElement() method is used to create an element using React JS. It is similar to the document.createElement() method in regular JavaScript

``` React.createElement(type, props);  ```
type - Tag names like div, h1 and p, etc.
props - Properties like className, onClick and id, etc.

Props are shorthand for properties. It is an optional argument

```
<script type="module">
  const elementProps = { className: "greeting", children: "Hello world!" };
  const elementType = "h1";
  const element = React.createElement(elementType, elementProps);
</script>
```
## Note:
The type attribute value of the HTML script element should be module to run React JS

## 3.3 ReactDOM.render()
The ReactDOM.render() method is used to display the React element.

Syntax:
```ReactDOM.render(reactElement, container); ```

reactElement - What to render
container - Where to render

```<body>
  <div id="root"></div>
  <script type="module">
    const elementProps = { className: "greeting", children: "Hello world!" };
    const elementType = "h1";
    const element = React.createElement(elementType, elementProps);
    ReactDOM.render(element, document.getElementById("root"));
  </script>
</body> 
