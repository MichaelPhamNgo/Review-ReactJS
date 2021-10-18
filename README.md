Table of React JS content
[I. SPA vs MPA] 
[I.1 SPA] 
[I.2 MPA] 
[II. JS HTML DOM] 
[III. JS Browser BOM] 
[IV. JS APIs] 
[V. Create an app react js] 
[II1. ] [II2. ] 
[VI. JSX]

II. JS HTML DOM
When a webpage is loaded, the browser will create a **Document Object Model** called DOM. The HTML elements are ***object***. Each HTML element contains properties and events and is managed by DOM, so the HTML DOM can *get, change, add, or delete* HTML elements.

- HTML DOM methods are actions
- HTML DOM properties are values

***EXAMPLE**

```javascript
<script>
    document.getElementById("demo").innerHTML = "Hello World!";     //getElementById is a method, innerHTML is a property
</script>
```


II.1 Find HTML elements
> Find an element by element id

SYNTAX
```javascript
document.getElementById("id")
```

***EXAMPLE***

> ex: show "Hello World" text into div

```html
<div id="hello"></div>
```
```javascript
document.getElementById("hello").innerHTML = "Hello World";
```