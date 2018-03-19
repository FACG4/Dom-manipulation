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
