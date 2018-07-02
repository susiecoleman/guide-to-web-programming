# Interactive Javascript

Javascript can be used to manipulate the HTML that makes up a webpage. This allows the page to be interactive and change depending on what actions a user does. For example, you could define a button using the html tag `<button>`. You could combine this with javascript to detect when the button is clicked. The javascript code that runs after you click the button could change the CSS to make the font of the page larger. This is an example of HTML, CSS and javascript all working together so that a webpage is interactive. You can write a webpage using only HTML and CSS. The webpage will look the same for everyone who visits it. This is called a static webpage, it never changes. By using javascript you can make a dynamic website, this is a website that changes based on user actions.

## The DOM (Document Object Model)

The DOM is provided by the javascript language and lets you easily access parts of a html page and then manipulate the page, for example changing the font colour or adding more html to a page. This is how interactivity can be added to a website. 

For example if you wanted to build a multiple choice quiz website with radio buttons for every possible answer and a button to allow whoever visited your website to check their answers. You would write the questions and the check button in a html document. But you would need to add javascript to make it interactive. The javascript code would run when the button was pressed. The javascript code would find the radio buttons in the html page and see which ones were selected. From this you could work out how many your user got right. The javascript code could then add a paragraph element to the html page telling the user how many answers the user got right. 

## Using the DOM to get HTML elements

```var body = document.body```

This will get everything inside the `<body>` tag on the html page and assign to to the variable `body`. The HTML page of this guide covered how a HTML page can be viewed as a tree where every HTML tag has a parent and children. This model can be applied here as well. Once we have used `document.body` and have the body we can get all the children of body.

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Bees Website</title>
	</head>
	<body>
		<h1>Bees</h1>
		<p>I like bees.</p>
		<p>Bees are nice.</p>
	</body>
</html>
```
In this example HTML document the body tag has 3 children
```html
<h1>Bees</h1>
<p>I like bees.</p>
<p>Bees are nice</p>
```

To select these 3 elements in our javascript code we can do:

```javascript
//Get the body of the html page
var body = document.body;
//Get all the children of the body. This will return an array.
var children = body.children;
```

Because our html page is just a tree we can 'walk the tree' and keep getting the children of children nodes until we get the element we need. 

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Bees Website</title>
	</head>
	<body>
		<h1>Bees</h1>
		<ul>
			<li>Honey Bees</li>
			<li>Bumblebees</li>
			<li>Stingless Bees</li>
		</ul>
	</body>
</html>
```

For example if we had this webpage and wanted the second item on the list we could do:
```javascript
//Get the body of the html page
var body = document.body;
//Get all the children of the body. This will return an array.
var children = body.children;
//Get the second item on the list (Don't forget the first item on a list is at index 0)
var beeList = children[1];
//Get the second item on the list
var itemTwo = list[1];
```

But this can get quite complicated especially if you have a complex webpage. It is possible to get an item on the page directly.

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Bees Website</title>
	</head>
	<body>
		<h1>Bees</h1>
		<ul>
			<li>Honey Bees</li>
			<li id='second'>Bumblebees</li>
			<li>Stingless Bees</li>
		</ul>
	</body>
</html>
```

This is the same webpage but with an id on item 2 in the list. Now it's easy to get the element directly.

```javascript
var item2 = document.getElementById('second');
```

Another option is to get all elements by type. For example if you wanted to add an accessablity button to your website to allow a user to change the font size of all of the paragraphs. It would be really useful to be able to select all of the paragraphs at once.

```javascript
//Gets an array of all the paragraphs
var paragraphs = document.getElementsByTagName("p");
//Gets an array of all the images
var images = document.getElementsByTagName("img");
```

## Using Javascript to Set Attributes

## Event Listeners

## Applying Javascript to HTML

Typically Javascript is written in a different file to the HTML. In order for the javascript to run when the html page is loaded the javascript file needs to be linked to the html document. Imagine you have created 2 files in the same directory (or folder) on your computer one called script.js and one called index.html. To link them together a `<script>` tag is used.

```html
<!DOCTYPE html>
<html>
	<head>
	</head>
	<body>
        <h1>My Website</h1>
        <script src="script.js"></script>
	</body>
</html>
```

The script tag can in theory go anywhere as long as it's within the `<html>` tag. However it typically is the final tag within the body tag so that all of the html content is parsed by the browser before it tries to get the javascript file. This allows your user to start reading the site even if the javascript hasn't yet run. This is useful for slow web connections. Also it means all the elements of the page that the javascript might manipute or refer to will have been rendered by the browser.