# CSS - Cascading Style Sheet
inline css:- when we apply css to a specific element inside the html file.

internal css:- written inside <head> tag.

external css:- written in another file with extension .css


we use external css the most, because if we use internal, inline css most of the time, html code will get hard to read.
-> we can use same css file with multiple html files.

# selector:- 
1. element selector/ tag selector
2. id based selector - id must be unique
3. class based selector - class can be repeated, used for grouping.
4. group based selection
5. universal selector

# color:-
rgb(_,_,_) : these co-ordinates means that how much amount of red, green, and blue we are putting in our colour.

values: (0-255, 0-255, 0-255) = total memory
let rgb(127, 140, 209) = 8+8+8 = 24 bits i.e., 3 bytes memory
    another fourth value is introduced sometimes, which is the alpha that represents the transparency of the color.
    0- completely transparent 
        rgba (_,_,_,_)

background-color: hsl(hue (0-360), saturation (0-100%), lightness (0-100%))
    hue- the pure color itself
        this is the degree of the color wheel (0-360).
        0 is red.
        120 is green.
        240 is blue.
    
    saturation - intensity or vibrancy of the color.
        0% is gray.
        100% is most vivid version of that color.

    lightness - the brightness of the color.
        0% is black.
        50% is the normal color.
        100% is white.
    
    hsla (_,_,_,_)
we mostly use rgba setting for the color

we can aslo show this rgb value in hexadecimal form, i.e., the values starting with '#'

# font:-
    font-size (written in pixels, it is short for "picture element")
        pixel is the smallest controllable unit of a digital image or display screen.
            they are the tiny dots or squares arranged in a 2d grid that form all images, text, videos on screens, with each pixel holding a specific color and brightness value.
                1 pixel is 1/96 inch, but actually, you cannot measure pixel in cm or inches.

                for images, each color will have 3 bytes, so image will of pixel*3 bytes memory

                our mobile phone resolution is 16*9, when we click an image, it shows 1920*1080 pixel*3 bytes= 6mb.
                    as it depends on the screen, therefore there is actually no measure of pixel in inches or cm. 
    
    also written in 'em' that means it will take the size of its parent value.

    also written in 'rem' that means size of its root element i.e. the <html>

    also written in 'vw'. if '2vw' that means it will be 2% size of the width of the device

    also written in 'vh'

    also written in percentage unit, font-size: 50% means it will be half the size of its parent element

font-family
    we can also download fonts from 'google fonts' and link them to our html page
font-weight (100-900)
font-style

# CSS box model:
    content -> padding -> border -> margin

# inline vs block elements:
    inline -> <a>, <span> 
        -> only applies to the text and the same width of the text
        -> padding will only be applied horizontal
        ->margin will only be applied horizontal 

    block -> <div>, <h1>, <h2>, <p> 
        -> takes up the whole width when you apply css
        -> always start with a new line
        -> height, width can be applied 

    best of both worlds:- display:inline-block

    border-box = border-width + padding-width + content-width 
    content-box = content-width

# Cascade & Positioning:
priority : 
    inline -> internal -> external
        but this is not entirely true, because what matters here is the order.
            what comes later gets higher priority.
    
    how specific you go for the element:
        id has the highest priority than any class or tag.
    
    therefore, sequence goes-> 
        important, inline css, id, class, tag, ordering (when there's a tie)

    when you wish to override the sequence, and want external css to get higher priority than inline you mark it as '!important'

Positions:
    1. Static (by default)
    2. Relative ((doesn't let anyone else come there in its space))
    3. Fixed
    4. Sticky
    5. Absolute (relative to the nearest ancestor)

by default z-index of every element is 0

# Flexbox:
    used to make layout (1 dimensional)
    parent-child relation:
    parent is the container and the child is the item.

    axis: when flex-direction=row
       1. main axis - horizontal (justify-content always works around here)
       (flex-basis also works around this)
       2. cross axis - vertical (align-items work around here)

    you can practice using: flexbox froggy

# CSS Grid:
    used to make multi-dimensional layout
    making it using flexbox is possible but lengthy and complex

    it is just like creating a matrix
        works just like tables.
            just mention the rows and columns
            -> parent: grid-container
            -> items: grid-items

    to solve the problem of items over-riding the parent: fraction
        ->using this, the length is defined dynamically.

# Responsive website:
    one whose content and layout automatically adapt to fit any screen size, whether it's a desktop, tablet, or mobile phone, ensuring a consistent and optimal viewing experience for the user.
    -> done using flexible grids, CSS media queries

        it is like if, else situation:-
            -> if screen width>900{
                apply this css
            }
            else{
                apply this css
            }
        here, order matters

        default-configuration:
            can be either desktop-first or mobile-first
            -> in real-world, mobile-first configuration is used.

            but we can achieve the same thing using flexbox-wrap feature: why not use that then?

# box shadow:
    giving shadow behind a box to make it look like 3d and more attractive
    -> they are interpreted as <offset-x> and <offset-y> and its color.
    -> other two values are the 'blue-radius' and 'spread radius'
        box-shadow: 0px 0px 0px 20px blue;
            -> this means that increase the border shadow 30px from each side
    -> inset : so as to get the shadow starts to come on the inside of the box rather than outside (away from it)

# CSS Animation:
    CSS allows animation of html elements without using javascript.
    -> Animation lets an element gradually change from one style to another.
        ->It is the process of creating the illusion of motion by displaying a sequence of static images (frames) in rapid succession, making it appear as if the objects withim them are moving.

        -> video is stored in the system like: 30fps i.e., 30 frames per second:- meaning in one second, 30 images are being shown continuously making it look like they are moving.

    animation shorthand property can be used as well.

# Transitions:
    styling changes when you hover over an html element.

difference between transition and animation:
    animation works automatically whereas transition needs a trigger moment.

Tranforms:
    CSS tranforms property applies on 2D or a 3D element.
    it allows you to rotate, scale, move and skew elements. 
        we use this property so when a transformation is applied to one element, it doesn't affect the positioning of other elements.