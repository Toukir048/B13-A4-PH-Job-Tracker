## \# Assignment -- 4

## 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

### Answer:

When working with the DOM, JavaScript gives us different ways to select
elements depending on what we need.

### getElementById()

This method selects an element using its unique ID. Since IDs are meant
to be unique, it always returns a single element.
It is simple and efficient when you already know the exact element you
want.

``` javascript
document.getElementById("header");
```

------------------------------------------------------------------------

### getElementsByClassName()

This method selects all elements that share the same class name.
It returns a live HTMLCollection, meaning if the DOM changes, the
collection updates automatically.

``` javascript
document.getElementsByClassName("card");
```

------------------------------------------------------------------------

### querySelector()

This method allows selecting elements using CSS selectors.
It returns only the first matching element.

``` javascript
document.querySelector(".card");
```

------------------------------------------------------------------------

### querySelectorAll()

This also uses CSS selectors but returns all matching elements.\
Unlike getElementsByClassName(), it returns a static NodeList that does
not auto-update.

``` javascript
document.querySelectorAll(".card");
```

------------------------------------------------------------------------

## 2. How do you create and insert a new element into the DOM?

### Answer:

To add a new element into a webpage, we usually follow three basic
steps:

1.  Create the element
2.  Add content to it
3.  Insert it into the page

Example:

``` javascript
const newDiv = document.createElement("div");
newDiv.textContent = "Hello World";
document.body.appendChild(newDiv);
```

This creates a new div, adds text inside it, and inserts it into the
webpage.

------------------------------------------------------------------------

## 3. What is Event Bubbling? And how does it work?

### Answer:

Event bubbling describes how an event moves through the DOM.

When you click an element inside another element, the event does not
stop at the clicked element. Instead, it continues upward through its
parent elements.

For example, if a button is inside a div:

-   The button's event runs first
-   Then the div's event
-   Then the body
-   Then the document

This upward movement from child to parent is known as event bubbling.

------------------------------------------------------------------------

## 4. What is Event Delegation in JavaScript? Why is it useful?

### Answer:

Event delegation means attaching a single event listener to a parent
element instead of attaching multiple listeners to each child element.

For example, instead of adding click listeners to many buttons
individually, we add one listener to their parent container.

It is useful because:

-   It improves performance
-   It reduces memory usage
-   It works for dynamically created elements
-   It keeps code organized and easier to manage

------------------------------------------------------------------------

## 5. What is the difference between preventDefault() and stopPropagation() methods?

### Answer:

Both methods control event behavior, but they serve different purposes.

### preventDefault()

This method prevents the browser's default action, such as submitting a
form or following a link.

``` javascript
event.preventDefault();
```

------------------------------------------------------------------------

### stopPropagation()

This method prevents the event from moving up to parent elements (stops
bubbling), but it does not stop the browser's default behavior.

``` javascript
event.stopPropagation();
```

------------------------------------------------------------------------

