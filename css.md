# What is CSS?
<li>CSS stands for Cascading Style Sheets
<li>CSS describes how HTML elements are to be displayed on screen, paper, or in other media
<li>CSS saves a lot of work. It can control the layout of multiple web pages all at once
<li>External stylesheets are stored in CSS files
<div style="margin-bottom:15px"></div>

# CSS Syntax
## CSS selector

<li>The selector points to the HTML element you want to style.

<li>The declaration block contains one or more declarations separated by semicolons.

<li>Each declaration includes a CSS property name and a value, separated by a colon.

<li>Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.
<div style="margin-bottom:15px"></div>

## The CSS element Selector
### The element selector selects HTML elements based on the element name.

Example
Here, all ```<p>``` elements on the page will be center-aligned, with a red text color: 
```
p {
  text-align: center;
  color: red;
}
```
<div style="margin-bottom:15px"></div>

## The CSS id Selector
### The id selector uses the id attribute of an HTML element to select a specific element.

The id of an element is unique within a page, so the id selector is used to select one unique element!

To select an element with a specific id, write a hash (#) character, followed by the id of the element.

Example
The CSS rule below will be applied to the HTML element with id="para1": 
```
#para1 {
  text-align: center;
  color: red;
}
```
### Note: An id name cannot start with a number!

<div style="margin-bottom:15px"></div>

# The CSS class Selector
## The class selector selects HTML elements with a specific class attribute.

To select elements with a specific class, write a period (.) character, followed by the class name.

Example
In this example all HTML elements with class="center" will be red and center-aligned: 
```
.center {
  text-align: center;
  color: red;
}
```
You can also specify that only specific HTML elements should be affected by a class.

Example
In this example only ```<p>``` elements with class="center" will be red and center-aligned: 
```
p.center {
  text-align: center;
  color: red;
}
```
HTML elements can also refer to more than one class.

Example
In this example the ```<p>``` element will be styled according to class="center" and to class="large": 
```
<p class="center large">This paragraph refers to two classes.</p>
Note: A class name cannot start with a number!
```
<div style="margin-bottom:15px"></div>

# The CSS Universal Selector
## The universal selector (*) selects all HTML elements on the page.

Example
The CSS rule below will affect every HTML element on the page: 
```
* {
  text-align: center;
  color: blue;
}
```
The CSS Grouping Selector
The grouping selector selects all the HTML elements with the same style definitions.

Look at the following CSS code (the h1, h2, and p elements have the same style definitions):
```
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```
It will be better to group the selectors, to minimize the code.

To group selectors, separate each selector with a comma.

Example
In this example we have grouped the selectors from the code above: 
```
h1, h2, p {
  text-align: center;
  color: red;
}
```