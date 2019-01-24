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

## Animation
|Property|Use-case|Values|
|--------|--------|------|
|backface-visibility|Helps determine whether the back of something is visible or not|hidden|
|animation-iteration-count|Allows ro run an animation more than once|_number_|
|animation-fill-mode|Allows to automatically apply properties of a keyframe|backwards[1st keyframe], forwards[Last keyframe], both|

## TIPS
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
1. __backface-visibility: hidden__  
    Used with animaitons to remove the shake or to hide the back of something (especially while dealing with 3d-rotations).
1. __text-align: center__  
    Could be used to center an inline-block element.
1. __Reason for using position: relative to the parent when using positon: absolute__  
    Because absolute positioning needs some reference to point to. 
1. __Declare root font size in percentage rather than pixels__   
    This will allow the users to change the font-size manually.
1. __Reset the after and before sudo elements[All*] too__  
    Along with the universal selector, also use before and after selectors to reset the margin and padding of the sudo elements as well.
----
# SASS/SCSS Notes

## Color Functions
|Property-name|use-case|values|
|-------------|--------|------|
|darken(color, percentage)| returns a darker color|base color & darkness percetage|
|lighten(color, percentage)| returns a lighter color|base color & lightness percentage|


## Mixins
|Property-name|use-case|values|
|-------------|--------|------|
|@mixin <mixin_name>(<arg1,arg2..>)|Creates a mixin with arguments|__CSS Code__|

1. Mixins could be imported using @include <mixin_name> command.