DOM (document object model) functions are a set of tools used to manipulate the content, style, and structure of web documents dynamically using JavaScript.

Hier zijn enkele voorbeelden die je misschien al eerder hebt gebruikt in je projecten:

- `querySelector(selector)`: Retourneert het eerste element dat overeenkomt met de opgegeven CSS selector.

## --- code ---

language: js
filename:
line_numbers:
--------------------------------------------------

```
 // Bijwerken Copyright Jaar functie 
 const currentYear = new Date().getFullYear();
 document.querySelector("#copyrightYear").innerText = currentYear
```

\--- /code ---

In dit voorbeeld gebruikt een HTML-element een kenmerk `id=copyrightYear"`. The element with this selector is then altered (its innerText property is changed).

- `querySelectorAll(selector)`: Retourneert een lijst met alle elementen die overeenkomen met de opgegeven CSS-selector.

## --- code ---

language: js
filename:
line_numbers:
--------------------------------------------------

// Wijzig Hero functie
const heroSlides = document.querySelectorAll('.hero-slide');
var currentHeroIndex = 0;

function changeHero(direction) {

heroSlides[currentHeroIndex].classList.remove("active");
currentHeroIndex = currentHeroIndex + direction;

if (currentHeroIndex < 0){
currentHeroIndex = 2;
} else if (currentHeroIndex > 2) {
currentHeroIndex = 0;
}

heroSlides[currentHeroIndex].classList.add("active");

}

\--- /code ---

In this example, multiple HTML elements contain the same attribute `class="hero-slide"` and a list of these is returned by the function. De lijst wordt vervolgens in de code gebruikt.
