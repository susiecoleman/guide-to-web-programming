# HTML

HTML stands for Hyper Text Markup Language. It gives the page a semantic structure e.g. This is text is a paragraph, this text is a header, this is an image, this is link. The browser will then use this information to decide how to display the HTML. For example header text should be bigger than paragraph text.

## Elements

These items (paragraphs, headers, images etc.) are referred to as elements. A webpage is a collection of elements.

## Tags

Tags are used to indicate an element (e.g. this is a paragraph). A html document is text annotated with html tags and a web page is a html document.

Tags look like this:
```html
<p>This is a paragraph</p>
```

There is a finite list of tags as browsers need to know all available tags in order to decide how to handle them. This list is maintained by [W3C (World Wide Web Consortium)](https://www.w3.org/). A list of all elements is available [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element). 

## Attributes

Elements can have attributes that provide additional information about the element or adjust the behaviour of the element. For example when using an [image tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) an attribute is used to provide the link to an image. When using a [form tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form) you can use it's autocomplete attribute to determine whether or not values can be autocompleted by the browswer. A list of all attributes is available [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes).

## Structuring a HTML Document

This is a very basic HTML document.

```html
<!DOCTYPE html>
<html>
	<head>
	</head>
	<body>
	</body>
</html>
```

Tags are nested and the structure of a webpage is like a tree. The `html` tag is the top level tag and it has 2 children `head` and `body`. The `head` tag has metadata about the page e.g. links to the css and the `body` tag contains the html for content that will appear on your site.

This is a more complicated example including some more html tags.

```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="style.css">
	</head>
	<body>
		<h1>Bees</h1>
		<p>Bees are flying insects closely related to wasps and ants, known for their role in pollination and, in the case of the best-known bee species, the European honey bee, for producing honey and beeswax. Bees are a monophyletic lineage within the superfamily Apoidea and are presently considered a clade, called Anthophila. There are nearly 20,000 known species of bees in seven recognized biological families. They are found on every continent except Antarctica, in every habitat on the planet that contains insect-pollinated flowering plants.</p>
		<p>Some species including honey bees, bumblebees, and stingless bees live socially in colonies. Bees are adapted for feeding on nectar and pollen, the former primarily as an energy source and the latter primarily for protein and other nutrients. Most pollen is used as food for larvae. Bee pollination is important both ecologically and commercially; the decline in wild bees has increased the value of pollination by commercially managed hives of honey bees.</p>
		<img src="https://upload.wikimedia.org/wikipedia/commons/3/32/Bee-apis.jpg" />
	</body>
</html>
```
This shows what the html looks like when rendered by a browser. By clicking on 'edit on Codepen' you can experiment with changing the html or adding new html tags. Note codepen does not include head and body tags in it's examples so any code written here would need to go inside the body tag if it was being added to a webpage.

<p data-height="628" data-theme-id="0" data-slug-hash="BYXEeO" data-default-tab="html,result" data-user="susiec20" data-embed-version="2" data-pen-title="Basic HTML Elements" class="codepen">See the Pen <a href="https://codepen.io/susiec20/pen/BYXEeO/">Basic HTML Elements</a> by Susie (<a href="https://codepen.io/susiec20">@susiec20</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
