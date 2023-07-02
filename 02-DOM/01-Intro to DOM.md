# What is DOM?

- Stands for Document Object Model.

- Structured representation of HTML documents.

- Allows JS to access HTML elements and styles and manipulate them.

- DOM is automatically created by the browser as soon as the page loads and is stored in a tree structure.

- In this tree each element is a DOM object.

## DOM Tree

![](/home/parth/.var/app/com.github.marktext.marktext/config/marktext/images/2023-06-16-17-20-51-image.png)

- The DOM always start with the Document Object which is at the top which serves as an entry point into the DOM.

- First child element of Document is usually the html element which is the root element.

- HTML element has two child siblings head and body and they have their respective child elements.

- This is how a DOM Tree is defined.

- DOM Tree also has the values of each child element.

- DOM and DOM methods are part of the Web APIs.

- Web APIs are like a library which browsers implement and we access that through JS.

- Web APIs are also written in JS.

## Selecting and manipulating elements

```js
document.querySelector(".messsage");
```

- In the above line of code, we are selecting the element with class message.

- We can pass and element name, class name or id name as the argument in querySelector method.

```js
let myText = document.querySelector(".message").textContent;
```

- The `textContent` method allows us to extract the text of the passed element/ class/ id in `querySelector`.

```javascript
document.querySelector(".message").textContent = "New Content";
```

- We can manipulate the text content of and element with above code.

```javascript
document.querySelector(".input-field").value = 24;
```

- Adding value to the input field.
