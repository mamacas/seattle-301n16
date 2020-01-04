# CSS Floats


## Property Overview

+ 'Float' is a positioning property that enables us to place content on one side of the page while allowing it to remain within the page flow. It can be used to create whole layouts, or simply to allow for text flow around images and other section dividers.

+ It is different from absolute positioning because when content is positioned absolutely, it is removed from the flow of the page.

+ It is different from fixed positioning because the content does not scroll along with the page (that would mean it would be removed from the flow of the page).


## Values

```
float: left;
float: right;
float: none;
float: inherit;
```

+ Left: floated content will snap to the left of the page and other content will flow around it

+ Right: floated content will snap to the right of the page and other content will flow around it

+ None: ensures the content will not float

+ Inherit: content assumes the float value of its parent element


## Clear

```
clear: both;
clear: left;
clear: right;
clear: none;
```

+ By default, when an element (i.e. a paragraph) is floated, the elements that come after it (i.e. a footer) will snap upwards and float adjacent to it. 

+ By using the 'Clear' property, we allow elements that follow floated elements to position themselves below the floated elements (so that our footer doesn't snap up and right-adjacent to our left-floated paragraph, but rather lies on the bottom of the page like we want it to).

+ Clear has four properties:

     * Both (clears floats from both directions)

     * Left (clears the left-float)

     * Right (clears the right-float)

     * None (used to remove clear values from cascade, but generally not
       used otherwise).

## Common Issues & Solutions

+ Pushdown: occurs when an element inside of a floated element is wider than the float itself. Most browsers will render the element outside of the float, but sometimes the wide element sticks out over the edge of the float, and pushes other elements down, affecting page layout. To solve this, use ```overflow: hidden; ``` which hides excess pixels.

+ Double Margin Bug: occurs when you apply a margin on the same direction as a float. To solve this, use ```display: inline;```. The float will remain a block element, but this is a quick fix.

+ 3px Jog: occurs when text that is next to a floated element is pushed away by 3px. To solve, set a width or height (whichever is needed) to the text. 

+ Bottom Margin Bug: occurs when a floated parent element has floated children elements and the bottom margins of the children elements are ignored. To fix, add bottom padding to the parent element.