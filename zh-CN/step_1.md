DOM（文档对象模型）函数是一组使用 JavaScript 动态操作 Web 文档的内容、样式和结构的工具。

以下是你可能在项目中使用过的一些示例：

- `querySelector(selector)`：返回与指定 CSS 选择器匹配的第一个元素。

--- code ---
---
language: js
filename: 
line_numbers:
---
     // 更新版权年份函数 
     const currentYear = new Date().getFullYear();
     document.querySelector("#copyrightYear").innerText = currentYear

--- /code ---

在此示例中，HTML 元素使用属性 `id="copyrightYear"`。 然后，具有此选择器的元素将被改变（其 innerText 属性将被更改）。

- `querySelectorAll(selector)`：返回与指定 CSS 选择器匹配的所有元素的列表。

--- code ---
---
language: js
filename: 
line_numbers:
---

// 更改 Hero 函数
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

--- /code ---

在这个例子中，多个 HTML 元素包含相同的属性 `class="hero-slide"`，并且该函数返回这些元素的列表。 然后在代码中使用该列表。
