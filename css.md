<h1>CSS info</h1>

CSS Selectors

***Simple / Tag*** - 

p { color: green; }

***Class*** - Classes can be defined and used in any element.

.coffeeType { color: green; }

***ID*** - IDs can be defined and only used for one element on any given html page.

#siteHeader { color: green; }

***Combined selector*** - 

p.coffeeType { color: yellow; }

***Descendant selectors*** - an element at any level that is within the initial (e.g.; .coffeetype) selector

.coffeetype a { color: red; }

***Child selectors*** - an element at the direct next level after the selector element

.coffeetype > a { color: red; }

***Pseudo classes*** - 
a:link { color: blue; }
a:visited { color: red; }
a:hover {color : green;}
a:active { color: red; }

***Pseudo elements*** - p:first-child { color: red; }
