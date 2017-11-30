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

________________________________

Browser Developer Tools are able to expose how the DOM is being handled. This is helpful to determine things like which .css is being applied.

_______________

Cascade and Weight of selectors

The last .css listed will be the one for which its elements has precedence. 

The exception to this depends on "specificity" which is evaluated by the wieght of the selector. Selectors that have more specificity, based on the 3 items below, are given a higher weight and are used before those with a lesser weight.

a = Count of ID selectors

b = Count of class and attribute selectors

c = Count of type selectors

* a=0 b=0 c=0 -> specificity = 0 

LI a=0 b=0 c=1 -> specificity = 1 

UL LI a=0 b=0 c=2 -> specificity = 2 

LI.red a=0 b=1 c=1 -> specificity = 11 

#content /* a=1 b=0 c=0 -> specificity = 100


