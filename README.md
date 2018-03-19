# Dom manipulation

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
