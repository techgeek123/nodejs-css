# CSS DeepDive

## Learning Competencies

- Understanding Box Bindings(Box Model, Positioning, Z-index)
- Pseduo classes & Pseudo elements in CSS
- Understanding Image replacement and sprites in CSS
- Writing Media Queries for different viewports
- Preprocessor(SASS, LESS)
- HTML5 Canvas
- Animation(Transitions, Transforms, Keyframes, SVG)
- Flexbox(Foreshadowing Flexbox, Justification and Order, Aligning Alibis, Sizing Up the Properties, Property Plotting)

## Introduction

### Box Bindings

#### Box Model: 

The CSS box model is a set of rules that defines how every element in a web page is rendered. According to the box model, every element in a page is a rectangular box with at least a content, a width and a height.

According to the CSS box model, every element in a web page is a rectangular box. The content is in the middle, surrounded by optional elements such as padding, border, and margin. The box model has five main parts/properties that determine the size of the box. Those properties are the width, the height, the padding, the border, and the margin.

Apart from the width, height, the other properties are optional. Meaning that we can have a box with no padding, no border, and no margin. In the next section, we will detail the different parts of this box.

Continue reading about box model from [here](https://medium.com/launch-school/https-medium-com-dembasiby-understanding-the-css-box-model-b005a82593a6).....

#### Psuedo selectors:

In this, the third in our series of articles on selectors, we discuss pseudo-selectors. These don't select elements, but rather certain parts of elements, or elements only in certain contexts. They come in two main types: pseudo-classes and pseudo-elements.

##### Psuedo classess

A CSS pseudo-class is a keyword, preceded by a colon (:), added to the end of selectors to specify you want to style the selected elements, and only when they are in certain state. For example, you might want to style an element only when it is being hovered over by the mouse pointer, or a checkbox when it is disabled or checked, or an element that is the first child of its parent in the DOM tree.

##### Psuedo elements

Pseudo-elements are very much like pseudo-classes, but they have differences. They are keywords, this time preceded by two colons (::), that can be added to the end of selectors to select a certain part of an element.



::after

::before

::first-letter

::first-line

::selection

::backdrop

They all have some very specific behaviors and interesting features, but digging into them all in detail is beyond our scope for now.

Read more [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Pseudo-classes_and_pseudo-elements)........

#### Image Replacement and Sprites in CSS

Gone are those days when we had to use Javascript in order to replace and image show some kind of animation like effect on hover or click

Read more [here](http://wpandsuch.com/css-sprites-image-replacement/).......

#### Preprocessor

##### _SASS_

- Variable creation: To remove duplicacy in CSS you can assign variables

```sass
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

- Nesting

 When writing HTML you've probably noticed that it has a clear nested and visual hierarchy. CSS, on the other hand, doesn't.
Sass will let you nest your CSS selectors in a way that follows the same visual hierarchy of your HTML. Be aware that overly nested rules will result in over-qualified CSS that could prove hard to maintain and is generally considered bad practice.
With that in mind, here's an example of some typical styles for a site's navigation:

```sass
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

- Partials

You can create partial Sass files that contain little snippets of CSS that you can include in other Sass files. This is a great way to modularize your CSS and help keep things easier to maintain. A partial is simply a Sass file named with a leading underscore. You might name it something like `_partial.scss`. The underscore lets Sass know that the file is only a partial file and that it should not be generated into a CSS file. Sass partials are used with the `@import` directive.

- Mixins

Some things in CSS are a bit tedious to write, especially with CSS3 and the many vendor prefixes that exist. A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. You can even pass in values to make your mixin more flexible. A good use of a mixin is for vendor prefixes. Here's an example for border-radius.

```sass
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

.box { @include border-radius(10px); }
```


- Inheritance

This is one of the most useful features of Sass. Using @extend lets you share a set of CSS properties from one selector to another. It helps keep your Sass very DRY. In our example we're going to create a simple series of messaging for errors, warnings and successes using another feature which goes hand in hand with extend, placeholder classes. A placeholder class is a special type of class that only prints when it is extended, and can help keep your compiled CSS neat and clean.

```sass
// This CSS won't print because %equal-heights is never extended.
%equal-heights {
  display: flex;
  flex-wrap: wrap;
}

// This CSS will print because %message-shared is extended.
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```

- Operators

Doing math in your CSS is very helpful. Sass has a handful of standard math operators like +, -, *, /, and %. In our example we're going to do some simple math to calculate widths for an aside & article

```sass
.container { width: 100%; }


article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complementary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```

##### _LESS_

Why LESS?

Bootstrap is made with LESS at its core, a dynamic stylesheet language created by our good friend, Alexis Sellier. It makes developing systems-based CSS faster, easier, and more fun.

What's included?

As an extension of CSS, LESS includes variables, mixins for reusable snippets of code, operations for simple math, nesting, and even color functions.

NOTE: LESS has very same structure to that of SASS. You'll easily be able to differentiate b/w LESS & SASS

Read more about less [here](http://lesscss.org)......

#### HTML5 Canvas

What is HTML Canvas?

The HTML <canvas> element is used to draw graphics, on the fly, via JavaScript. The <canvas> element is only a container for graphics. You must use JavaScript to actually draw the graphics. Canvas has several methods for drawing paths, boxes, circles, text, and adding images.

```html
<canvas id="myCanvas" width="300" height="150">
This is HTML5 canvas feel free to draw anything on it
</canvas>
```

## Exploration:

- Understanding CSS Box Model Visually: http://guyroutledge.github.io/box-model/
- Read more about HTML5 canvas API here: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- MDN Canvas tutorial here: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial
- A complete guide on Flexbox by CSS Tricks: https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- A good read on CSS3 Animations: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations

