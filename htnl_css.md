**HTML Interview QA**

What is HTML(Hyper Text Markup Language?
=> HTML stands for HyperText Markup language.
It is a standardized system for creating web pages.
HTML creates the structure of a web page and uses “tags” to mark up a web page.

# Types HTML Doctype
  In HTML version 4, there are three types of DOCTYPES can be used: 
  * strict 
  * transitional
  * frameset.


# What is semantic elemnts?

=> A semantic element clearly describes its meaning to both the browser and the developer.

  Semantic Elements: 							          Non-semantic Elements:

  * <form> <table> and <article>				    * <div> and <span>
  * <header> <footer>, <nav>, <section>

# Web storage:

  window.localStorage - stores data with no expiration date      size: 2 MB to 10 MB

  localStorage.setItem("lastname", "Smith");	// Store
  localStorage.getItem("lastname");			      // Retrieve
  localStorage.removeItem("lastname");		    // Remove

  window.sessionStorage - stores data for one session (data is lost when the browser tab is closed)

# HTMl attributes:
=> name="value"
href="", src="", style="", title="", width="", height="", class="", id=""

# block vs inline elements

  block-level elements in HTML:
  <address>    <article>    <aside>    <canvas>
  <div>		<fieldset>	<figure>	<footer>
  <form>	<h1>-<h6> 	<header> 	<hr>	<li>	<main>	<nav>	<noscript> <p> <pre>
  <section>	<table>	<tfoot>	<ul>	<video>


  inline elements:
  <a>		<abbr>	<span>	<strong>	<acronym>	<b>		<br>	<button>
  <code>	<em>	<i>		<img>	<input>		<label>		<map>	<object>
  <script>	<select>	<small>	<textarea>

# DOM
  The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web.

# Meta elements:
  The <meta> element is typically used to specify the character set, page description, keywords,
  author of the document, and viewport settings.

  The metadata will not be displayed on the page, but is used by browsers (how to display content or reload page),
  by search engines (keywords), and other web services.

  The viewport is the users visible area of a web page. It varies with the device - it will be smaller on a mobile phone
  than on a computer screen.

  ex	=> <meta name="viewport" content="width=device-width, initial-scale=1.0">

  "initial-scale=1.0" => sets the initial zoom level when the page is first loaded by the browser.

  "width=device-width" => sets the width of the page to follow the screen-width of the device.

# Here are the different input types you can use in HTML:

  <input type="button">					<input type="checkbox">
  <input type="color">					<input type="date">
  <input type="datetime-local">	<input type="email">
  <input type="file">						<input type="hidden">
  <input type="image">					<input type="month">
  <input type="number">					<input type="password">
  <input type="radio">					<input type="range">
  <input type="reset">					<input type="search">
  <input type="submit">					<input type="tel">
  <input type="text">						<input type="time">
  <input type="url">						<input type="week">

# What are void elements in HTML?

=> HTML elements which do not have closing tags or do not need to be closed are Void elements.

  For Example <br />, <img />, <hr />, etc.

# id vs class

  class can assign to multiple elements

  id is provide unique-ness for elemnts

# attributes vs properties
  
  - Attributes are defined by HTML.                 Properties are defined by the DOM.
  - The value of an attribute is constant.          The value of a property is variable.


# innerHTML vs InnerText

  innerText returns all text contained by an element and all its child elements. 
  innerHtml returns all text, including html tags, that is contained by an element.

# Tag Description

  <!-- <script> => Defines a client-side script
  <noscript /> => Defines an alternate content for users that do not support client-side scripts -->

**CSS(Cascading Style Sheet)**

Q What is a CSS Preprocessor? What are Sass, Less?

=> A CSS Preprocessor is a tool used to extend the basic functionality of default vanilla CSS
through its own scripting language. 

It helps us to use complex logical syntax like 
– variables, functions, mixins, code nesting, and inheritance to name a few, supercharging your vanilla CSS.

# SASS (Syntactically Awesome Style Sheets) ($)

  SASS syntax 								SCSS Syntax

  $font-color: #fff 						$font-color: #fff;
  $bg-color: #00f								$bg-color: #00f;

  #box										    #box {
    color: $font-color							color: $font-color;
    background: $bg-color						background: $bg-color;
    											        }


