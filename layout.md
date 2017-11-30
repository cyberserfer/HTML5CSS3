# Layout

positioning - relative, fixed and absolute

relative - set position relative to tje element's starting point

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
