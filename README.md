``` 
                      Introduction to CSS
 ``` 
 # CSS INTRODUCTION
 ● CSS stands for Cascading Style Sheets

● CSS describes how HTML elements are to be presented on screen

● CSS can control the layout of multiple web pages all at once

● Includes adding visuals like color, fonts, layouts, etc.

The syntax for CSS is:

selector {
properties;
}

Each property ends with a semicolon.
Each property includes a CSS property name and a value, separated by a colon.

Below is an example, to see how CSS modifies the HTML
 code:
```<h1>Welcome to All!</h1>```

```<h2>Where coding is a way of life..</h2>```

Now, adding CSS to the above HTML code:

h1 { font-family: monospace; }

h2 { color: blue; }

# CSS COMMENTS
Just like HTML, CSS also contains comments and can be used to define the various sections
of HTML element styles that can help in changes at later stage, easily. You can also describe
where certain generic style(s) can be used.
A CSS comment starts with

 /* and ends with */. 

 Comments can also span multiple lines.

 ADDING CSS TO HTML PAGE
The browser formats the HTML document based upon the information in the stylesheet. The
browser access the stylesheets from the HTML document itself. 

There are 3 ways to add CSS

styles in your document. Each of them can contain multiple properties:

● Inline styles

● Internal styles

● External styles

Cascading order defines which style will be applied to element when multiple styles are used.

Cascading order priority: Inline > ( internal≅ external ) > browser default.

The internal and external CSS are treated equally by the browser. But the order of their
definition decides which one’s property will get preference.

If link to external CSS is defined before the internal CSS, then properties of internal CSS will
get the preference, i.e internal CSS > external CSS.

If link to external CSS is defined after the internal CSS, then properties of external CSS will get
preference over internal CSS, i.e. external CSS > internal CSS.

# Inline styles
Inline stylesheet is applied directly to our HTML code using the style attribute. The
inline stylesheet syntax contains properties written inside the style attribute.
Multiple properties can be defined at a time.
An inline style is used to apply a unique style for a single element.
You can use inline styles like this:

```<p style="color:blue;font-size:40px">Inline CSS</p>```


# Internal styles
An internal or in-page stylesheet holds the CSS code for the web page. The internal
stylesheet contains the styles for that HTML document only. They cannot be reused.
Internal CSS can be applied using ```<style> ```tag inside the <head> tag.
You can use internal styles like this:
```
<style>
h1 { color:blue; }
h2 { color:red; }
p { color:green; }
</style>
 ```


 # External styles
With an external stylesheet, you can change the look of an entire website by
changing just one file. The syntax is similar to internal stylesheets, but it is applied
using a complete different CSS file. It is saved with '.css' extension. Eg. 'styles.css'.
To use external stylesheet, a reference is provided to file inside the ```<link>``` element:
```<link rel="stylesheet" type="text/css" href="styles.css">```
The rel defines the relationship with the linked document(here, favicon).
The href defines the location of the lined document(here, favicon).
The type defines the media type of the linked document(here, favicon)

NOTE: The ```<link> ```element goes inside the ``` <head>``` section. The 'styles.css' contains
the CSS syntax code only.

# SELECTORS
Selectors point to the HTML element which we want to style. We use selectors in internal
and external stylesheets. There are mainly 3 types of selectors that are used to apply styles:

● Element selector

● Class selector

● Id selector

Specificity here defines which style will be applied when same multiple styles are applied to
an element. If the specificity is same, then the latest rule is applied.
Specificity order: inline > id selector > class selector > tag selector > browser default.
NOTE: If same property is defined inside the same type of selector, then the property which is
defined at the last, will be used by the browser.

# Element Selector
The element selector selects all elements with the specified element name. This will
select all the elements in the HTML document. But most of the time we don't want
this. So, to apply styles to only some elements we need to use some restrictions.
We will look into this later in this section only.
Syntax: element { css declarations; }
Eg., applying style to h2 tag like this:
```<h1>Blue Color</h1>```
and applying css like this:

h1 { color: blue; }


# Class Selector
The class selector selects multiple elements with a specific class attribute. To select
elements with a specific class, write a period(.) character, followed by the name of
the class.

Syntax:
 ```.class-name {css declarations; }```


 To use the class selector, the class attribute is used in the element's opening tag.
The value of the class attribute contains the name of the class. There can be
multiple classes added to the tag by giving a space in between.

Eg., defining the classes in the HTML file like this:

