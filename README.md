# Dom-manipulation

<!-- ramy -->

<!-- razan -->

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
