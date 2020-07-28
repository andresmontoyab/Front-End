# Html

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

- `<em>` :This tag is used to write text in italic.

### Div

Sometimes we want to group an specific amount of element, so in order to put all of those elements together we can wrap those element with a div tag.

In the next example we are going to wrap some text tag in a div.

```html
<div>
    <p>This paragrahp talk about topic a</p>
    <p>This topic a too.</p>
    <p>This too.</p>
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





## Atributes

