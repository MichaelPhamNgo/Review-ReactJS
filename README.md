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

# II. JS HTML DOM
When a webpage is loaded, the browser will create a **Document Object Model** called DOM. The HTML elements are ***object***. Each HTML element contains properties and events and is managed by DOM, so the HTML DOM can *get, change, add, or delete* HTML elements.

- HTML DOM methods are actions
- HTML DOM properties are values

***EXAMPLE***

```javascript
<script>
    document.getElementById("demo").innerHTML = "Hello World!";     //getElementById is a method, innerHTML is a property
</script>
```


## II.1 Finding HTML Elements

<table>
    <tr>
        <th>Method</th>
        <th>Description</th>
        <th>Syntax</th>
    </tr>
    <tr>
        <td>document.getElememtById</td>
        <td>Find an element by element id</td>
        <td>document.getElementById(id)</td>
    </tr>
    <tr>
        <td>document.getElementsByTagName</td>
        <td>Find elements by tag name</td>
        <td>document.getElementsByTagName(name)</td>
    </tr>
    <tr>
        <td>document.getElementsByClassName</td>
        <td>Find elements by class name</td>
        <td>document.getElementsByClassName(name)</td>
    </tr>
    <tr>
        <td>document.querySelector</td>
        <td>Find a selector</td>
        <td>document.querySelector(selector)</td>
    </tr>
    <tr>
        <td>document.querySelectorAll</td>
        <td>Find all selectors</td>
        <td>document.querySelectorAll(selectors)</td>
    </tr>
</table>

> Find an element by element id

***SYNTAX***
```javascript
document.getElementById("id")
```

***EXAMPLE***
```html
<div id="ex-id"></div>
```
```javascript
//ex: show "Hello getElementById" text into div
document.getElementById("ex-id").innerHTML = "Hello getElementById";
```

> Find an element by class name

***SYNTAX***
```javascript
document.getElementsById("class name")
```

***EXAMPLE***
```html
<div class="ex-class"></div>
<div class="ex-class"></div>
<div class="ex-class"></div>
```
```javascript
//ex: show "Hello getElementsByClassName" text into div class dom
var exClasses = document.getElementsByClassName("ex-class");
for(let exClass of exClasses){
    exClass.innerHTML = "Hello getElementsByClassName";
}        
```

> Find an element by tag name

***SYNTAX***
```javascript
document.getElementsByTagName("tag name")
```

***EXAMPLE***
```html
<h4></h4>
<h4></h4>
<h4></h4>
```
```javascript
//ex: show "Hello getElementsByTagName" text into h4
var h4s = document.getElementsByTagName("h4");
for(let h4 of h4s){
    h4.innerHTML = "Hello getElementsByTagName";
}     
```

> Find an element by CSS Selector
***SYNTAX***
```javascript
document.querySelector("selector")		//selector can be id, tag, or class
```

***EXAMPLE***
```html
<div class="selector1"></div>
<div class="selector"></div>
<div class="selector2"></div>
```
```javascript
//ex: show "Hello querySelector"
document.querySelector(".selector").innerHTML = "Hello querySelector";
``` 

> Find an element by CSS Selectors
***SYNTAX***
```javascript
document.querySelectorAll("selectors")		//selector can be id, tag, or class
```

***EXAMPLE***
```html
<p></p>
<p></p>
<p></p>
```
```javascript
//ex: show "Hello querySelectorAll"
var ps = document.querySelectorAll("p");
for(let p of ps){
	p.innerHTML = "Hello querySelectorAll";
}   
``` 

## II.2 Actions on HTML elements

<table>
    <tr>
        <th>Property</th>
        <th>Description</th>
        <th>Syntax</th>
    </tr>
    <tr>
        <td>innerHTML</td>
        <td>Change the inner HTML of an element</td>
        <td>element.innerHTML =  new html content</td>
    </tr>
    <tr>
        <td>attribute</td>
        <td>Change the attribute value of an HTML element</td>
        <td>element.attribute = new value</td>
    </tr>
    <tr>
        <td>style.property</td>
        <td>Change the style of an HTML element</td>
        <td>element.style.property = new style</td>
    </tr>
    <tr>
        <td>addEventListener</td>
        <td>Attaches an event handler to the specified element</td>
        <td>element.addEventListener(event, function, useCapture)</td>
    </tr>
    <tr>
        <td>appendChild</td>
        <td>Appends a node as the last child of a node</td>
        <td>node.appendChild(node)</td>
    </tr>
    <tr>
        <td>childElementCount</td>
        <td>Returns the number of child elements an element</td>
        <td>node.childElementCount</td>
    </tr>
    <tr>
        <td>childNodes</td>
        <td>Returns a collection of a node's child nodes</td>
        <td>element.childNodes</td>
    </tr>
    <tr>
        <td>children</td>
        <td>Returns a collection of an element's child elements, as an HTMLCollection object</td>
        <td>element.children</td>
    </tr>
    <tr>
        <td>classList</td>
        <td>Returns the class name(s) of an element</td>
        <td>element.classList</td>
    </tr>
    <tr>
        <td>click</td>
        <td>Simulates a mouse-click on an element</td>
        <td>HTMLElementObject.click()</td>
    </tr>
    <tr>
        <td>firstChild</td>
        <td>Returns the first child node of the specified node, as a Node object</td>
        <td>node.firstChild</td>
    </tr>
    <tr>
        <td>firstElementChild</td>
        <td>Returns the first child element of the specified element</td>
        <td>element.firstElementChild</td>
    </tr>
    <tr>
        <td>focus</td>
        <td>Give focus to an element</td>
        <td>HTMLElementObject.focus()</td>
    </tr>
    <tr>
        <td>getAttribute</td>
        <td>Returns the value of the attribute with the specified name, of an element</td>
        <td>element.getAttribute(attributename)</td>
    </tr>
</table>

> Change HTML content

***SYNTAX***
```javascript
document.getElementById(id).innerHTML = 'new HTML';
document.getElementsByClassName(className).innerHTML = 'new HTML';
...
```

***EXAMPLE***
```html
<div id="change-html-content"></div>
```
```javascript
//ex: show "Hello getElementById" text into div
document.getElementById("change-html-content").innerHTML = "Change HTML Content";
```

> Change value of an atrribute

***SYNTAX***
```javascript
document.getElementById(id).'attribute'  = 'new value';
document.getElementsByClassName(className).'attribute' = 'new value';
...
```

***EXAMPLE***
```html
<img id="change-value-attribute" />
```
```javascript
//ex: show "Hello getElementById" text into div
document.getElementById("change-value-attribute").src = "https://www.w3schools.com/js/pic_htmltree.gif";
```

> Change HTML style

***SYNTAX***
```javascript
document.getElementById(id).style.'property'  = 'new style';
document.getElementsByClassName(className).style.'property' = 'new style';
...
```

***EXAMPLE***
```html
<div id="change-property" >Change color of the text</div>
```
```javascript
//ex: show "Hello getElementById" text into div
document.getElementById("change-property").style.color = "blue";
```

> Action Events

***SYNTAX***
```javascript
document.getElementById(id).'onActionEvent'  = 'function';
document.getElementsByClassName(className).'onActionEvent'  = 'function';
...
```

***EXAMPLE***
```html
<button type="button" id="myBtn">Click Me</button>
```
```javascript
//ex: change the text of the button
document.getElementById("myBtn").onclick = function() {
    this.innerHTML = "You clicked on me";
}
```

---
***NOTE***
[See more action events](https://www.w3schools.com/jsref/dom_obj_event.asp)
---