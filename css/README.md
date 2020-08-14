# CSS

Cascading Style Sheet.
CSS is presentation lenguage that is used to modify the design of a web page.

* [First Steps](#First-Steps)
* [CSS Syntax](#CSS-Syntax)
* [Typografhy](#Typografhy)
* [Box Model](#Box-Model)
  * [Dimension](#Dimension)
  * [Box Sizing](#Box-Sizing)
* [Selectors](#Selectors)
  * [Descending](#Descending)
  * [Identifiers](#Identifiers)
  * [Classes](#Classes)
  * [Universal](#Universal)
  * [Child](#Child)
  * [Grouping](#Grouping)
  * [Adjacent](#Adjacent)
* [Pseudo Classes](#Pseudo-Classes)  
* [Backgrounds](#Backgrounds)
* [Measure Unit](#Measure-Unit)
  * [Absolute Measure Unit](#Absolute-Measure-Unit)
    * [Pixel](#Pixel)
  * [Relative Measure Unit](#Relative-Measure-Unit)
    * [Percentage](#Percentage)
    * [em](#em)
    * [rem](#rem)
* [Animations](#Animations)
  * [Transform](#Transform)
  * [Transitions](#Transitions)
  * [KeyFrames](#KeyFrames)
  * [Css Animations Libraries](#Css-Animations-Libraries)
  

## First Steps

In order to start with css we need first need to create some basic html document.

- `<link>` : This tag is going to help use to link our html file to our css file.

  - rel : In this atribute we describe that we are going to link a stylesheet document

  - type : The type of the linked file is going to be css

  - href : With this atribute we are going to say where is the linked file located.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Learning HTML</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>
  <body>
    <h1>Learning CSS</h1>
    <p>How to add a CSS in a HTML file.</p>
  </body>
</html>
```

## CSS Syntax

When we are writing css code we need to identify that there are three basic components in the structure.

- selector : One selectors could have more than one property. Also we could have multiples selectors.

- property : A property is a specific characteristic like font or color.

- value : Is the value that we a assign to each properties.

```css
selector {
    property: value;
    property: value;
}

h1 {
  font-family: Georgia, serif;
  font-size: 24px;
}
```

## Typografhy

When we are talking about typography is all about how it looks our text, the font, size and even the style, css give us some tools in order to modify the typography in our applications.

- font-family : With this property we can choose predefined typography styles, also we can send a list of values in where the highest priority is the left side, if the web page ist no able to use the element in the left side is going to move to the right side until one of those match.

```css
h1 {
    font-family: Arial, sans-serif, Helvetica;
}
```

- font-size : This property let us define the size of the typography.
  - px : It means pixel

```css
h1 {
    font-size: 16px;
}
```

- font-style: This property help us to define if we want that a specific text use italic style, also if we want a normal text we can set font-style as normal.

```css
h1 {
    font-style: italic;
}

h2 {
    font-style: normal;
}
```

- font-weight: This property tell us when a property could be bold("nregrilla") or not.

```css
h1 {
    font-weight: bold;
}

h2 {
    font-weight: normal;
}
```

- color: Let us define letter colors that we want to use.


```css
h1 {
    color: #ff0000;
}
```

- letter-spacing: It means the space between letters.

```css
h1 {
    letter-spacing: 3px;
}
```

- word-spacing: This property allow us to set a specific distance between words.

```css
h1 {
    word-spacing: 3px;
}
```

- line-height: Let us set a height for every line.

```css
h1 {
    line-height: 20px;
}
```

- text-align: This property allows to set the text to the right, center, left or justify.

```css
h1 {
    text-align: center;
}

h2 {
    text-align: left;
}

h3 {
    text-align: right;
}

h4 {
    text-align: justify;
}
```

- text-decoration: This property let us put one line under or in the middle of the text.

```css
h1 {
    text-decoration: underline;
}

h2 {
    text-decoration: line-through;
}
```

- text-transform: Let us convert a text into a uppercase, lowercase or capitalize (All the first letter are uppercase and other lowercase.).

```css
h1 {
    text-transform: uppercase;
}

h2 {
    text-transform: lowercase;
}

h2 {
    text-transform: capitalize;
}
```

## Box Model

Every single time that we write a tag in html this element draw a rectangule or box. This box has different parts:

- content: In the content is going to be our text.

![](https://github.com/andresmontoyab/Front-End/blob/master/css/resources/box-model.PNG)


- padding : Is the space between the content of the box and the external boundary. When
 
```css
h1 {
  padding: 30px;
}

h2 {
  padding-top: 20px;
  padding-right: 30px;
  padding-bottom: 40px;
  padding-left: 50px;
}

h3 {
  padding: 20px 30px 40px 50px;
}
```

 - border : Is the external boundary. Every border has three properties:

    - thickness : example 5px
    - type : example solid
    - color : the color of the border
    - all together -> border: 5px solid #ff0000

```css
p {
  border: 5px solid #ff0000;
}

h1 {
  border-top: 5px solid #ff0000;
  border-right: 5px solid #ff0000;
  border-bottom: 5px solid #ff0000;
  border-left: 5px solid #ff0000;
}
```

- margin : Space between one box and another box.

```css
p {
   margin: 10px 20px 0px 7px; // All the side in the order top, right, bottom and left
}

h1 {
   margin: 10px; // Apply for all the sides
}

h2 {
   margin: 10px 20px; // First number is for top and botton, second number is for left and right.
}

h3 {
  margin-top: 5px;
  margin-right: 5px;
  margin-bottom: 5px;
  margin-left: 5px;
}
```

### Dimension

In order to modify the size of our bos we can use the next two properties.

![](https://github.com/andresmontoyab/Front-End/blob/master/css/resources/widht-height.PNG)

```css
p {
  width: 100px;
  height: 50px;
}
```

### Box Sizing

This property allow us to specify if the size of our box is going to include the padding and border dimenstion or if the specified widht and height are the total of the box.

```css
p {
  box-sizing: content-box;
  box-sizing: border-box;
}
```

![](https://github.com/andresmontoyab/Front-End/blob/master/css/resources/box-sizing.PNG)

#### Boxing Properties

- max-width: Allow us to mark a max width for a box but this width is also variable.

```css
div {
  max-width: 800px;
}
```

- min-width: Allow us to mark a min widht for a box, but this width is variable.

```css
div {
  min-width: 800px;
}
```


- max-height: Allow us to mark a max height for a box but this height is also variable.

```css
div {
  max-height: 800px;
}
```

- min-height: Allow us to mark a min height for a box, but this height is variable.

```css
div {
  min-height: 800px;
}
```

- display: With this property we set up how we want to display our component.
  - block: If we setup the display property as block, the component is going to be displayed as a box (with content, margen, border and padding).
  - inline: This type flows like a text, so if the line finish the next value can continue in the next line.
  - inline-block: This proprety is a hybrid between the two above options, and basically are box but those can be next to next.
  - none: that means that the specific box are not going to be shown.

```css
div {
  display: block;
  display: inline;
  display: inline-block;
  display: none;
}
```

- border-radius: Is a property that let us modify the corner of the box and make it round

```css
h1 {
  border-radius: 3px;
}

h2 {
  border-radius: 5% 5% 10em 10em; // top-right, top-left, bottom-left, bottom-right
}
```

- box-shadow: this property let us add shadows to our boxes

```css
h1 {
  box-shadow: #000 10px 10px 0; // color movx movy blur
}

h2 {
  box-shadow: 10px 10px 5px #000;
}

h3 {
  box-shadow: #000 5px -7px 3px inset;
}
```

- text-shadow: this property let us add shadows to our texts

```css
h1 {
  text-shadow: 2px 5px 0 #f00;
}
```

## Selectors

### Descending

When we have nested tag in our html, we can specify those nested elements creting a descending selector.

```css
ul li{
    // Properties
}

ol li {
    // Properties
}
```

### Identifiers

If in our html we have a tag with "id" we can create a selector to only select the element with the specific id.

```html
<h1 id="main">
  Main Title
</h1>
```

```css
#main {
  color: #00ff00;
  font-size: 24px;
}
```

### Classes

If we want to have a spcific design for all the element that belongs to a class, we could use the operator "."

```css
.className {
    font-size: 18px;
}
```

### Universal

With the universal selector all the element inside our application are going to be affected.

```css
* {
  // .. properties here
}

#id * {
  // .. properties here
}
```

### Child

Child is very similar to the Descending selector, the only difference is that child(>) is just going to modify those element that are just one leve above, that means the children.

```css
ul>li {
  // .. properties here
}
```

### Grouping

Let's say that we have to selectors with the same style rules, in order to evade write multiple time the same code, we can group the selectors and apply the same rules.

```css
h4, p.destacado {
 // .. properties here
}
```

### Adjacent

If two elements are adjacent, we can create a selector that only is going to apply if those specific elements are adjacent.

```css
h1 + p {
   // .. properties here
}
```

### With Atribute

We can create selector that check the html atributes

- `[]` : Within this symbols we are going to write the specific atributes to check.
- `~` : Some atributes can have multiple values, with this symbol we check if some of those value match the value write in the selector.
- `|` : check if the atribute has the exact value or is after a `-`
- `^` : This symbol indicate if the atribute start with the value
- `$` : This symbol indicate if the atribute ends with the value
- `*` : This symbol indicate if the atribute contains the value

```css
a[href="http://www.google.com"] {
  background: #ff0;
}

a[class~="button"] {
  background: #eee;
  border-radius: 3px;
}

li[class|="nav"] {
  background: #eee;
}

a[href^="http://"] {
  background: #eee;
}

p[class$="-error"] {
  color: #f00;
}

a[class*="button"] {
  background: #ff0;
}
```

## Pseudo Classes

In order to use pseudo class we can use the symbol ":"  and there are multiples options.

```css
a {
  text-decoration: none;
}

a:link {
  color: #0000ff;
}

a:visited {
  color: #777777;
}

a:hover {
  text-decoration: underline;
}

a:active {
  font-weight: bold;
}
```

### first-child

If we want to style different the first child of a specific element, we can use this property.

```css
p:first-child {
   // .. properties here
}
```

### last-child

If we want to style different the last child of a specific element, we can use this property.

```css
p:last-child {
   // .. properties here
}
```

### lang

The pseudo-class lang means leanguage and help us to give style in base of the lenguage.

```css
p:lang(es) {

}
```

### focus

This pseudo class help us to identify where an specific element is being focused.

```css
input:focus {
  // properties.
}
```

### enabled

Sometimes in our webpages we want a different style of those element that are enabled, in order to do that we can use the pseudo class "enabled"

```css
input:enabled {
  // properties.
}
```

### disabled

Sometimes in our webpages we want a different style of those element that are disabled, in order to do that we can use the pseudo class "disabled"

```css
input:disabled {
  // properties.
}
```

#### nth-child

Previously we define the last-child and first-child pseudo class, the nth-child let us select the child in the position n and apply the style.

```css
p:nth-child(3) {
  font-size: 1.5em;
  color: #444;
}
```

#### first-line

This pseudo class let us modify just the first line of a text.

```css
p:first-line {
  font-size: 1.3em;
}
```

#### first-letter

This pseudo class let us modify just the first letter  of a text.

```css
p:first-letter {
  font-size: 1.3em;
}
```

#### not

This pseudo class let us exclude some element from our selectors.

```css
div:not(.contenedor) {
  font-size: 2em;
  color: #f00;
}
```

#### empty

The empty pseudo class let us modify an element only if this element is empty.

```css
div:empty {
  background-color: #000;
}
```

#### before

Let us add some specific content just before the element.

```css
h1:before {
  content: "- ";
  color: #888;
}

h2::before { // double : for pseudo element
  content: "- ";
  color: #888;
}
```

#### after

Let us add some specific content just after the element.

```css
h1::after {
  content: " -";
  color: #888;
}
```

## Backgrounds

There are several properties to modify the backgroung, in the next sections we are going to check it:

- background-color : With this property we are going to set a color for the background

```css
div {
  background-color: #ff0000;
}
```

- background-image : With this property we are going to set a specific image as background

```css
div {
  background-image: url("my_image.jpg");
}
```

- background-repeat : When we apply the property background-image the image is going to be repeated multiples times, in order to control that we can use this property

```css
.box1 {
  background-repeat: no-repeat; // With this value the image ist not going to repeated.
}
.box2 {
  background-repeat: repeat-x; // The image is going to be repeated horizontally
}
.box3 {
  background-repeat: repeat-y; //The image is going to be repeated vertically
}
```

- background-position: When we aplpied background-image and background-repeat as no-repeat the image is going to appear in the left top of the box, in order to set the position of the image inside the box we can use this property.
  - We can use the next key words like right, left, top, botton or center.
  - We can use pixeles in order to set the position

```css
.div {
  background-position: top center;
}
.p {
  background-position: 20px 10px;
}
```

## Measure Unit

### Absolute Measure Unit

The absolute measure unit are those unit in where the size is fixed and does not matter the devices in where you are seeing it.

#### Pixel

In css one of the most used absolute measure unit  is the pixel which symbol is "px".

```css
.p {
  width: 500px;
}
```

### Relative Measure Unit

Currently we have to create applications for multiples devices, in this scenarios is not recommended to use absolute measure unit because maybe some devices are to little or to big to support 300px, so in this cases we can use relate measure unit.

#### Percentage

The relative measure unit percentage is mark as "%" and basically means that the box is going to use the specific percentage avaiable in that box.

```css
h1 {
  width: 80%;
  margin-right: 25%;
  font-size: 200%; // This 200% means different, with font-size that means that the size is going to be the double of the in
}
```

There is another use of the percentage symbol and is related to the font-size, when we use the property font-size with %, the % is going to mean that the font size is the % of the inherited font size.

```css
body {
  font-size: 16px;
}
h1 {
  font-size: 200%; // 32px
}
h2 {
  font-size: 50%; // 16px
}
```

#### em

This relative measure unit depends only of the font-size. The em is always going to depend to the font-size

```css
body {
  font-size: 20px;
}

h1 {
  font-size: 2em; // 40px or 200% 
}

p {
  font-size: 24px;
  margin-top: 1em; /* 1 x 24 = 24px */
  margin-bottom: 1em; /* 1 x 24 = 24px */
}
```

#### rem

It means root em, the only difference with em is that rem is always going to depend to the root(html) font size and not of the relative box font size.

```css
html {
  font-size: 20px;
}
p {
  font-size: 1.2rem;
}
```

## Animations

### Transform

The transform property is going to help us to create animations, this property let us apply some movement to elements in order to make more frendly our interfaces. There are two things to keep in mind when we are using transform.
1. Everything is going to be position relative.
2. Transform modifies all the element.


- rotate: The subproperty rotate is going to rotate a specific amount of degrees our elements.
  - If our degrees are positives this is going to rotate to the right.
  - If our degrees are negatives this is going to rotate to the left.
  - If we want more than one turn, we can specified the amount of turns

```css
div:hover {
  transform: rotate(45deg);
}

h1:hover {
  transform: rotate(-45deg);
}

button:hover {
  transform: rotate(rotate(3.5turn));
}
```

- skew : It is a property that let us incline the element.
  - We can incline for both dimension x and y.  ex: skew(25deg, 30deg), that means that we are going to incline 25 degrees in x and 30 degres in y.

```css
div:hover {
  transform: skew(25deg,35deg);
}
```

- scale: this property let us increase the size of the elements.  

```css
div:hover {
  transform: scale(1.5); // scale x and y 1.5 times
}

button:hover {
  transform: scale(1.5, 2); // scale x 1.5 times and y 2 times
}
```
- translate: This property let us to move the element in x and y.

```css
button:hover {
  transform: translate(45px,20px); // move 45px in x and 20px in y
}
```

- transform-origin: usually when we use the property transform, the base point (x,y) is where the element is, with transform-origin we can move that initial point to another one.

```css
#element{
  transform-origin: bottom right;
}
#element:hover{
  transform: rotate(30deg);
}
```

#### Applying multiple properties in transform

If we want to apply multiples properties at the same time we can do it separating the properties by a space, it is important to keep in mind that the transformations are going to be applied in the left-right order that you wrote it.

```css
#elemento{
	transform: rotate(-15deg) skew(0, 25deg) scale(1, 0.5) translate(20px,10px);
}
```

### Transitions

 This property is very usefull when we are working with animations, basically we can indicate which property we want to animate and how many time should take the animation. There are few point that we kee in mind.
  - The transition property goes in the non-hover selector.
  - transition-property is the name of the property that we want to animate.
  - transition-duration is the time that the transition is going to take.

```css
#one { 
  background: #900;
  transition-property: background;
  transition-duration: 2s;
}
#one:hover {
  background: #009;
  border-radius: 50%;
}

a {
  background: #ff0000;
  transition: background 0.5s;
}
a:hover {
  background: #ff4444;
}

h1 {
  background: #ff0000;
  transition: all 500ms;
}
h1:hover {
  background: #ff4444;
}
```

#### Delay

Something we want that our transitions start after a few seconds, in order to make this happen we can use the dalay property.

```css
#element {
  transition-property: height;
  transition-duration: 2s;
  transition-delay: 3s;
}
#element:hover {
	height: 75px;
}
```

Something we have multiples transition wiht multiples delay, in order to combine multiple transition with those delays with can apply the next structure.
  - Keep in mind that when we are dealing with multiples delay you must keep in mind the delay of the previous transition.

```css
div {
  width: 200px;
  height: 200px;
  background-color: #900;
  color: white;
  line-height: 200px;
  text-align: center;
  margin: 50px auto;
}
#linea {
  line-height: 0px;
  transition-property: line-height, background-color, border-radius, border-radius;
  transition-duration: 3s, 2s, 1s;
  transition-delay: 0s, 3s, 5s;
}
#linea:hover{
  line-height: 200px; /* 3s*/
  background-color: #090; /* 2s*/
  border-radius: 50%; /* 1s*/
}
```

#### Acelerations

When we are dealing with transition usually all the movements are applied at the same speed but if we want to change that speed with time we need the conceptos acelarations. In order to do that css give a property called trasition-timing-function that let us change the speed.

- ease-out: faster at the beginning and with time gets slower
- ease-in: slow at the beginning and with time get faster.
- linear: it does not have any kind of change
- cubic-bezier: If you want to create custom movements you can use the function cubic-bezier

```css
#one {
  transform-origin: center left;
  transition-property: all;
  transition-duration: 1.2s;
  transition-timing-function: ease-out;
}
#one:hover {
  transform: scale(2.4,1);
  background: #ff6;
}
```

### KeyFrames

With keyframe we are able to create more complex animations than the transition, some of the differences with the transitions are:

1. I can divide an animations into multiples keyframes. So that means more rich animations
2. I dont need to way until the hover.
3. You can repeat keyframes but you're not able to repeat transitions

 ```css
 @keyframes color {
   from {
    background: blue;
  }
  to {
    background: violet;
  }
}
#color{
  width: 300px;
  height: 100px;
  text-align: center;
  line-height: 100px;
  animation-name: color;
  animation-duration: 2s;
  animation-timing-function: linear;
}
 ```

- animation-itearation-count: If you want to repeat a animation using keyframes you should use this property
  - If you put the value of "infinite" the animations is going to repeat infinite times.

```css
@keyframes color{
  0%{
    background: blue;
  }
  100%{
    background: violet;
  }
}

#color {
  animation-name: color;
  animation-duration: 2s;
  animation-iteration-count: 3;
}
```

- animation-direction : with keyframes we can set a specific direction of our animations, usually the animations start in 0% and goes to 100% but we can modifies that.
  - normal : Start in 0 % and goes to 100%
  - reverse : Start in 100 % and goes to 0%
  - alternate : Start in 0 % goes to 100% and after that 100% to 0%
  - alternate-reverse : Start in 100 % goes to 0% and after that 0% to 100%

```css
@keyframes rotate{
  100%{
    transform: rotate(360deg);
  }
}

#rotar {
  animation-name: rotate;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-direction: alternate-reverse;
}
```

- play-state: We can stop the animation when the user put the click in the element(hover) using the play-state property.

```css
@keyframes rotate {
  100%{
    transform: rotate(360deg);
  }
}
#rotar {
  animation-name: rotate;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-direction: reverse;
  animation-play-state: paused;
}
#rotar:hover {
  animation-play-state: running;
}
```

- fill-mode : This property help us to define, what happens when the animations finish, there are two options.
  - forwards : After the animation finish our element is going to keep the last keyframe (100%)
  - backwards : After the animation finish our element is going to keep the first keyframe (0%)

### Css Animations Libraries

There are some already created library with some animations that can helps to create a web page with animations faster, some of those are:

1. Animate CSS
2. CSS Shake
3. Wow.js

## Preprocessor

SASS and LESS are pre-processors that can help us to write similar css code that is easy to mantain in the future.

### Sass

Sass is a preprocessor scripting language that is interpreted or compiled into Cascading Style Sheets

- compilers : The compiler let us to process our Sass code and transform into CSS code
  - ruby: Ruby provide us a cli-compiler, so in order to start with this guide you are going to need to install ruby in your machine.
  - gui: prepros,codekit, scout are options to compile sass code into css code wiht a gui.
  - online: codepen, sassmeister are online compilers.

gem install sass.

sass estilos.scss gemerado.css // command
sass --watch estilos.scss:estilos.css // automatic generation

#### Sass vs Sassy

- Sass
  - We dont longer need to write the `{}` or  `;`
  - We need very good knoweldge in css
  - we need to implement good tabulation rules.

```scss
$sans: "Open Sans", sans-serif
$serif: "Times New Roman", serif

body
  font-family: $sans
  color: #900
```

- Sassy
  - We need very good knoweldge in css
  - We mark the file as .scsss

```scss
$sans: "Open Sans", sans-serif;
$serif: "Times New Roman", serif;

body{
  font-family: $sans;
  color: #900;
}
```

### Variables

When we are working with Sass we are able to use variables.
  - When you create a variable you must use the symbol `$`.
  - Variables in Sass are not strong typed.

```scss
$base-color: #300;
$second-color: red;
$width: 300px;

body{
	background-color: $base-color;
	.wrapper{
		width: $width / 150px;
	}
}
```

### Conditionals

Also if you want to check the type of a variable, you can use the `@if` exapresion

```scss
$color-base: #300;
@if type-of($color-base) == color {
    /* Do Something */
} @else {

}
```

### List

There is just one thing to remember regarding the sass list, those list are 1-index

```scss
$colors: red, black, white;

body{
  background-color: nth($colors, 1);
}
```

There are soem very useful function for Sass Lists.
  - nth : return the element in the position n nth($list, n)
  - length: return the size of the list

### Loops

@each

```scss
$colors: red, yellow, green, blue;
 
 @each $value in $colors {
   body {
    	background-color: $value;
   }
}
```

@each

```scss
$socialNetworks:  "facebook", "twitter", "linkedin", "youtube";
$height: 0px; 

@each $valor in $redes {
  .#{$valor}-icon {
    background-image: url('https://resources.acamica.com/gx3253z/b_redes.svg');
	background-position: 0 $alto;
  }
/* 22px para que nos tomen los 2px que viene por defecto */
  $alto: $alto + 22;
}
}
```

@while

```scss
$divs: 5;
$divs-width: 10%;


@while $divs > 0{
  .el-#{$divs}{
		width: $divs-width + $divs;
	}
	$divs: $divs - 1;
}
```

@for

```scss
@for $i from 1 through 4{
  .el-#{$i}{
		width: 20 + $i;
	}
}
```

### Nesting

With Sass we can have nesting selectors.
  - Even that the nesting feature in sass is very useful it is recommended to at most apply 3 leve of nest
  - the `&` symbol is going to represent the previous element of the selector.

```scss
$sans: "Open Sans", sans-serif;
$serif: "Times New Roman", serif;

body{
  font-family: $sans;
  color: #900;
  h2{
    color: violet;
  }
  p{
    text-decoration: none;
        &:hover{
      text-decoration: underline;
      }
  }
}

.cabecera{
	.contenedor &{
		background-color: red;
	}
}
```

#### Nested Media Query

With Sass we can apply nested media queries like the next example:

```scss
$sans: "Open Sans", sans-serif;
$serif: "Times New Roman", serif;

body{
	font-family: $sans;
	color: #900;
	h1{
		color: violet;
  		@media (max-width: 768px){
			color: blue;
			text-align: right;
		}
	}
}
```
### Extend

Sometimes we need a base selector to be used in different parts, in order to dont duplicate the selector we can just write one and ise the @extend feature of sass.

```scss
.message {
  border: 1px solid #999;
  padding: 10px;
  color: #000;
}

.success {
   @extend .message;
   border-color: green;
}

.error {
  @extend .message;
  border-color: red;
} 
```

### Mixin

Mixin is a variation of the extend but it also give us the chance to pass parameters.

```scss
@mixin imgs($name, $color){
  color: $color;
  background-image: url("./imgs/"+$name+".jpg");
  content: $name;
}

.facebook {
  @include imgs("facebook","blue");
}

.pinterest {
  @include imgs("pinterest","red");
}
```

### Functions

Saas also provide us a way to create custom functions when we require it.

```css
@function calculate($num1, $num2){
	@return $num1 + $num2;
  }

.checkout{
	width: calculate(15px, 20px);
}
```

### Maps

Map are pretty much as dictionaries, Sass provide us some features to deal with maps.

 ```scss
$red: (
	color: #CCC,
	background-color: #ff0000,
);

$black: (
	color: #CCC,
	background-color: #000,
);
```

#### Maps Functions

In order to retrieve the information of our created maps we can use the next approaches.
  - map-get function
  - @each over the map

```scss
$red: (
	color: #ff0000,
	background-color: #333,
	text-shadow: 0 0 1px #99F
);

.elemento{
	background-color: map-get($red,color);
}

.elemento{
	@each $key, $valor in $red{
    #{$key}: #{$valor};
  }
}
```