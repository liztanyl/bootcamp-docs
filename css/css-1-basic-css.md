# CSS.1: Basic CSS

## Intro To CSS 

In the beginning was html and only html.  But programmers wanted to add styling to their web pages to help distinguish themselves from others on the web.  Initially, the answer was 'you're screwed'.  But in October 1994, Håkon Wium Lie introduced Cascading Style Sheets to the world. Today it is better known as CSS.

CSS is a declarative language. It doesn't tell the browser what to do but rather describes the rules that the browser then uses to render the page. CSS became popular because it was predictable and forgiving in its syntax.  It was also easy to learn.  
The concept of cascading styles is unique to CSS.  To cascade means that styles can inherit and overwrite styles through its hierarchy called specificity.  More on that in section 2. This concept also allowed for many style sheets to be applied to one page.  That is what made CSS so popular.   

As a declarative language, CSS uses selectors and declarations to apply styling rules to HTML pages.  The syntax for CSS starts with a selector which tells the browser the rules for styling  the selected elements. Then a code block is created using open and closing curly braces.  Inside the code block declarations or rules are created.  A declaration is made up of a property name followed by a colon and then the value of the property followed by a semi-colon.  You can have as many declaration statements as needed. It is the standard to put each declaration on its own line in code. The semi-colon tells the browser that the end of the line is reached so be sure to add it at the end of every declaration. 

###Sample Syntax

```css
selector{
	property: value;
}
```

There are three places where CSS styling can occur: 


1. in-line 
2. internal
3. external. 

### In-Line Styling

**In-line styling** is written inside the HTML opening tag as an attribute-value pair. Like this:

```html

<p style=“color: red;”> This text would be red </p>


```


If more than one style declaration is applied:

```html

<p style=“color: red; font-weight: bold;”> This text is red and bold</p>


```

### Internal Styling

**Internal styling** is placed inside the head tag of the page and is wrapped inside the style tag. In this example, the selector of p is chosen to style all the paragraph tags on the page.

```html
<html>
   <head>
      <title> Page Title </title>
 		  <style>
			  p{			
	  			 color: white;
			   }
		  </style>
	</head>
	<body>
		<p> This text is white </p>
	</body>
</html>
```

### External Styling
	
**External styling** links a css stylesheet to the HTML page.  This is done by adding a link tag in the head of the HTML file.

```html

<link src=“style.css” rel=“type/stylesheets” />


```

The stylesheet would contain the same css coding that would be put in the head directly.

**External Styling is the standard and should always be used.**  The other two ways should seldom if ever be used.   


##CSS Example 
In these examples, we will be using internal styling as it makes it easier for teaching purposes.  However, in the coding world, all css should be externally linked to the html page. 

Remember that every browser has a CSS engine and that engine has default declarations for HTML elements. So to change the look of an h2 tag requires that a declaration block be made to apply new rules to the h2 tags in the file. Let's start with the following file.

```html
<html>
   <head>
      <title> Page Title </title>
  	</head>
	<body>
		<h2> Styling H2 tags </h2>
	</body>

```
Copy and paste the above code snipet and save the file as index.html.  Then open the file in a browser and notice how the text looks.

Next insert the following code just after the title tag and just above the closing head tag.

```html
	<style>
		h2 {
			background-color: blue;
			color: white;
		}
	</style>
```

This code targets all h2 tags in the file and makes the background-color blue and the color of the text white.

Refresh your browser and you should see that the h2 has a blue background-color and white text.

##Selector Combinations

So far we have been looking at a single selector and applying declarations for that element.  Below is a table that shows how to use different selector combinations and the elements they target.

| Selector Type | Example | Explanation |
|:---: | :---: | --- |
| single  | p | Targets all p tags |
| multiple | p , h1, h3 | Targets p, h1 and h3 tags |
| descendant | div p | Targets p tags that are descendants of a div |
| child | div > p | Targets p tags that are immediate children of a div |
| adjacent sibling | h2 + p | Targets p tag that is immediately adjacent to an h2 tag |
| class | .class_name | Targets all elements with the class of class_name|
|id | #id_name | Targets the one element with the id of id_name| 
| universal | * | Targets all elements |
  




##CSS In-Class Exercises

Now download the following folder css\_exercises 
And then open the day\_1 folder inside the css\_exercises directory.
Let's link the html file to the css file by adding the following line just after the meta tag inside the head tag:

`<link src="styles.css" rel="type/stylesheets" />`

