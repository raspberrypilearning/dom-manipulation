DOM (document object model) -functies zijn een reeks hulpmiddelen waarmee je de inhoud, stijl en structuur van webdocumenten dynamisch kunt manipuleren met behulp van JavaScript.

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

In dit voorbeeld gebruikt een HTML-element een kenmerk `id="copyrightYear"`. Het element met deze selector wordt vervolgens gewijzigd (de eigenschap innerText wordt gewijzigd).

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

In dit voorbeeld bevatten meerdere HTML-elementen hetzelfde kenmerk `class="hero-slide"`, en de functie retourneert een lijst hiervan. De lijst wordt vervolgens in de code gebruikt.
