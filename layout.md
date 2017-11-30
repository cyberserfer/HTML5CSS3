# Layout

positioning - relative, fixed and absolute

relative - set position relative to the element's starting point

fixed - set position in window regardless of page elements. The item will always be displayed where you put it in the window.

absolute - set position on the page regardless of other page elements

float attribute allows text to wrap around the floated container (e.g.; an image)

clear has the ability to stop the wrap created by float. e.g.; you just want the image explanation to the right of the image and do not want the next paragraph creaping up.

```
#figure1 {
  float: left;
  margin-right: 5px;
}

.clear {
  clear: both;
}
```

## Columns

To create column you set margin(s) to the right/left of a container.

margin-left: 400px; When applied to the css this will create a margin of 400px to the left of the element it was applied to.

 <- 400px ->[container element]

 <- column->[     column 2    ]
 
 3 column layouts are sort of the Holy Grail of CSS. They are often problematic.
 
