CSS Positioning

***Fixed*** positioning ’fixes‘ the position of an element relative to the browser window. The element always stays fixed in 
place, even when scrolling.

```
.blueBox {
    background: #627da0;
    position: fixed;
    top: 0px;
    left: 0px;
}
```
(pins it to the top right corner of the window)

***Absolute*** positioning takes an element out of document flow, meaning the browser acts as if the element has no width and 
height, and the other elements on the page move up as if it was never there. The position of the element is then fixed 
relative to the top level container, or the closest parent with a set positioning.

```
.blueBox {
    background: #627da0;
    position: absolute;
    top: 0px;
}
```
(pins it to the top right corner of the page)

***Relative*** positioning sets the position of an element relative to its original position. The element's original width and 
height is retained in document flow and other elements behave as if it was in its original position.

```
.blueBox {
    background: #627da0;
    position: relative;
    bottom: 20px;
}
```

***Static*** positioning is the default behavior of elements.

```
.blueBox {
    background: #627da0;
    position: static;
}
```

***Inherited*** positioning tells an element to inherit its positioning from its parent element. 

***Z-index*** controls the vertical stacking order of elements. Elements must have a set positioning for z-index to work.

```
.blueBox {
    background: #627da0;
    position: relative;
}

.greenBox {
    background: #5b8054;
    position: relative;
    top: -150px;
    z-index: -1; 
}
```

Float and Clear
The float will allow elements to wrap around it although this does not apply to multiple img elements. If one img element has a float=left attribute and the other does not, the one that does not will just slide up and under the floated element.

Clear will ignor the designated float and kick the text (or next element) to the next line - like a break tag.

```
.blueBox {
    background: #627da0;
    float: left;
}

.greenBox {
    background: #5b8054;
    float: left;
}

h1 {
    clear: both;
}
```
