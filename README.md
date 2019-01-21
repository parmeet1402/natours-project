# Advanced CSS Notes

## Images
|Property|Use-case|Values|
|--------|--------|------|
|clip-path|Allows to crop the image|polgon(x1,y1,x2,y2....), circle(), ellipse(), _URL referencing SVG_, inset()[_could help to crop out image_] |
## Positioning or Layout
|Property|Use-case|Values|
|--------|--------|------|
|background-size|Helps to change the background size|cover, contain, width height|
|background-position| Makes sure the background always stick to either top, bottom or center. |top, bottom, center|

_TIPS_
1. __background-size: cover__  
    Makes the background size same as viewport size.

1. __clip-path: inset()__  
    Helps to crop out image.

1. __Setting text background as a a gradient__  
    1. First we need to set the background as a gradient.  
            `background-image: linear-gradient(to right, $color-primary-light, $color-primary-dark);`

    2. Then we would use background clip property to be only visible where the text is present.  
            `-webkit-background-clip: text;`             
    2. In Order to see the effect we need to change the text color to transparent.  
            `color: transparent;`