# CSS

  * Cascading Style Sheets (CSS)
  * CSS, by itself, does nothing.
  * Responsible for determining how your HTML **looks**

# Why Does CSS Exist?

  * CSS formats your webpage. Without it, there is only content, and no structure or styles.
  * Can be written within HTML, or using an external style sheet (the correct way)
  * Creating external style sheets prevents you from having to write code multiple times, and makes it easy to modify.

# Styling Text With CSS

  * Using CSS **properties**, you can modify the appearence of your HTML.
  * This can done by targeting HTML **elements**.

# Inline Style

  * Adding the style onto the HTML element directly
  * Uses the `style` attribute of an element
  * Declarations go within the `style` attribute value

```html
<h1 style="color: red; font-size: 32px;">
```

# Example:

Let's say we have the following HTML:

```html

<!DOCTYPE html>
<html>
  <head>
    <title>My Cat</title>
  </head>
  <body>
  	<h1>My Cat Bob</h1>
    <p>My cat is named Bob. He is a lazy cat.</p>
  </body>
</html>
```

Here is an example of CSS:

```css
h1 {
  color:red;
  font-size:24px;
}

p {
  color:blue;
  font-size: 12px;
}
```

What is the CSS doing here?

# Selectors and Properties

  * CSS is constructed of **selectors** and **properties**.
  * Selectors determine where the styles are applied.
  * Properties determine what those styles are.
  * CSS begins with a selector, followed by curly braces.
  * Declare your styles inside the curly braces.

# Examples of Selectors

| selector         | meaning          |
|------------------|------------------|
| `p`, `div`, etc. | element selector |
| `.class`         | class selector   |
| `#id`            | ID selector      |
| `*`              | Wildcard ("any") |

# Examples of Properties

| property      | meaning                                |
|---------------|----------------------------------------|
| `color`       | text color                             |
| `border`      | Defines border width, style, and color |
| `text-align`  | justifies text                         |
| `font-size`   | size of font                           |
| `font-family` | defines font                           |

# LAB: Basic Selectors