**LESS(Leaner Stylesheets) (@)**
  @font-color: #fff;
  @bg-color: #00f

    #box{
    	color: @font-color;
    	background: @bg-color;
    }

- Reset CSS: CSS resets aim to remove all built-in browser styling.
- Normalize CSS: Normalize CSS aims to make built-in browser styling consistent across browsers.

# Pseudo-elements vs Pseudo-class

  * Pseudo-elements => allows to create items that do not normally exist in the document tree.

  ::before
  ::after
  ::first-letter
  ::first-line
  ::selection

  Ex.
  p::first-line {
  color: #ffOOOO;
  font-variant: small-caps;
  }

  * Pseudo-classes => select regular elements but under certain conditions like when the user is hovering over the link.

  :link
  :visited
  :hover
  :active
  :focus

  /_ mouse over link _/
  a:hover {
  color: #FFOOFF;
  }

# Position:
- Static : The element is positioned according to the normal flow of the document.
- Relative : The element is positioned according to the normal flow of the document.
- Absolute : The element is removed from the normal document flow. and space not created.
- fixed : The element is removed from the normal document flow.

**CSS media Types:**

  all => Used for "all media" type devices
  print => Used for "printers"
  screen => Used for computer screens, tablets, smart-phones etc.
  speech => Used for screenreaders that "reads" the page out loud

  Media Query Syntax:

  @media not|only mediatype and (expressions) {
      CSS-Code;
  }

  Ex.
  @media screen and (min-width/max-width: 480px) {
  body {
  background-color: lightgreen;
  }
  }

# Z-index:

  Z-index is used to specify the stack order of elements that overlap each other.

# specificity:
  If there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element.

# CSS Units
  
  https://www.w3schools.com/cssref/css_units.asp

  Absolute length
    Absolute length units are not recommended for use on screen, because screen sizes vary so much. However, they can be used if the output medium is known, such as for print layout.

    Unit	Description
    cm	  centimeters
    mm	  millimeters
    in	  inches (1in = 96px = 2.54cm)
    px *	pixels (1px = 1/96th of 1in)

  Relative Lengths
    Relative length units specify a length relative to another length property. Relative length units scale better between different rendering medium.

  EX => rem,vw, vh,ex,em

# Grid vs Flex

* Grid: Grid was designed for two-dimensional layout - rows, and columns at the same time.

* Flexbox: Flexbox was designed for layout in one dimension - either a row or a column.

  Properties
  - flex
  - flex-basis
  - flex-direction
  - flex-flow
  - flex-grow
  - flex-shrink
  - flex-wrap
  - order

  justify-content
  - align-content
  - align-items
  - align-self
  - place-content
  - place-items
  - row-gap
  - column-gap
  - gap

**Standard Media Queries**
  /_ Extra small devices (phones, 600px and down) _/
  @media only screen and (max-width: 600px) {...}

  /* Small devices (portrait tablets and large phones, 600px and up) */
  @media only screen and (min-width: 600px) {...}

  /* Medium devices (landscape tablets, 768px and up) */
  @media only screen and (min-width: 768px) {...}

  /* Large devices (laptops/desktops, 992px and up) */
  @media only screen and (min-width: 992px) {...}

  /* Extra large devices (large laptops and desktops, 1200px and up) */
  @media only screen and (min-width: 1200px) {...}


#  Center vertically and horizontally

.center-div{
  position: absolute;
  top: 50%;                                  
  left: 50%;  
  transform: translate(-50%, -50%)
}

.center-div{
  display: flex;
  justify-content: center;
  align-items: center;
}

# Box model:
  The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.
  - Content
  - padding
  - border
  - margin