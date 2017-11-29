<h1>CSS info</h1>

CSS Selectors

***Simple / Tag*** - 

p { color: green; }

***Class*** - Classes can be defined and used in any element.

.coffeeType { color: green; }

***ID*** - IDs can be defined and only used for one element on any given html page.

#siteHeader { color: green; }

***Combined*** - 

p.coffeeType { color: yellow; }

***Descendant*** - an element at any level that is within the initial (e.g.; .coffeetype) selector

.coffeetype a { color: red; }

***Child*** - an element at the direct next level after the selector element

.coffeetype > a { color: red; }

***Attribute selector*** - selects based on attribute value

img[alt=spacer] {
  padding:0px;
}

***Pseudo class*** - Set based on condition. Not explicitly set but are inherent based on condition.

a:link { color: blue; }

a:visited { color: red; }

a:hover {color : green;}

a:active { color: red; }

***Pseudo elements*** - p:first-child { color: red; }

___________________________

The user.css (from the person's browser) will be overridden by the style.css from the site unless the user.css has selectors which indicate "!important". 

body {
  font-size: 150%; !important;
}