```<p class="red">I am red1</p>
<p class="blue right">I am blue1</p>
<p class="red">I am red2</p>
<p class="blue right">I am blue2</p> ```

and applying css like this:

.red { color:red; }
.blue { color:blue; }
.right { text-align:right; }

```

# Id Selector
The id selector selects only one element with a specific id attribute. To select
element with a specific id, write a hash(#) character, followed by the name of the id.
Syntax: ``` #class-name {css declarations; }```
To use the id selector, the id attribute is used in the element's opening tag. The
value of the id attribute contains the name of the id. There can only be one id in the
tag. The id is unique in a HTML page. If another element is given the same id, the
styles would not be applied by the browser.


```
Eg., defining the ids in the HTML file like this:

<p id="one">This is id one!</p>
<p id="two">This is id two!</p>
<p id="three">This is id three!</p>
<p id="four">This is id four!</p>

and applying css like this:

#one { color: blue; }
#two { background-color: teal; }
#three { color: green; }
#four { background-color: lightgrey; }

```

# Grouping Selectors
It is most of the time that we use same css for multiple elements and we can't use
too much classes. This would bring classes without any meaning in the scenario and
would become difficult to manage.
So, CSS provides with a grouping feature where you can apply CSS rules to multiple
elements with the use of combination of either tag, class or id. For grouping, we use
comma between the different selectors.
These are the few examples how you can use grouping:

● ```p, .class-name { CSS properties }``` - apply styles to 'para' and element
with class as 'class-name'

●``` #id1, #id2, span { CSS properties } ```- apply styles to 'span' and
elements with ids as 'id1'and 'id2'

● ```.class-name, #id1, div { CSS properties } -``` apply styles to 'div' and
elements with class 'class-name' and id as 'id1'

# Nesting Selectors
There are times when we want to target elements inside a specific section of HTML
page. So, instead of the using the classes we can use nesting that works like a
hierarchy and is easy to understand.
To use nesting, use a space between the selectors such that the sequence
represents a hierarchy, starting from top.
These are the few examples:

● ```.class-name span { CSS declarations } ```- apply styles to only those
'span', which are inside the element with class 'class-name'

● ```#id1 .class-name span { CSS declarations } ```- apply styles to only
those 'span', which are inside the element with class 'class-name' and 'classname'
is inside the element with id 'id1'

# Chaining Selectors
There are a times when we have(or want to have) same class for multiple elements
and we want to apply style/s to one/some of them. Then we can use chaining

selectors.
To use chaining we use the combination of selectors without any space in between
them.
Eg., we have a class 'header-style' applied to every heading. We can apply different
styles to them like this:

```h1.header-style { CSS declarations }```

```h2.header-style { CSS declarations }```

``` 
            Styling With CSS
```

# COLOR
The color property is used to set the foreground color of an element's text context and its
decoration.
The color property can be specified in 6 different ways. Each one of them provides has some
difference from the other. Although color can also be applied to backgrounds and borders,
we will discuss them later.

```
Eg. the following code:

<h2 style="color:orangered;">orangered</h2>
<h2 style="color:#ff6347;">#ff6347</h2>
<h2 style="color:rgb(255, 99, 71);">rgb(255, 99, 71)</h2>
<h2 style="color:hsl(9, 100%, 64%);">hsl(9, 100%, 64%)</h2>
<h2 style="color:rgba(255, 99, 71, 0.7);">rgba(64, 213, 240, 0.5)</h2>
<h2 style="color:hsla(9, 100%, 64%, 0.7);">hsla(190, 73%, 95%, 0.5)</h2>

```
# By name
All modern browsers support 140 different colors named in CSS. Unlike HTML, CSS
will completely ignore unknown keywords.
The color keywords all represent plain, solid colors, without transparency.

 Eg.orangered, green, blue, lightgrey, etc.

 # Using rgb
RGB stands for Red, Green and Blue. It is a color model where combination of red,
green and blue form a color. The intensity of each color has value ranging from 0 to
255. This provides very large number of colors dataset.

Eg.the RGB value for black is: rgb(0, 0, 0) and for white is: rgb(255, 255,
255).

# By hex code
The colors can be represented by 6 digits hexadecimal code. The codes are made
using the 3 colors(Red, Green and Blue). First 2 digits are red, next 2 are green and
last 2 are blue. So, the syntax for hex code is: #RRGGBB.
For each hexadecimal value between 00 - FF is similar to 0 - 255.

