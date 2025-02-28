DOM (document object model) functions are a set of tools used to manipulate the content, style, and structure of web documents dynamically using JavaScript.

Voici quelques exemples que tu as peut-être utilisés dans tes projets :

- `querySelector(sélecteur)` : renvoie le premier élément qui correspond au sélecteur CSS spécifié.

## --- code ---

language: js
filename:
line_numbers:
--------------------------------------------------

```
 // Mise à jour de la fonction Copyright Year 
 const currentYear = new Date().getFullYear();
 document.querySelector("#copyrightYear").innerText = currentYear
```

\--- /code ---

Dans cet exemple, un élément HTML utilise un attribut `id="copyrightYear"`. The element with this selector is then altered (its innerText property is changed).

- `querySelectorAll(sélecteur)` : renvoie une liste de tous les éléments qui correspondent au sélecteur CSS spécifié.

## --- code ---

language: js
filename:
line_numbers:
--------------------------------------------------

// Fonction Change Hero
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

In this example, multiple HTML elements contain the same attribute `class="hero-slide"` and a list of these is returned by the function. La liste est ensuite utilisée dans le code.
