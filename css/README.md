# CSS

Cascading Style Sheet.

CSS is presentation lenguage that is used to modify the design of a web page.

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

![](https://github.com/andresmontoyab/Frontend/blob/master/resources/story-mapping.PNG)

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

![](https://github.com/andresmontoyab/Frontend/blob/master/resources/story-mapping.PNG)

```css
p {
  width: 100px;
  height: 50px;
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