Eg., #000000 is black and #FFFFFF is white.

# Using hsla
HSLA (Hue, Saturation, Lightness, Alpha) is also an extension of HSL, provided with
alpha transparency. The alpha value and property is same as that in RGBA.

Eg., hsla(0, 100%, 50%, 0.6) is also a red color with 0.6 opacity and have same
color:

# CSS UNITS
CSS units are used for expressing size of different properties.
The units are expressed by a number followed by the unit symbol. Many CSS properties
take "length" values, such as width, margin, padding, font-size, border-width, etc.

Eg. 10px, 2em, 50% etc.

# A whitespace cannot appear between the number and the unit.
If the value is 0, the unit can be omitted.
For some CSS properties, negative lengths are allowed. Eg. margin
There are two types of length units: absolute and relative

# Absolute Units
The absolute units a fixed size/length of the element. Absolute length units are not
recommended for use on screen, because screen sizes vary so much.

The absolute units consist of the following:

● cm - centimeters

● mm - millimeters in inches (1in = 96px = 2.54cm)

● px - pixels (1px = 1/96th of 1in)

● pt - points (1pt = 1/72 of 1in)

● pc - picas (1pc = 12 pt)


# Relative Units
Relative length units specify a length relative to another length property.

Some of the relative units are the following:

● em - Relative to the font-size of the element (2em means 2 times the size of
the current font)

● rem - Relative to font-size of the root element

● vw - Relative to 1% of the width of the browser window size

● vh - Relative to 1% of the height of the browser window size

● % - Relative to the parent element

# BORDER
The border property is used to set element's border. CSS borders allows you to specify the
style, width, and color of an element's border.
Border is a shorthand for border-width, border-style, and border-color written together.

Eg., applying border property to a div like this:

``` 
border: 5px solid red;
```
# Border Width
The border-width property specifies the width of the four borders.
The width can be set as absolute or relative size or by using one of the three
predefined values: thin, medium, or thick.

Eg., border-width: 2px 10px 4px 20px;, 

will have top border of 2px, right
border of 10px, bottom border to 4px and left border to 20px

# Border Style
The border-style property specifies what kind of border to display.
The values for border-style are: dotted, dashed, solid, double, groove, ridge, inset,
outset, none, hidden.

Eg., border-style: dotted dashed solid double;, will have dotted top border,
dashed right border, solid bottom border and double lined left border.

```
NOTE: It is necessary to add border-style property else no other border properties
will work
```


# Border Color
The border-color property specifies the color of the four borders.
The value of the property is same as that of the color property. But now you can
provide different color to different border sides.
If border-color is not set, it inherits the color of the element.
```
Eg., border-color: red green;
```

will have top and bottom border color red and
left and right border color green.

# Border Individual Sides
Using the border property, we are able to provide width, style and color to all the
borders separately but still we have to give some value to all the sides of the border.
CSS border also have property to give border value separately to each of the border
sides. 

The border property for the sides are:

● border-top

● border-right

● border-bottom

● border-left

This is further broken to provide style, width and color separately to the border
sides. Some of them are: border-top-style, border-right-width, border-left-color,
etc.

# Border Radius
The border-radius property is used to add rounded borders to an element. You can
give absolute(eg. in px) or relative(eg. in %) value to this property.

Eg., if we add border-radius: 10px; property to the first border example, will
show like:

# The border-radius can be provided in elliptical form as well. Therefore, you need to
provide horizontal and vertical radius differently. This is done using a slash ("/")
between horizontal and vertical radius. Here is an example:
```
div {
border-radius: 30px/10px; /* horizontal radius / vertical radius */
background: teal;
width:20%;
height:20%;
padding:40px;
}
```

# TEXT AND FONT STYLING
Various properties are provided to change the look and style of text in the HTML document.
These styles will apply only to content of any element that is text. We will look into some of
the mostly used text and font styling properties.
Font properties define the look of the font like font family, boldness, size and style. The first
4 are font properties.
Text properties define the layout and presentation of the text in the HTML page.

# font-size
This defines the size of the text. The font-size value can be an absolute, or relative
size, i.e., values can be applied in px, %, em, etc.

Eg., h1 { font-size: 30px; } h2 { font-size: 1.875em; }

# font-family
The font family of a text is set with the font-family property.
The font-family property should hold several font names as a "fallback" system. If
the browser does not support the first font, it tries the next font, and so on.
Start with the font you want, and end with a generic family, to let the browser pick
a similar font in the generic family, if no other fonts are available.

