# JQuery

jQuery is a JavaScript library designed to simplify HTML DOM tree traversal and manipulation, as well as event handling, CSS animation, and Ajax

* [First Steps](#First-Steps)
* [JQuery Selectors](#JQuery-Selectors)
  * [Parent](#Parent)
  * [Closest](#Closest)
  * [Children](#Children)
  * [All Decendents](#All-Decendents)
* [Visual Efects](#Visual-Efects)
  * [FadeIn](#FadeIn)
  * [FadeOut](#FadeOut)
  * [SlideDown](#SlideDown)
  * [SlideUp](#SlideUp)
  * [Hide](#Hide)
  * [Show](#Show)
  * [Animate](#Animate)
* [Updating Tag Content](#Updating-Tag-Content)
* [Updating Tag Atribute](#Updating-Tag-Atribute)
* [Updating CSS](#Updating-CSS)
* [Events](#Events)

## First Steps

In order to start with JQuery we have go to the oficcial page https://jquery.com and right there download the min.js file.

When we have in our local the min.js file with the jquery function, we must imported in our html.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title> Using Jquery</title>
        <script src="jquery-1.x-git.min.js"></script>
        <script>
            $(document).ready( function(){
                $("h1").hide();
                $("h1").fadeIn();
        });
        </script>
    </head>
    <body>
        <h1>Using Jquery</h1>
    </body>
</html>

```

## JQuery Selectors

A JQuery selector is a way to select elements from the DOM using JQuery.

Let say that we want to select all the h1 elements in our DOM and after that hide all of those elements, we can write something like this.

```js
$(document).ready(function(){
    var $elemento = $("h1");
    $elemento.hide();
  });
```

Basically in JQuery we can use the same css selectors, some examples are the next.

```js
$(document).ready(function(){
    var $elemento = $("h1");
    var $menu = $("#menu"); // Element with id menu
    var $visible = $(".visible"); // Element that belongs to the class visible
    var $p = $("h1 p"); // Element p that is inside a h1 element
  });
```

### Parent

If we already retrieve some elements using selectors, but we want the parent of those element, we can use the jquery funtion parent()

```js
$(document).ready(function(){
    $("#principal").parent().slideUp();
});
```

### Closest

If we already retrieve some elements using selectors, but we want the parent of those element that match another selector , we can use the jquery funtion closest()

```js
$(document).ready(function(){
    $("li a").closest("ul").slideUp();
});
```

### Children

If we already retrieve some elements using selectors, but we want the children of those elements , we can use the jquery funtion children()

```js
$(document).ready(function(){
    $("#botonera").children(".actual").slideUp();
});
```

### All Decendents

Sometimes we just dont want to find the children, also we want to find even the children of the children, in this case the children() function is not enought, but we can use the function find();

```js
$(document).ready(function(){
  $("#botonera").find("a.actual").slideUp();
});
```

## Visual Efects

Usually in our webpage we want some visual effects, like  dissapear some element for a specific amount of time or show a element with an animations, for this reason JQuery has some visual effects that can helps us to achieve that.

### FadeIn

We can hide some element with the function hide() and after that we can show with an animation that hidden element using the function fadeIn().

- This function receives a parameter in which we can set the amount of time in miliseconds that the animations is going to take. fadeIn(1000)

```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.hide();
    $elemento.fadeIn(1000);
  });
```

### FadeOut

If we have a visible element we can make it dissapear with an animation using the the function fadeOut()

- This function receives a parameter in which we can set the amount of time in miliseconds that the animations is going to take. fadeOut(1000)

```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.hide();
    $elemento.fadeIn(1000);
    $elemento.fadeOut(2000);
  });
```

### SlideDown

This function make an element appear from top to the bottom with an animation, also this function receives a parameter that indicate the amount of time that the animation is going to take.
 
```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.hide();
    $elemento.slideDown(2000);
  });
```

### SlideUp

This function make an element disappear from bottom to the top with an animation,  also this function receives a parameter that indicate the amount of time that the animation is going to take.

```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.slideUp(2000);
  });
```

### Hide

If we want to hide instantaneously an element without any kind of animatioonm we can use the function hide()

```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.hide();
  });
```

### Show

If we want to show instantaneously an element without any kind of animatioonm we can use the function show()

```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.show();
  });
```

### Animate

JQuery let us animate elements with the function animate, this function receives two propertoes.

- first parameter: Is an object with the css properties that we want to modify.
- second parameter: Is the amount of time that the animation is going to take.

```js
$(document).ready(function(){
    var $elemento = $("#element");
    $elemento.animate(
        {
            "opacity": "0.5", 
            "margin-left": "10px", 
            "height": "toggle"
        }, 1000);
  });
```

## Updating Tag Content

Something we want to update some specific elements of our DOM for new want, jquery let us do this with the html function.

```js
$("#botonera").html("<li>Nuevo item</li>"); // Update Tag
```

If we use the html() without any parameter the istead of chaging the tag is going to return the current value.

```js
$("#botonera").html(); // Retrieve current tag
```

## Updating Tag Atribute

If we wanto to update one atribute of one tag, we can use the jquery function attr(), the function attr is overlaoded, the first one receive two parameters and the second one receive just one.

### attr two parameters

- first parameter: The name of the atribute
- second parameter: The new value of the parameter

```js
$("img").attr("alt", "New value");
```

### attr one parameter

This function instead of update the value is going to retrieve the current value of the atribute

- first parameter: The name of the atribute that we want to retrieve

```js
var $img_src = $("img").attr("src");
```

## Updating CSS

If we want to update/retrieve one css property using jquery, we can do it using the function css(), the function css() is overlaoded with three signatures

### css one parameter

This signature is going to retrieve the value of the css property

- first parameter: The name of the css property that we want to retrieve

```js
var margen_superior = $("h1").css("margin-top");
```

### css two parameter

This signature is going to update one css property.

- first parameter: The name of the css property that we want to update
- second parameter: The new value of the css property.

```js
$("h1").css("opacity", "0.5");
```

### css multiple updates

This signature is going to update more than one css property.

- first parameter:  An object with multiples css property.

```js
$("h2").css({"opacity": "0.5", "margin-top": "20px"});
```

## Events

Events are actions that the application can trigger when the user does one specific actions, the most common event is a click.

```js
$("h1").click( function(){
    $(this).fadeOut(); // #(this) was the clicked element
} );


$("h1").hover( function(){
  $(this).animate({"opacity": "0.5"}, 500);
}, function(){
  $(this).animate({"opacity": "1"}, 500);
});
```