* Complete the following exercise on Mozilla Developer Network

  * [Selecting Different Elements](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Simple_selectors#Active_learning_Selecting_different_elements)

# CodePen

<iframe height="265" style={{width: '100%'}} scrolling="no" title="MWWVEeO" src="https://codepen.io/habenzy/embed/MWWVEeO?height=265&theme-id=default&default-tab=html,result" frameBorder="no" allowtransparency="true" allowFullScreen={true}>
  See the Pen <a href='https://codepen.io/habenzy/pen/MWWVEeO'>MWWVEeO</a> by Robert Stauss
  (<a href='https://codepen.io/habenzy'>@habenzy</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

To embed codepens in our markdown you need to embed them as iframes, modify the style tag so that it's in React format (`style="width: 100%"` => `style={{width: "100%"}}`), make the `frameborder` property camelCase (`frameBorder`), as well as the `allowfullscreen` property, which also needs it's value to be a boolean (`allowfullscreen="true"` => `allowFullScreen={true}`)

# CodeSandbox

<iframe
     src="https://codesandbox.io/embed/hello-world-b2j7u?fontsize=14&hidenavigation=1&theme=dark"
     style={{width:"100%", height:"500px", border:0, borderRadius: "4px", overflow:"hidden"}}
     title="hello-world"
     allow="geolocation; microphone; camera; midi; vr; accelerometer; gyroscope; payment; ambient-light-sensor; encrypted-media; usb"
     sandbox="allow-modals allow-forms allow-popups allow-scripts allow-same-origin"
   ></iframe>

Like codepen, works if you change the style prop (`style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"` => `style={{width:"100%", height:"500px", border:0, borderRadius: "4px", overflow:"hidden"}}`)


# Compound Selectors 1

Selectors can target elements nested within other elements

```css
p img {
  max-width: 320px;
  height: auto;
}
```

# Compound Selectors 2

Selectors can target specific elements with a class

```css
h1 .title {
  display: block;
  margin: 0, auto;
  padding-top: 1em;
}
```

# LAB: Multiple Class Selectors

* Complete the following exercise on Mozilla Developer Network

  * [CSS Selectors for Multiple Classes](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Simple_selectors#Active_learning_Handling_multiple_classes)

# Compound Selectors 3

Selectors can target specific elements with several layers of nesting

```css
main .introduction > p {
  background-color: lightgray;
  margin: 10px auto;
}
```

"apply these styles to all `p`s that are direct children of a `div` of class `introduction` inside the `main` section"

# Psuedo-Class Selectors

You can target the state of an element using `psuedo-class` selectors

  * Hover
  * Visited
  * Checked
  * Active
  * Many others

[Full List on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes "Full list of CSS psuedo-classes on Mozilla Developer Network")

[MDN Psuedo-Class Tutorial](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Pseudo-classes_and_pseudo-elements "MDN Psuedo-Class Tutorial")

```css
a:hover {
  background-color: red;
}

a:clicked {
  background-color: blue;
}

a:active {
  background-color: green;
}
```

# LAB: CSS Diner

* Complete the following CSS selector game

  * https://flukeout.github.io/

# Including CSS into HTML

There are several ways to add style to an HTML page

  * `<style>` Embedded CSS
  * `<link>` Tag to a CSS file
  * `<h1 style="color: red; font-size: 32px;">` Inline
  * `<link>` Tag to a CSS file
  * `<style>` Tags with `@import` of a CSS file

# CSS Style Tags

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Cat</title>
    <style type="text/css" media="screen">
     div {
       float: left;
       width: 49%;
       height: 100px;
       border: solid red 1px;
     }

     button {
       float: left;
       clear: both;
     }
    </style>
  </head>
  <body>
  	<h1>My Cat Bob</h1>
    <p>My cat is named Bob. He is a lazy cat.</p>
  </body>
</html>
```

# Linking to CSS

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Cat</title>
    <link href="styles/style.css" rel="stylesheet" type="text/css">
  </head>
  <body>
  	<h1>My Cat Bob</h1>
    <p>My cat is named Bob. He is a lazy cat.</p>
  </body>
</html>
```

# @import

  * You can put all your CSS in one file
  * You can load one CSS file into another using `@import`

## Example

```html
<style type="text/css" media="screen">
  @import 'my_special_css_file.css';
</style>
```

https://developer.mozilla.org/en-US/docs/Web/CSS/%40import

# The Element Box Model

  * Imagine every HTML element as a 'box'.
  * Every box consists of four different 'layers': Margin, Border, Padding, and Content.
  * Margins and padding help to position and align content inside an HTML element.
  * Padding and margins are transparent. Think of it as empty space.
  * Borders can be colored, or image-based. They can also be 'styled' (dashes, dots, etc.)

![Illustration of the CSS box model](https://pressupinc.com/wp-content/uploads/2014/01/box-model.png "CSS Box Model")

* More information: [MDN: CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model "MDN CSS Box Model, additional information")
* Even more information: [Shay Howe, opening the box model](https://learn.shayhowe.com/html-css/opening-the-box-model/ "Learn CSS with Shaw Howe, opening the box model")

# Cascading Syles

```css

h1 {
  color: red;
}

.title {
  color: yellow;
}

#introduction {
  color: blue;
}
```

```html
<h1>Hi there, I am RED</h1>
<h1 class="title">Hi there, I am YELLOW</h1>
<h1 class="title" id="introduction">Hi there, I am BLUE</h1>
```

# The !Important Declaration

Using `!important` in a declaration overrides all other declarations

## Example

```css

h1 {
  color: red;
}

.title {
  color: yellow !important;
}

#introduction {
  color: blue;
}
```

# Style Override Precedence

* 5. Element Selectors
* 4. Class Selectors
* 3. ID Selectors
* 2. Inline CSS
* 1. !important

# Style Specificity Precedence

* More specific selectors will override less specific

```css
.main p {
  // Least specific
  background-color: yellow;
}

.header .title h1{
  // Somewhat specific
  background-color: red;
}

.nav .menu .option li{
  // Most specific
  background-color: blue;
}
```
