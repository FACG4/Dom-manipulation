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

Returns an item in the list by its index, or null if the index is out-of-bounds; can be used as an alternative to simply accessing nodeList[idx] (which instead returns undefined when idx is out-of-bounds).

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

## JAVASCRIPT EVENTS:

**An JAVASCRIPT event can be something the browser does, or something a user does.**

## Here are some examples of HTML events:

* An HTML web page has finished loading

* An HTML input field was changed
* An HTML button was clicked
  Often, when events happen, you may want to do something.

**JavaScript lets you execute code when events are detected.**

**HTML allows event to handler attributes, with JavaScript code, like add new text or replace text ... etc.**

## Can take this format:

```
<element event='some JavaScript'>
```

event like onClick, hover, right click, ... etc.
**Example:**

```
<button onclick="document.getElementById('demo').textContent = Date()">The time is?</button>
```

## event.preventDefault():

As it's name, it's prevent the default action of the event to be excute.

**For examples:**

* click on anchors will not take the browser to a new URL.
* Clicking on a "Submit" button, prevent it from submitting a form.

**Code example:**

```
<body>
<a href="http://jquery.com">default click action is prevented</a>
<div id="log"></div>
<script>
$( "a" ).click(function( event ) {
  event.preventDefault();
  document.getElementById("log").innerHTML = "New Paragraph";
});
</script>

</body>
```

## InnerHTML:

The **innerHTML** property is part of the Document Object Model (DOM) that allows Javascript code to manipulate a website being displayed, like add text or replace it in specific elements u choose.

DOM manipulations using innerHTML are slower and failure-prone.

## Security of innerHTML:

innerHTML is unsecure, why? if the API is unreliable or has been injected with an malicious code, innerHTML can edit the whole HTML.

it’s mean the hackers can accessible to the whole html that specialy for programmer.

**Notice:** The risk lies when the website contains input box for the visitors of the site as i under stand i'm not sure.

**InnerHTML Examples:**

```
document.getElementById("demo").innerHTML = "Paragraph changed!";

The output :  Paragraph changed!

document.getElementById("demo").innerHTML = "<h1>Paragraph changed!</h1>";

The output: Paragraph changed!    With H1 property.
```

## what could you use instead?

There are many Document Object Model better than innerHTML, like, **textContent and createElement**.

TextContent Examples:

```
    document.getElementById("demo").textContent = "<h1>paragraph changed</h1>";

The output: <h1>paragraph changed</h1>   it considered any thing between “ ” text without parse it.
```