```
Eg. h1 { font-family: sans-serif, monospace, serif; }
```

NOTE: If the name of a font family is more than one word, it must be in quotation
marks, like: "Times New Roman".

# font-style
The font-style property specifies the style for a text. The values for this property
are: normal, italic, oblique, initial, inherit

# color
We have already discussed applying color to text using the color property. The color
can be defined either by name, hex code, rgb, rgba, hsl, or hsla.

# text-align
The text-align property is used to set the horizontal alignment of a text.
A text can be aligned left, right, centered, or justified.

```
Eg.,
p#center { text-align: center; }
p#left { text-align: left; }
p#right { text-align: right; }
```
# text-indent
The text-indent property specifies the indentation of the first line in a text-block.
Negative values are allowed. The first line will be indented to the left if the value is
negative.

```
Eg., <p style="text-indent: 100px;">
```

Don’t you just love exploring beautiful
and neat sites with a clean user interface? While most of us would reply
with an assertive ‘YES,’ little, do we know.</p>


# text-transform
The text-transform property is used to specify the case of the letters in a text.

It can be used to turn text to:

● uppercase - turns every character to uppercase

● lowercase - turns every character to lowercase

● capitalize - turns first letter of each word to uppercase and other to lowercase

● none - text renders as it is. It is the default

# text-decoration
The text-decoration property is used to set or remove decorations from text.
The value text-decoration: none; is often used to remove underlines from links.
The text-decoration is used to decorate text. It has 4 values:

● underline - puts a line under the text

● overline - puts a line above the text

● line-through - puts a line through the text

● none - removes any of the above decorations

```
Eg.,
h3#underline { text-decoration: underline; }
h3#line-through { text-decoration: line-through; }
h3#overline { text-decoration: overline; }
```

# line-height
The line-height property sets the height of the lines in an element. It does not
change the size of the font.
The font-size value can be an absolute, or relative size, i.e., values can be applied in
px, %, em, etc. If no unit specified then it is multiplied by element’s font-size.

Eg., h3 { line-height:1.5; }

# letter-spacing
The letter-spacing property is used to specify the space between the characters in
a text. This is used to increase or decrease the space between the characters only.
The value of letter-spacing can be absolute or relative.

```
Eg., h3 { letter-spacing: 0.5em; }
```
# word-spacing
The word-spacing property is used to specify the space between the words in a text.
This is used to increase or decrease the space between the words.
The value of word-spacing can be absolute or relative.

```
Eg., h3 {word-spacing: 10px; }
```
# text-shadow
The text-shadow property adds shadow to text.
The value contains 3 values, which are position of the horizontal shadow, the
position of the vertical shadow and the color of the shadow.

Eg., h2 { text-shadow: 2px 1px red; }

# BACKGROUND
The background properties are used to define the background effects for elements. The
background of an element is the total size of the element and includes padding and border
but not the margin.
Backgrounds can be filled with a color or image, clipped or resized, and otherwise modified.

CSS background properties:

● background-image

● background-repeat

● background-position

● background-attachment

● background-size

```
body {
background-image: url("static/img.png
"), lineargradient(#
a3f7ff, #fff58e);
background-repeat: repeat-x;
background-position: center center;
background-attachment: fixed;
}
```
# background-color
The background-color property sets the background color of an element. It has the
same value as that of the color property.
Eg.,

``` <p style="background-color: #afcbff;">```

 Don’t you just love exploring
beautiful and neat sites with a clean user interface? While most of us would
reply with an assertive ‘YES,’ little, do we know. 
```</p>```

# background-image
The background-image property is used to specify an image to use as the
background of an element.
This can set one or more background images for an element.
By default, a background-image is placed at the top-left corner of an element, and is
repeated so it covers the entire element both vertically and horizontally.
The values it can take are:

● url('URL') - specifies the URL of the image. You can specify more than one
image by separating the URLs with a comma

● none - this is default value. No background image will be displayed

● linear-gradient() - sets a linear gradient as the background image. At least two
colors needed to be mentioned (default direction is top to bottom)

● radial-gradient() - sets a radial gradient as the background image. At least two
colors needed to be mentioned (default is from center to edges)

● repeating-linear-gradient() - repeats a linear gradient

● repeating-radial-gradient() - repeats a radial gradient

