﻿# HTML

* [First Steps](#First-Steps)
    * [What is a Tag](#What-is-a-Tag)
    * [Basic Structure](#Basic-Structure)
* [Tag](#Tag)
    * [Texts](#Texts)
    * [Div](#Div)
    * [Unordered List](#Unordered-List)
    * [Order List](#Order-List)
* [HiperText](#HiperText)
    * [Link](#Link)
    * [Images](#Images)
    * [Nav](#Nav)
* [Global Atributes](#Global-Atributes)
    * [title](#title)
    * [id](#id)
    * [class](#class)
    * [lang](#lang)
* [Media Tags](#Media-Tags)    
    * [Audio](#Audio)
    * [Video](#Video)

Hypertext Markup language is the standard markup language for documents designed to be displayed in a web browser.

## First Steps

In order to start with html documents, the only thing that we need to do is to create a file with the extension html.

### What is a Tag

Tag is one of the most important concepts of html and basically means all of those pre-defined syntax, that we can use in html.

In order to write Tag we must use the next structure.

```html
<tag-name>content</tag-name>
<p> Paragraph </p>
<h1> Title </h1>
```

### Basic Structure

In the next code we are going to see the basic structure for a html file.

- `<!DOCTYPE html>` :This line defines that we are going to use HTML5 version.

- `<head>` : In the head taf is going to be all the general information of the document

- `<meta charset="UTF-8>` : Define which encoding type uses, UTF-8 is an world wide standard.

- `<body>` : In the body tag is going to be all the content of the document like texts.

````html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
    </head>
    <body>
        <h1>Example test</h1>
    </body>
</html>
````

## Tag

### Texts

- `<title>` : This tag is used in the head section and it is used to give it a name to the page.

- `<p>` : P it means Paragraph.

- `<h1>` : Is the biggest Heading in html, there are 6 levels, h1, h2 .... h6, greater the level smaller the letter.

- `<strong>` : This tag is used to highlight a specific text inside a paragraph.

- `<em>` : This tag is used to write text in italic.

- `<time>` : With this tag we are going to say that the content is a date-time.

### Div

Sometimes we want to group an specific amount of element, so in order to put all of those elements together we can wrap those element with a div tag.

In the next example we are going to wrap some text tag in a div.

```html
<div>
    <p>This paragrahp talk about topic a</p>
    <p>This topic a too.</p>
    <p>This too. <time datetime="2020-01-01"> First January 2020</p>
</div>
```

### Unordered List

The first type of list that we are going to see is the unordered list and basically those list dont keep any kind of order.

- `<ul>` : It means unordered list.

- `<li>` : It means list item.

```htlm
<ul>
    <li>First Item</li>
    <li>Second Item</li>
    <li>Third Item</li>
</ul>
```

See example unorderList.html

### Order List

In this type of list we care about the order.

- `<ol>` : It means ordered list.

- `<li>` : It means list item.

```htlm
<ol>
    <li>First Item</li>
    <li>Second Item</li>
    <li>Third Item</li>
</ol>
```

See example orderList.html

## HiperText

It allows to "jump" from one place to another one using links.

### Link

In order to use links we need to follow the next structure.

- `<a>` : Is the main tag that we must to use if we want to use links

- `href` : Is the address to where we want to go when the user select the link.

```html
<a href="http://www.google.com"> Linked Text </a>
```

### Images

In order to add images in our html pages we need to use the next structure.

- `<img>` : Is the main tag when we want to add images in our document.

- `<src>` : Is the first mandatory atribute for the img tag, means source and the value must be the address where is the image stored.

- `<alt>` : Is the second mandatory img atribute and basically is used to show an alternative message when the image is not successfully load.

```html
<img
    src="imageSource.jpg"
    alt="Alternative message"
    width="400"
    height="300"/>
```
### Nav

Usually we have in our web pages navegation, that means that we can move to different html documents in the same web page, in order to define the navegation we can use the tag Nav.

```html
<nav>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="services.html">Serivces</a></li>
    <li><a href="products.html">Products</a></li>
    <li><a href="contact">Contacts</a></li>
  </ul>
</nav>
```

## Global Atributes

We previously see that some specific tags have some atributes, for example the tag <a></a> has the atribute href or the tag <img></img> has the atributes src and alt, but there are other kind of atributes that we can apply to every single tag.

### title

Have you ever noticed that sometimes when we are in a webpage and leave the pointer over one component, one specific text appears?. This is the purpose of the title atribute, when you leave the pointer in a component is going to show a little text.

### id

This atribute allow us to identified an element. It is very important that if we want to use this atribute we must be sure that all the ids are unique.

### class

This atribute allow to identified a group of elements, so we can mark multiples element with the same class name.

### lang

It means languague and the purpose of this tag is to specify what is language use in the html page.

## Media Tags

There are some tags that we used  when we need to deal with media information like audios or video information.

### Audio

If you're dealing with audios, html5 allow you to use one specific tag called `<audio>`, If you add the controls atribute then the stop and play options are going to be available in the web page.

```html
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  <p>Alternative Content for the old browsers</p>
</audio>
```

### Video

Otherwise if you're dealing with videos you can use the tag `<video>`, the video tag has some extra atributes like width, height, poster(The preview image just before play the video) and controls(play and stop controls).

```html
<video controls width="320" height="240" poster="images/movie.gift">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  <p>Alternative Content for the old browsers</p>
</video>
```