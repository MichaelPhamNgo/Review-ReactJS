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
  - [See more action events](#see-more-action-events)

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

<table>
    <tr>
        <th>Method</th>
        <th>Description</th>
        <th>Syntax</th>
    </tr>
    <tr>
        <td>getElememtById [Click Here]</td>
        <td>Find an element by element id</td>        
    </tr>
    <tr>
        <td>document.getElementsByTagName</td>
        <td>Find elements by tag name</td>        
    </tr>
    <tr>
        <td>document.getElementsByClassName</td>
        <td>Find elements by class name</td>        
    </tr>
    <tr>
        <td>document.querySelector</td>
        <td>Find a selector</td>        
    </tr>
    <tr>
        <td>document.querySelectorAll</td>
        <td>Find all selectors</td>
        <td>document.querySelectorAll(selectors)</td>
    </tr>
</table>

#### getElememtById
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

#### getElementsByTagName
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

#### getElementsByClassName
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

#### querySelector
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

#### querySelectorAll
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
    <tr>
        <td>getAttributeNode</td>
        <td>Returns the attribute node with the specified name of an element, as an Attr object</td>
        <td>element.getAttributeNode(attributename)</td>
    </tr>    
    <tr>
        <td>id</td>
        <td>The id property sets or returns the id of an element</td>
        <td>HTMLElementObject.id</td>
    </tr>
    <tr>
        <td>innerText</td>
        <td>Sets or returns the text content of the specified node, and all its descendants</td>
        <td>node.innerText</td>
    </tr>
    <tr>
        <td>insertBefore</td>
        <td>Inserts a the specified element into a specified position</td>
        <td>node.insertAdjacentElement(position, element)</td>
    </tr>
    <tr>
        <td>insertAdjacentHTML</td>
        <td>Inserts a node as a child, right before an existing child, which you specify</td>
        <td>node.insertBefore(newnode, existingnode)</td>
    </tr>
    <tr>
        <td>lastChild</td>
        <td>Returns the last child node of the specified node, as a Node object</td>
        <td>node.lastChild</td>
    </tr>
    <tr>
        <td>lastElementChild</td>
        <td>Returns the last child element of the specified element</td>
        <td>element.lastElementChild</td>
    </tr>
    <tr>
        <td>matches</td>
        <td>Returns a Boolean value indicating whether an element is matched by a specific CSS selector or not</td>
        <td>element.matches(selectors)</td>
    </tr>
    <tr>
        <td>nextSibling</td>
        <td>Returns the node immediately following the specified node, in the same tree level</td>
        <td>node.nextSibling</td>
    </tr>
    <tr>
        <td>nextElementSibling</td>
        <td>Returns the element immediately following the specified element, in the same tree level</td>
        <td>node.nextElementSibling</td>
    </tr>
    <tr>
        <td>nodeName</td>
        <td>Returns the name of the specified node</td>
        <td>node.nodeName</td>
    </tr>
    <tr>
        <td>nodeValue</td>
        <td>Sets or returns the node value of the specified node</td>
        <td>node.nodeValue</td>
    </tr>
    <tr>
        <td>outerHTML</td>
        <td>Sets or returns the HTML element and all it's content, including the start tag, it's attributes, and the end tag</td>
        <td>element.outerHTML</td>
    </tr>
    <tr>
        <td>outerText</td>
        <td>Sets or returns the text content of the specified node</td>
        <td>node.outerText</td>
    </tr>
    <tr>
        <td>parentNode</td>
        <td>Returns the parent node of the specified node, as a Node object</td>
        <td>node.parentNode</td>
    </tr>
    <tr>
        <td>parentElement</td>
        <td>Returns the parent element of the specified element</td>
        <td>node.parentElement</td>
    </tr>
    <tr>
        <td>previousSibling</td>
        <td>Returns the previous node of the specified node, in the same tree level</td>
        <td>node.previousSibling</td>
    </tr>
    <tr>
        <td>previousElementSibling</td>
        <td>Returns the previous element of the specified element, in the same tree level</td>
        <td>node.previousElementSibling</td>
    </tr>
    <tr>
        <td>remove</td>
        <td>Removes the specified element from the DOM</td>
        <td>node.remove()</td>
    </tr>
    <tr>
        <td>removeAttribute</td>
        <td>Removes the specified attribute from an element</td>
        <td>element.removeAttribute(attributename)</td>
    </tr>
    <tr>
        <td>removeAttributeNode</td>
        <td>Removes the specified attribute from an element, and returns the removed attribute, as an Attr Node object</td>
        <td>element.removeAttributeNode(attributenode)</td>
    </tr>
    <tr>
        <td>removeChild</td>
        <td>Removes a specified child node of the specified element</td>
        <td>node.removeChild(node)</td>
    </tr>
    <tr>
        <td>removeEventListener</td>
        <td>Removes an event handler that has been attached with the addEventListener() method</td>
        <td>element.removeEventListener(event, function, useCapture)</td>
    </tr>
    <tr>
        <td>removeEventListener</td>
        <td>Removes an event handler that has been attached with the addEventListener() method</td>
        <td>element.removeEventListener(event, function, useCapture)</td>
    </tr>
    <tr>
        <td>replaceChild</td>
        <td>Replaces a child node with a new node</td>
        <td>node.replaceChild(newnode, oldnode)</td>
    </tr>
    <tr>
        <td>setAttribute</td>
        <td>Adds the specified attribute to an element, and gives it the specified value</td>
        <td>element.setAttribute(attributename, attributevalue)</td>
    </tr>
    <tr>
        <td>setAttributeNode</td>
        <td>Adds the specified attribute node to an element</td>
        <td>element.setAttributeNode(attributenode)</td>
    </tr>
    <tr>
        <td>tagName</td>
        <td>Returns the tag name of the element</td>
        <td>element.tagName</td>
    </tr>
    <tr>
        <td>textContent</td>
        <td>Sets or returns the text content of the specified node, and all its descendants</td>
        <td>node.textContent</td>
    </tr>
    <tr>
        <td>title</td>
        <td>Sets or returns the value of the title attribute of an element</td>
        <td>HTMLElementObject.title</td>
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