In the above example, we are using both the image and linear-gradient together.
Try to swap the sequence of image and gradient and see what happens

# background-repeat
The background-repeat property is used to specify how/if a background image will
be repeated.
By default, a background image repeats both vertically and horizontally, so
background-repeat will how will the image repetition works.
The values this property can take are:

● repeat - this is default value. The background image is repeated both vertically
and horizontally. The last image will be clipped if it does not fit

● repeat-x - the image is repeated only horizontally

● repeat-y - the image is repeated only vertically

● no-repeat - the image will only be shown once

● space - the background-image is repeated without clipping. The space
remaining is distributed evenly between images with first and last images
pinned to sides of the element

● round - the image is repeated and shrink or stretch to fill the space

# background-position
The background-position property is used to specify the initial position of a
background image.
By default, a background image is placed at the top-left corner of an element and
you can change the position with background-position property.

By default, a background image is placed at the top-left corner of an element and
you can change the position with background-position property.
The values this property can take are(X represents horizontal position and Y
represents vertical position):

● X Y - they both can each take value from one of the following - left, right, top,
bottom, center. If one value is specified, the other value will be "center"

● Xpos Ypos - specifies the horizontal and vertical position relative to the
viewport. Units can be any of the CSS units. If you only specify one value, the
other value will be 50%.

# background-attachment
The background-attachment property is used to specify whether a background
image scrolls with the rest of the page, or is fixed.

The values it can take are:

● scroll - this is default value. The background image will scroll with the page

● fixed - the background image will not scroll with the page

● local - the background image will scroll with the element's contents

# MARGIN
The CSS margin properties are used to create space between the borders and the other
surrounding elements.
You can also provide negative margins as well.
There are two other values that are used for the margin:
auto - the margin is applied by the browser itself only to horizontal margins

none - to remove any margins from the element or makes the value of margin equal to zero
Just like the border property, you can provide margins separately to the sides. The margin
property for the sides are:

● margin-top

● margin-right

● margin-bottom

● margin-left

```
Eg. for the below HTML code:
<div class="blue-box"><div class="orange-box">This is div</div></div>
and applying the following CSS to the code:
.blue-box {
border: 3px solid black;
background-color: skyblue;
} .
orange-box {
border: 1px solid black;
margin:25px 50px;
text-align: center;
background-color: orange;
}
```

NOTE: When two elements are positioned vertically, then the top and bottom margins of
elements are collapsed into a single margin that is equal to the largest of the two
margins. Margin can contain negative values.

# PADDING
The CSS padding properties are used to generate space around an element's content, and
its borders.
Just like the border property, you can provide margins separately to the sides. The margin

property for the sides are:

● padding-top

● padding-right

● padding-bottom

● padding-left

```
Eg. for the below HTML code:
<div class="blue-box"><div class="orange-box">This is div</div></div>
```

and applying the following CSS to the code:
```
.blue-box {
border: 3px solid black;
background-color: skyblue;
} .
orange-box {
border: 1px solid black;
margin:25px 50px;
padding: 10px 0 20px 0;
text-align: center;
background-color: orange;
}
```

# DISPLAY
The display property is a very important CSS property for controlling layout. It specifies
if/how an element is displayed.
Many of the elements have default display property value as inline or block (inline and block
elements in HTML).
The display property has following values:

● inline

● block

● inline-block

● none

# Inline Display
When display: inline; is used these following happens to the element:

● element doesn't starts in a new line

● only takes up as much width as necessary, so cannot set height and width

● the vertical margins do not work

```
making the list inline:

li { display: inline; }

and the list will now be shown in a single line like this(the space before the list is
because ul element have a default padding value
```

# Block Display
When display: block; is used these following happens to the element:

● element starts in a new line

● takes up full-width of the parent element
```
Eg., originally the 2 spans look like this:

<span>The quick brown fox</span> <span>jumps over the lazy dog!</span>

adding the block property to them like this:
li { display: block; }
```

# Inline-block Display
display: inline-block; is a combination of the properties of the inline and block
elements. These are the advantages of inline-block:

● height and width of the element can be set now

● vertical margins are allowed

● element can sit next to each other

There is a space between the elements next to each other
```
Eg., there are two empty div element:

<div class="div"></div>
<div class="div"></div>
and the following properties have been applied to them:
.div {
display: inline-block;
border: 1px dashed black;
width: 100px;
height: 100px;
background-color: lightgrey;
}
```
You can notice a space between these 2 divs. It is because inline elements have a
word-spacing in them and it is also a default in inline-block elements.

