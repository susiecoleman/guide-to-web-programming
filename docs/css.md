# CSS

CSS stands for cascading style sheets. It is used to describe how a html document should look. In web development typically this means how it will look on the screen but it could also mean how it will look on paper. CSS is a style sheet language (as opposed to a mark up language or programming language). Using CSS styles can be applied to elements on the page.

## CSS Syntax
CSS styles are applied to elements they have the following syntax:

```css
h1 {
    color: #ff0000;
}
```
The entire block is called the rule set. This is made up of the selector (in this case `h1`) and the declaration (in this case `color: #ff0000`). The declaration has 2 parts, the property (`color`) and the property value (`#ff0000`). The selector can have multiple properties e.g.

```css
p {
    color: #ff00ff;
    font-size; 10px;
}
```

## Selectors
The selectors determine what part of the page the declarations will be applied to.
### Element Selectors
This is when a style is applied to every element of a certain type. In the example below there are `h1`, `p` and `span` tags and the selectors in the CSS have the same names as the tags they are applied to

<p data-height="432" data-theme-id="0" data-slug-hash="PRGxaG" data-default-tab="html,result" data-user="susiec20" data-embed-version="2" data-pen-title="PRGxaG" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/PRGxaG/">PRGxaG</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

### Class Selectors
Class selectors must always have a `.` at the start of their name when declared in the CSS. They can have any name provided it has no spaces. To apply the class to an element use the syntax `class=className`. In the example below the class `blue-text` is applied to a `span` tag and a `h1` tag. Any element with the class on it will have the declarations for that class appiled to it e.g. turning the text blue.

<p data-height="428" data-theme-id="0" data-slug-hash="LdRXXw" data-default-tab="html,result" data-user="susiec20" data-embed-version="2" data-pen-title="Class Selectors" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/LdRXXw/">Class Selectors</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

### ID Selectors
ID selectors always start with a `#` when declared in the CSS and can have any name provided it has no spaces. An ID can only be applied to one element and allow you to uniquely identify a single element on the page.

<p data-height="265" data-theme-id="0" data-slug-hash="KogbNG" data-default-tab="html,result" data-user="susiec20" data-embed-version="2" data-pen-title="ID Selector" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/KogbNG/">ID Selector</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## Pseudo Classes

Pseudo classes are added to the end of selectors to indicate that you only want the style applied on that selector when the element is in a certain state e.g. when the element is hovered over. The syntax is `selectorName:pseudoClass`. In the example below the paragraph text changes size when you hover over it.

<p data-height="265" data-theme-id="0" data-slug-hash="QmKzgV" data-default-tab="html,result" data-user="susiec20" data-embed-version="2" data-pen-title="QmKzgV" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/QmKzgV/">QmKzgV</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## Properties

There is a finite list of CSS properties that can be set on elements. Common CSS properties are available [here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference).

## Cascading Styles

### Inheritance

In CSS, inheritance controls what happens when property is set for a specific element. The the example below `color` is an inherited property. This is why the text in the span tag is red as well despite the colour of the text in the span tag never being specifically set. `border` is not an inherited property only the paragraph has a border around it. The text in the span tag does not have a border around it. 

<p data-height="152" data-theme-id="0" data-slug-hash="LdRamo" data-default-tab="html,result" data-user="susiec20" data-embed-version="2" data-pen-title="CSS Inheritance" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/LdRamo/">CSS Inheritance</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Inherited styles explain why the style of your web page can change even when a style has not been applied directly to an element. These styles can be overridden by more specific styles as shown in the example below.

<p data-height="227" data-theme-id="0" data-slug-hash="BrLbGW" data-default-tab="css,result" data-user="susiec20" data-embed-version="2" data-pen-title="Override styles" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/BrLbGW/">Override styles</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

If multiple styles are added with the same level of importance, for example definining multiple rule sets with the same selector, the declration that is further down the document will be applied. As shown in this example:

<p data-height="265" data-theme-id="0" data-slug-hash="yKawGj" data-default-tab="css,result" data-user="susiec20" data-embed-version="2" data-pen-title="Identical styles" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/yKawGj/">Identical styles</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Only conflicting rules are overridden. So in this case the background colour is applied from the first rule set but the value for the color property is overridden by the property further down the CSS document.

## Colour Names

Colours in CSS are usually written as [hexidecimal numbers](http://www.mathsisfun.com/hexadecimals.html). This [website](https://htmlcolorcodes.com/) provides a tool to get a colour's hexidecimal value.

## Applying CSS to HTML
Typically CSS is written in a different file to the HTML. This is known as an external stylesheet. In order for the styles in the css file to be applied to the html the css file needs to be linked to the html document. Imagine you have created 2 files in the same directory (or folder) on your computer one called style.css and one called index.html. To link them together a `<link>` tag nested within in the `<head>` tag is used. This is done within the head tag as linking to a style sheet is information about the webpage (metadata) as opposed to information that should appear on the webpage.

```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="style.css">
	</head>
	<body>
	</body>
</html>
```

Styles can also be applied using inline stylesheets and inline styles this article covers [alternative approaches](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works) in more detail.