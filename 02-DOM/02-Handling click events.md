# What are events?

- Mouse click

- Mouse moving

- Keypress

# Event Listener

- Waits for a certain event to happen and then react to that event accordingly.

- First we need to select the element where event is going to happen.

- Most of the times its a button.

```js
document.querySelector(".button-class").addEventListener("click", function() {
  console.log(document.querySelector(".input-class").value);  
});
```

- The above code adds an event listener when we click on the button and displays the value of the input field in console when the event is executed.
