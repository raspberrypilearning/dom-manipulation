DOM (Document Object Model) functions are a set of tools used to manipulate the content, style and structure of web documents dynamically using JavaScript.

These methods enable developers to manipulate a document while the code is running. 

Here are some examples you may have used in your projects:

+ querySelector(selector): Returns the first element that matches the specified CSS selector.
    var element = document.querySelector(".myClass");

--- code ---
---
language: js
filename: script.js
line_numbers: true
---
     // Update Copyright Year function 
     const currentYear = new Date();
     document.querySelector("#currentYear")
    
--- /code ---

In this example, the HTML element contains an attribute `id=currentYear"` therefore this was passed through the function to find it.

+ querySelectorAll(selector): Returns a list of all elements that match the specified CSS selector.
    var elements = document.querySelectorAll("p.myClass");

--- code ---
---
language: js
filename: script.js
line_numbers: true
---

// Place Hero slider variables here 
let currentHeroIndex = 0;
const heroSlides = document.querySelectorAll('.hero-slide');
  
--- /code ---

In this example, multiple HTML elements contained the same attribute `class="hero-slide"`. Therefore this selector was passed through the function to find all the HTML elements.

Here are some other DOM functions you may come across:

+ getElementById(id): retrieves an element by its id attribute.
    var element = document.getElementById("myElement");

+ getElementsByClassName(className): Returns a collection of elements with the given class name.
    var elements = document.getElementsByClassName("myClass");

+ getElementsByTagName(tagName): Returns a collection of elements with the given tag name.
    var paragraphs = document.getElementsByTagName("p");

+ addEventListener(event, callback): Attaches an event listener to an element.
    element.addEventListener("click", function() {
        console.log("Element clicked!");
    });

   