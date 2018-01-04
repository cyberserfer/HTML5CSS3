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

"*" a=0 b=0 c=0 -> specificity = 0 

"LI" a=0 b=0 c=1 -> specificity = 1 

"UL LI" a=0 b=0 c=2 -> specificity = 2 

"LI.re"d a=0 b=1 c=1 -> specificity = 11 

"#content" /* a=1 b=0 c=0 -> specificity = 100

Finally, an "inline style" will have the highest weight and will take precedence over all.

http://www.css3.info/modules 
 
CSS structure 
 
Tag name   p {color:green;} 
Class name    .coffeeType {color:green;} 
Element ID    #siteHeader {color:green;} 
Combined Selector p.coffeeType {color:yellow;} 
Child Selector    .coffeeType a {color:red;} 
                             .coffeeType  > a {color:red;}  (child of) 
Pseudo Classes   a:link {color:red;} 
                              a:visited {color:red;} 
Pseudo Elements    p:first-child{color:red;} 
 
 
CSS Box Model 
Margin ---------------------- 
|    Border ------------------ 
|     |   Padding ------------- 
|     |    |     Content ------- 
|     |    |       | 
 
New input types 
Color 
Email 
Number 
Range 
Search 
Tel 
Url 
Date, datetime, datetime-local, time, week, month 
 
Validation Attributes 
Maxlength 
Pattern (use regx) 
Required 
Max 
Min 
Placeholder (puts an example in box) 
Novalidate (on form tag) 
Formnovalidate (on form element tag) 
 
Selectors are broke into 3 groups 
Attribute selectors 
Pseudo Classes 
Pseudo Elements 
 
"Starts with" selector ->    ^ 
E.g.; [href ^= "https"] 
 
"Ends with" selector ->   $ 
E.g.; [href $= "store"] 
 
"Contains" selector ->    * 
E.g.; [href *="blog"] 
 
Pseudo Classes 
:nth-child     e.g.; p:nth-child(2n)  this will select even number items 
:nth-last-child   this counts from last element  e.g.; p:nth-last-child(2)  this will return the 2nd from last  
:nth-of-type 
:last-child 
:only-child 
:not  this is an inverse selector 
:out-of-range 
 
DOM 
 getElementById 
 getElementsByName 
 getElementsByTagName 
 getElementsByClassName 
 
Borders & Backgrounds 
 border-radius: 20px;  rounds corners 
 background-size: % or px; 
 background-origin:         identifies where to place upper left corner of image 
 background:url(image1.jpg), url(image2.jpg);   this will stack images 
 
Gradients 
 background:linear-gradient(orange, green);  this will gradient orange to green from top to bottom 
 background:linear-gradient(to right, orange, green); this will gradient right to left 
 background:linear-gradient(to bottom right, orange, green);  this will gradient from top left to bottom right 
 
Radial Gradients 
 background: radial-gradient(yellow, orange, red); 
 background: radial-gradient(yellow 10%, orange 20%, red 70%); 
 
Transforms 
 transform: rotate(45deg); 
                     skew(30deg, 20deg); 
                     matrix            this is a combo of transforms 
 
CSS Animations 
 
 @keyframes homeAnimation { 
0% {background:green; left:0px; top:0px;} 
25% {background:brown; left:200px; top:0px;} 
50% 
75% 
100% 
 } 
NOTE: the % will equal times in the sequence 
 
USED 
 
 div { 
Animation: homeAnimation:10s; 
} 
@keyframes homeAnimation { 
0% {background:green; left:0px; top:0px;} 
25% {background:brown; left:200px; top:0px;} 
50% 
75% 
100% 
 } 
 
Animation Properties 
 @keyframes 
 animation-name 
 animation-duration 
 animation 
 animation-fill-mode 
 animation-play-state 
 animation-delay 
 animation-iteration-count 
 animation-timing-function 
 
Text Effects 
 
 text-shadow: 5px 5px 5px #ffffff; 
Which means: text-shadow: horizontal verticle blur color; 
 
Fonts (HF, OTF, WOFF, SVG are supported) 
 font-face { 
font-family: headerFont; 
src: url(sansation_light.woff); 
} 
USED 
 div { 
Font-family: headerFont; 
} 
 
Multi colunm 
<style> 
.multicol { 
column-count: 3;  (no notation = em) 
column-gap: 40px; 
} 
</style> 
USED 
<div class="multicol"> …… </div> 
 
Drag & Drop 
Attributes 
 draggable="true" 
 dropzone="copy" 
 
Events 
 ondragstart 
 ondrag 
 ondragenter 
 ondragover 
 ondragleave 
 ondrop 
 ondragend 
 
Data transfer object  (workhorse of drag & drop) 
Properties: 
 dropEffect 
 files 
 types 
 
Methods 
 setData 
 getData 
 clearData 
 setDragImage 
 addElement 
