# Table of React JS content

- [Table of React JS content](#table-of-react-js-content)
- [I. Single Page Application vs Multiple Page Application](#i-single-page-application-vs-multiple-page-application)
- [I.1 Single Page Application](#i1-single-page-application)
- [I.2 Multiple Page Application](#i2-multiple-page-application)
- [II. JS HTML DOM](#ii-js-html-dom)
  - [II.1 Finding HTML Elements](#ii1-finding-html-elements)
    - [getElememtById](#getelememtbyid)
    - [getElementsByTagName](#getelementsbytagname)
    - [getElementsByClassName](#getelementsbyclassname)
    - [querySelector](#queryselector)
    - [querySelectorAll](#queryselectorall)
  - [II.2 Actions on HTML elements](#ii2-actions-on-html-elements)
    - [innerHTML](#innerhtml)
    - [style.property](#styleproperty)
    - [addEventListener](#addeventlistener)
    - [appendChild](#appendchild)
    - [childNodes](#childnodes)
    - [children](#children)
    - [classList](#classlist)
    - [className](#classname)
    - [focus](#focus)
    - [getAttribute](#getattribute)

# I. Single Page Application vs Multiple Page Application 
# I.1 Single Page Application 
A Single Page Application (SPA) is a web application implementation that loads only a single web document, and then update the body content of that single document via JS APIs such as XMLHttpRequest and Fetch.

# I.2 Multiple Page Application
A Multiple Page Application (MPA) is the traditional web applications that reload the entire page and displays the new one when a user interacts with the web app. Each time when a data is exchanged back and forth, a new page is requested from the server to display in the web browser.

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

### getElememtById
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

### getElementsByTagName
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

### getElementsByClassName
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

### querySelector
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

### querySelectorAll
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

***NOTE***
<table>
    <tr>
        <th>Method</th>
        <th>Description</th>        
    </tr>
    <tr>
        <td>getelememtbyid</td>
        <td>Find an element by element id</td>        
    </tr>
    <tr>
        <td>getelementsbytagname</td>
        <td>Find elements by tag name</td>        
    </tr>
    <tr>
        <td>getelementsbyclassname</td>
        <td>Find elements by class name</td>        
    </tr>
    <tr>
        <td>queryselector</td>
        <td>Find a selector</td>        
    </tr>
    <tr>
        <td>queryselectorall</td>
        <td>Find all selectors</td>        
    </tr>
</table>


## II.2 Actions on HTML elements

### innerHTML
> Change HTML content

***SYNTAX***
```javascript
// Set the innerHTML property:
HTMLElementObject.innerHTML = text

// Return the innerHTML property
HTMLElementObject.innerHTML;
```

***EXAMPLE***
```html
<div id="demo-innerHTML"></div>
```
```javascript
//ex: show "Hello innerHTML"
document.getElementById("demo-innerHTML").innerHTML = "Hello innerHTML";
```

### style.property
> Change HTML style

***SYNTAX***
```javascript
// Set style properties
element.style.property = value

// Return style properties
element.style.property
```

***EXAMPLE***
```html
<div id="demo-property" >Hello Property</div>
```
```javascript
//ex: show "Hello getElementById" text into div
document.getElementById("demo-property").style.color = "blue";
```

### addEventListener
> Adds an event handler to the specified element

***SYNTAX***
```javascript
element.addEventListener(event, function, useCapture)
```

***EXAMPLE***
```html
<button type="button" id="demo-addEventListener">Click Me</button>
```
```javascript
//ex: change the text of the button
document.getElementById("demo-addEventListener").addEventListener("click", function(){
    this.innerHTML = "Hello addEventListener";
});
```

### appendChild
> Appends a node as the last child of a node

***SYNTAX***
```javascript
node.appendChild(node)
```

***EXAMPLE***
```html
<button type="button" id="demo-appendChild">Add A Last Node</button>
<ul id="myList-appendChild">
    <li>Node 1</li>
    <li>Node 2</li>
</ul>
```
```javascript
//ex: add li node to ul#myList-appendChild
document.getElementById("demo-appendChild").addEventListener("click", function(){
    //create node li
    let node = document.createElement("li");
    //create text for li node
    let textNode = document.createTextNode("Node 3");
    //add text to li node
    node.appendChild(textNode);
    //add li to ul#myList-appendChild
    document.getElementById("myList-appendChild").appendChild(node);
});
```

### childNodes
> Show list of child nodes

***SYNTAX***
```javascript
element.childNodes
```

***EXAMPLE***
```html
<button type="button" id="demo-childNodes">Show list of child nodes</button>
<ul id="myList-childNodes">
    <li>Node 1</li>
    <li>Node 2</li>
</ul>
```
```javascript
//ex: show childNodes
document.getElementById("demo-childNodes").addEventListener("click", function(){
    console.log(document.getElementById("myList-childNodes").childNodes);       
    //NodeList(5) [text, li, text, li, text]
});
```

### children
> A collection of an element's child elements, as an HTMLCollection object

***SYNTAX***
```javascript
element.children
```

***EXAMPLE***
```html
<button type="button" id="demo-children">Show list of child nodes</button>
<ul id="myList-children">
    <li>Node 1</li>
    <li>Node 2</li>
</ul>
```
```javascript
//ex: show children
document.getElementById("demo-children").addEventListener("click", function(){
    console.log(document.getElementById("myList-children").children);       
    //HTMLCollection(2) [li, li]
});
```

### classList
> Show the class name(s) of an element, as a DOMTokenList object

***SYNTAX***
```javascript
element.classList
```

***Methods***
<table>
    <tr>
        <td>Method</td>
        <td>Description</td>
    </tr>
    <tr>
        <td>add(class1, class2, ...)</td>
        <td>Adds one or more class names to an element</td>
    </tr>
    <tr>
        <td>contains(class)</td>
        <td>Returns a Boolean value, indicating whether an element has the specified class name</td>
    </tr>
    <tr>
        <td>item(index)</td>
        <td>Returns the class name with a specified index number from an element. Index starts at 0</td>
    </tr>
    <tr>
        <td>remove(class1, class2, ...)</td>
        <td>Removes one or more class names from an element</td>
    </tr>
    <tr>
        <td>toggle(class, true|false)</td>
        <td>Toggles between a class name for an element</td>
    </tr>
</table>

***EXAMPLE***
```html
<button type="button" id="demo-classList">Add list css</button>
<div id="change-class">Add new style(s) for div</div>
```
```javascript
//ex: add css styles for div
document.getElementById("demo-classList").addEventListener("click", function(){
    document.getElementById("change-class").classList.add("style1", "style2");
});
```

### className
> Sets or gets the class name of an element

***SYNTAX***
```javascript
// Set the className property
HTMLElementObject.className = class
// Return the className property
HTMLElementObject.className
```

***EXAMPLE***
```html
<button type="button" id="demo-className">Add css</button>
<div id="change-classname">Add new style for div</div>
```
```javascript
//ex: change css
document.getElementById("demo-className").addEventListener("click", function(){
    document.getElementById("change-classname").className = "style1";
});
```

### focus
> Gives focus to an element

***SYNTAX***
```javascript
HTMLElementObject.focus()
```

***EXAMPLE***
```html
<input type="text" id="myText-focus">
<button type="button" id="demo-focus">Get focus</button>
```
```javascript
//ex: set focus
document.getElementById("demo-focus").addEventListener("click", function(){
    document.getElementById("myText-focus").focus();
});
```

### getAttribute
> Gets the value of the attribute with the specified name, of an element

***SYNTAX***
```javascript
element.getAttribute(attributename)
```

***EXAMPLE***
```html
<button type="button" id="demo-getAttribute">Get Attributes</button>
<div id="show-attribute"></div>
```
```javascript
//ex: show attribute
document.getElementById("demo-getAttribute").addEventListener("click", function(){
    var x = document.getElementById("change-class").getAttribute("class");
    document.getElementById("show-attribute").innerHTML = x;
});
```

***NOTE***

<table>
    <tr>
        <th>Property</th>
        <th>Description</th>        
    </tr>
    <tr>
        <td>innerHTML</td>
        <td>Change the inner HTML of an element</td>        
    </tr>    
    <tr>
        <td>style.property</td>
        <td>Change the style of an HTML element</td>        
    </tr>
    <tr>
        <td>addEventListener</td>
        <td>Attaches an event handler to the specified element</td>        
    </tr>
    <tr>
        <td>appendChild</td>
        <td>Appends a node as the last child of a node</td>        
    </tr>    
    <tr>
        <td>childNodes</td>
        <td>Returns a collection of a node's child nodes</td>        
    </tr>
    <tr>
        <td>children</td>
        <td>Returns a collection of an element's child elements, as an HTMLCollection object</td>        
    </tr>
    <tr>
        <td>classList</td>
        <td>Returns the class name(s) of an element</td>        
    </tr>
    <tr>
        <td>className</td>
        <td>Sets or returns the class name of an element</td>        
    </tr>        
    <tr>
        <td>focus</td>
        <td>Give focus to an element</td>        
    </tr>
    <tr>
        <td>getAttribute</td>
        <td>Returns the value of the attribute with the specified name, of an element</td>        
    </tr>
    <tr>
        <td>getAttributeNode</td>
        <td>Returns the attribute node with the specified name of an element, as an Attr object</td>        
    </tr>    
    <tr>
        <td>id</td>
        <td>The id property sets or returns the id of an element</td>        
    </tr>
    <tr>
        <td>innerText</td>
        <td>Sets or returns the text content of the specified node, and all its descendants</td>        
    </tr>
    <tr>
        <td>insertBefore</td>
        <td>Inserts a the specified element into a specified position</td>        
    </tr>
    <tr>
        <td>insertAdjacentHTML</td>
        <td>Inserts a node as a child, right before an existing child, which you specify</td>        
    </tr>
    <tr>
        <td>lastChild</td>
        <td>Returns the last child node of the specified node, as a Node object</td>        
    </tr>
    <tr>
        <td>lastElementChild</td>
        <td>Returns the last child element of the specified element</td>        
    </tr>
    <tr>
        <td>matches</td>
        <td>Returns a Boolean value indicating whether an element is matched by a specific CSS selector or not</td>        
    </tr>
    <tr>
        <td>nextSibling</td>
        <td>Returns the node immediately following the specified node, in the same tree level</td>        
    </tr>
    <tr>
        <td>nextElementSibling</td>
        <td>Returns the element immediately following the specified element, in the same tree level</td>        
    </tr>
    <tr>
        <td>nodeName</td>
        <td>Returns the name of the specified node</td>        
    </tr>
    <tr>
        <td>nodeValue</td>
        <td>Sets or returns the node value of the specified node</td>        
    </tr>
    <tr>
        <td>outerHTML</td>
        <td>Sets or returns the HTML element and all it's content, including the start tag, it's attributes, and the end tag</td>        
    </tr>
    <tr>
        <td>outerText</td>
        <td>Sets or returns the text content of the specified node</td>        
    </tr>
    <tr>
        <td>parentNode</td>
        <td>Returns the parent node of the specified node, as a Node object</td>        
    </tr>
    <tr>
        <td>parentElement</td>
        <td>Returns the parent element of the specified element</td>        
    </tr>
    <tr>
        <td>previousSibling</td>
        <td>Returns the previous node of the specified node, in the same tree level</td>        
    </tr>
    <tr>
        <td>previousElementSibling</td>
        <td>Returns the previous element of the specified element, in the same tree level</td>        
    </tr>
    <tr>
        <td>remove</td>
        <td>Removes the specified element from the DOM</td>        
    </tr>
    <tr>
        <td>removeAttribute</td>
        <td>Removes the specified attribute from an element</td>        
    </tr>
    <tr>
        <td>removeAttributeNode</td>
        <td>Removes the specified attribute from an element, and returns the removed attribute, as an Attr Node object</td>        
    </tr>
    <tr>
        <td>removeChild</td>
        <td>Removes a specified child node of the specified element</td>        
    </tr>
    <tr>
        <td>removeEventListener</td>
        <td>Removes an event handler that has been attached with the addEventListener() method</td>        
    </tr>
    <tr>
        <td>removeEventListener</td>
        <td>Removes an event handler that has been attached with the addEventListener() method</td>        
    </tr>
    <tr>
        <td>replaceChild</td>
        <td>Replaces a child node with a new node</td>        
    </tr>
    <tr>
        <td>setAttribute</td>
        <td>Adds the specified attribute to an element, and gives it the specified value</td>        
    </tr>
    <tr>
        <td>setAttributeNode</td>
        <td>Adds the specified attribute node to an element</td>        
    </tr>
    <tr>
        <td>tagName</td>
        <td>Returns the tag name of the element</td>        
    </tr>
    <tr>
        <td>textContent</td>
        <td>Sets or returns the text content of the specified node, and all its descendants</td>        
    </tr>
    <tr>
        <td>title</td>
        <td>Sets or returns the value of the title attribute of an element</td>        
    </tr>
</table>