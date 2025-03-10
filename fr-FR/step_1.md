Les fonctions DOM (document object model) sont un ensemble d'outils utilisés pour manipuler dynamiquement le contenu, le style et la structure des documents Web à l'aide de JavaScript.

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

In this example, an HTML element uses an attribute `id="copyrightYear"`. L'élément avec ce sélecteur est ensuite modifié (sa propriété innerText est modifiée).

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

Dans cet exemple, plusieurs éléments HTML contenaient le même attribut `class="hero-slide"` et une liste de ces éléments est renvoyée par la fonction. La liste est ensuite utilisée dans le code.
