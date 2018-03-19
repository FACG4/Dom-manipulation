# Dom-manipulation
### How can you use JavaScript to create an HTML element and then add it to your webpage? How would you replace an existing element with it?
  *** 1. How can you use JavaScript to create an HTML element and then add it to your webpage?***
* first : creates a new element (e.g ```<h1>```).
* ```var newElement = document.createElement("h1");```

* add text
*  ```var text = document.createTextNode("This Is New");```

*  append the text node to the ```<h1>``` element:
* ``` newElement.appendChild(text);```

* select the place where the element should be added before:

* ```  var place = document.getElementById("p1");```
*  appends the new element to the existing element
* ``` place.insertBefore(newElement,place);```

*** 2. How would you replace an existing element with it?***

first : creates a new element (e.g ```<p>```).
* ```var newElement = document.createElement("p");```

* add text
*  ```var text = document.createTextNode("This is a new paragraph");```

*  append the text node to the ```<p>``` element:
* ``` newElement.appendChild(text);```

select the place where the element should be replaced:

* ```  var replaced = document.getElementById("replacedID");```

* replace it with new Element :

* ```replaced.replaceWith(newElement);```

## How would you add a ```<li>``` element to the start of a ```<ul>```?
first : creates a new element (```<li>```).
* ```var newli = document.createElement("li");```

* add text
*  ```var text = document.createTextNode("Your text Here...");```

*  append the text node to the ```<li>``` element:
* ``` newli.appendChild(text);```

select the **ul** where the **li** should be added:

* ```  var ulElement = document.getElementById("ulID");```

*  appends the new **li** to the  **ul**
* ``` ulElement.appendChild(newli);```
## What is nodeList ?

**this expression is old
and the apdate of it is html collection
The node list is an array with no ability to use the array method for it : (push , slice etc ..)**


_This line will explain the idea :_
```
var nodeList = document.getElementsByClassName('className');
             = document.querySelectorAll('');
```
[More about querySelectorAll](https://www.w3schools.com/jsref/met_document_queryselectorall.asp)



It will return a list of all tags or elements that have the same classes and it will be nodeList not array
or " all of nodes that have the similer name of class"

_To be clear :_

DOM is a collection of nodes .. and if we want to get a specific node we can get the nodeList then get the chile of this list by 'childNodes'

_We can convert nodelist to array :_

```
var myArray = Array.prototype.slice.call(myNodeList);
```

### Methods
**NodeList.item()**

Returns an item in the list by its index, or null if the index is out-of-bounds; can be used as an alternative to simply accessing nodeList[idx] (which instead returns  undefined when idx is out-of-bounds).

**NodeList.entries()**

Returns an iterator
 allowing to go through all key/value pairs contained in this object.

**NodeList.forEach()**

Executes a provided function once per NodeList element.

**NodeList.keys()**

Returns an iterator allowing to go through all keys of the key/value pairs contained in this object.

**NodeList.values()**

Returns an iterator allowing to go through all values of the key/value pairs contained in this object.

_The differences between NodeList and array_
* We can create array programatically but the nodeList connot .
* The methods they provide .
* The element in Array is arr[i] ,
   in NodeList is NodeList.item(i);
* [To more differences](https://toddmotto.com/a-comprehensive-dive-into-nodelists-arrays-converting-nodelists-and-understanding-the-dom/#browser-support)