# No Display
The ``` display:none; ```property hides the elements in a browser. It actually removes
the element from the HTML page and nothing is shown in its place.
This is similar to another property - ```visibility:hidden;``` The difference is that the
element is not removed from the page and still occupies the space.

# POSITION
The position property is for specifying the positioning of element on the page. This fixes the
position of element relative to web page or parent element.
The position property provides 5 ways to position the element

● static - default

● relative

● absolute

● fixed

● sticky

This property is not enough to manipulate the position of the element. The position property
just specifies the behaviour. Therefore, to move the elements
 
 we have these 4 properties:

● left - shifts the element with respect to the left side of the element

● right - shifts the element with respect to the right side of the element

● top - shifts the element with respect to the top side of the element

● bottom - shifts the element with respect to the bottom side of the element

The above properties, i.e. left, right, top and bottom have numerical values in both relative
and absolute units. The value can be both positive and negative.

They also work differently depending on the position value.

```Eg., for the layout like this:
<div class="outer">
<h2>POSITION property</h2>
<span class="inner">This is relative to viewport</span>
</div>
```

and making div’s position relative with css code like:

```
.outer {
position: relative;
width: 250px;
height: 150px;
border: 1px solid red;
padding: 10px;
} .
inner {
border: 1px solid blue;
padding: 5px;
top: 10px;
left: 40px;
}
```
# static
The static value positions the element according to the normal flow of the page
and not in any special way. This is the default property.
Properties like top, right, bottom, left do not work when this is used.
You can alternatively use ``` position: static;``` 

# relative
The relative value positions the element relative to its first positioned (i.e. not
static) ancestor element. It is similar to the static value, but now the properties like
top, right, bottom, left will work on the element.
The original position of the element remains occupied.
Use ```position: relative;``` 

# absolute
The absolute value positions the element relative to its closest positioned ancestor.
If there is no positioned ancestor, then the position would be relative browser's
window.
The element doesn't occupy its original space.
Use ```position: absolute;``` 

# sticky

The sticky value is initially positioned as in the HTML source. It is then fixed
relative to the viewport as soon as it reaches the desired position.

A sticky element toggles between relative and fixed, depending on the scroll
position. It is positioned relative until a given offset position is met in the viewport -
then it "sticks" in place (like position:fixed).

Use position: sticky; to apply this property and the layout initially be same as
that of relative positioned and moves with the page on scrolling until the final
position (i.e. same as fixed position) is reached.

# BOX MODEL
Box model describes the layout of the elements. The HTML elements are considered as
boxes.
The CSS box model is essentially a box that wraps around every HTML element. It consists
of: margins, borders, padding, and content. The image below illustrates the box model

The total width of the element is equal to the total of the horizontal margin, border and
padding, and content width of element.
The total height of the element is equal to the total of the horizontal margin, border and
padding, and content height of element.

# MIN/MAX WIDTH

Width property is used to set the width of the element, to a specific size. But the size of the
becomes fixed with this and this brings problem of in smaller devices. The browser then gets
a scrollbar to scroll through the entire content.

So, to overcome this problem, CSS provides max-width property. This specifies the
maximum width that an element can have. If the browser window's width becomes smaller
than the width of the element, the element width adjusts with the browser width.

But, a very small element is very difficult to read. So, another property min-width is
provided by the CSS that specifies the minimum width that the element can have.

```
Eg., we have two divs like this:

<div id="div1">
<div id="div2">This example shows how the max and min width property
works.</div>
</div>
and the CSS is applied to them:
#div1{
background-color:lightgrey;
} #
div2 {
max-width: 400px;
min-width:300px;
}

```

# OVERFLOW
The overflow property is used to specify what happens if the content of an element
overflows, i.e. the content’s height or width is larger than element’s height or width.
This property adds a scroll-bar or clips the content when an element's content is too big to
fit in a specified area.

The values that the overflow property can take are:

● visible -this is default value. The content overflows and seen outside the box

● hidden - only the content that fits inside the box is visible and the overflow is
clipped

● scroll - all the content is visible through a scroll-bar added to the box

● auto - a scroll-bar gets added if content overflows

```
with fixed height and width as:

div {
background-color: aliceblue;
width: 200px;
height: 200px;
overflow: scroll;
}
```

NOTE: The overflow property only works for block elements with a specified height.