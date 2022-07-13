# Exercise 03: CSS Basics

## CSS: Cascading Style Sheets

Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML. CSS describes how elements should be rendered on screen, on paper, or on other media.

CSS is among the core languages of the open web and is standardized across Web browsers according to W3C specifications. Previously, development of various parts of CSS specification was done synchronously, which allowed versioning of the latest recommendations. You might have heard about CSS1, CSS2, CSS3. However, CSS4 has never become an official version.

Like HTML, CSS is not a programming language. It's not a markup language either. CSS is a style sheet language. CSS is what you use to selectively style HTML elements. For example, this CSS selects paragraph text, setting the color to red:

```css
p {
  color: red;
}
```

![mozilla](./images/website-screenshot-styled.png)

---

## Anatomy of a CSS ruleset

Let's dissect the CSS code for red paragraph text to understand how it works :

![css-declaration-small](./images/css-declaration-small.png)

The whole structure is called a ruleset. (The term ruleset is often referred to as just rule.) Note the names of the individual parts:

**Selector**
This is the HTML element name at the start of the ruleset. It defines the element(s) to be styled (in this example, ```html<p>``` elements). To style a different element, change the selector.

**Declaration**
This is a single rule like ```color: red;```. It specifies which of the element's **properties** you want to style.

**Properties**
These are ways in which you can style an HTML element. (In this example, ```color``` is a property of the ```html<p>``` elements.) In CSS, you choose which properties you want to affect in the rule.

**Property value**
To the right of the property—after the colon—there is the property value. This chooses one out of many possible appearances for a given property. (For example, there are many ```color``` values in addition to ```red```.)

*Note the other important parts of the syntax:*

Apart from the selector, each ruleset must be wrapped in curly braces. ({})
Within each declaration, you must use a colon (:) to separate the property from its value or values.
Within each ruleset, you must use a semicolon (;) to separate each declaration from the next one.
To modify multiple property values in one ruleset, write them separated by semicolons, like this:

```css
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

---

## Selecting multiple elements

You can also select multiple elements and apply a single ruleset to all of them. Separate multiple selectors by commas. For example:

```css
p, li, h1 {
  color: red;
}
```

---

## Different types of selectors

There are many different types of selectors. The examples above use element selectors, which select all elements of a given type. But we can make more specific selections as well. Here are some of the more common types of selectors:

**Element selector (sometimes called a tag or type selector) :**
All HTML elements of the specified type.

p selects ```<p>```

**ID selector**
The element on the page with the specified ID. On a given HTML page, each id value should be unique.

```#my-id```
selects ```<p id="my-id"> or <a id="my-id">```

**Class selector**
The element(s) on the page with the specified class. Multiple instances of the same class can appear on a page.

```.my-class``` selects ```<p class="my-class">``` and ```<a class="my-class">```

**Attribute selector**
The element(s) on the page with the specified attribute.

img[src]
selects ```<img src="myimage.png">``` but not ```<img>```

**Pseudo-class selector**
The specified element(s), but only when in the specified state. (For example, when a cursor hovers over a link.)

a:hover
selects ```<a>```, but only when the mouse pointer is hovering over the link.

---

## CSS: all about boxes

Something you'll notice about writing CSS: a lot of it is about boxes. This includes setting size, color, and position. Most HTML elements on your page can be thought of as boxes sitting on top of other boxes.

*CSS layout is mostly based on the box model. Each box taking up space on your page has properties like:*

- padding - the space around the content. In the example below, it is the space around the    paragraph text.

- border - the solid line that is just outside the padding.

- margin - the space around the outside of the border.

![box-model](./images/box-model.png)

In this section we also use:

- width (of an element).

- background-color, the color behind an element's content and padding.

- color, the color of an element's content (usually text).

- text-shadow sets a drop shadow on the text inside an element.

- display sets the display mode of an element.

---

## Exercise

Let's practice styling some sqares. Go to [JS Fiddle](https://jsfiddle.net/).

1). In the ```html``` section create two ```div``` elements.

2). In the fist div, add an ```h1``` element with the text **"Square1"**

3). In the second div, add an ```h2``` element with the text **"Square2"**

4). To each ```div```, add a class and set it equal to square.

5). Paste the following to the ```css``` section.

```css
.square{
  outline: 2px dashed black;
  width: 20vw;
  height: 20vw;
  position: relative;
}
```

6). Make the first ```div``` green by adding an ```id```, setting it equal to ```div1-id```, and pasting the following in the ```css``` section.

```css
#div1-id{
  background-color: green;
}

```

7). Make the background color of the second ```div`` blue.

8). Create squares for the remaining 4 header tags and set the colors to:

```h3``` yellow, ```h4``` red, ```h5``` brown, ```h6``` pink.

9). How would you make the ```h6``` into a circle?

---

Now let's practice learning CSS by styling the Star Wars fan club page we created.[Link](https://yahshemi.github.io/Star-Wars-Fan-Club/index.html).

## Setup

1). Change directory into the new folder:

```sh
cd semanticHtml
```

2). Open VS Code in the current folder.

```sh
code .
```

3). Verify that your index.html looks like the following.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta
      charset="utf-8"
      name="viewport"
      content="width=device-width, initial-scale=1.0"
    />
    <title>Star Wars Fan Club</title>
  </head>

  <body>
    <header>
      <h1>Star Wars</h1>
    </header>
    <section>
      <img src="./images/Star_Wars_Logo.png" alt="starwars logo" />
      <div>
        <h2>Welcome to the<br /><span>Star Wars Fan Club</span></h2>
      </div>
    </section>
    <nav >
      <ul>
        <li><a href="./index.html">Join the club</a></li>
        <li><a href="./index.html">Latest news</a></li>
        <li><a href="./index.html">New shows</a></li>
        <li><a href="./index.html">Contact</a></li>
      </ul>
    </nav>
    <main>
      <article>
        <h2>May the Force be with you</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repudiandae
          possimus sapiente, ducimus asperiores error eum ipsam quasi
          repellendus iste earum laboriosam nesciunt officiis atque rerum quos
          incidunt aspernatur velit voluptates. Lorem ipsum, dolor sit amet
          consectetur adipisicing elit. Praesentium labore perferendis minus
          incidunt doloribus, eligendi repudiandae earum dignissimos est neque
          deserunt consequatur. Repudiandae autem maxime magnam eveniet! Atque,
          suscipit amet. Lorem ipsum, dolor sit amet consectetur adipisicing
          elit. Praesentium labore perferendis minus incidunt doloribus,
          eligendi repudiandae earum dignissimos est neque deserunt consequatur.
          Repudiandae autem maxime magnam eveniet! Atque, suscipit amet.
        </p>
      </article>
      <ul>
        <li><img src="./images/StarWarsPoster1977.jpeg" /></li>
        <li><img src="./images/Mandalorian.jpg" /></li>
      </ul>
    </main>
    <section>
      <h2>Join Today!</h2>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Corporis
        dignissimos minus voluptatem.
      </p>

      <form>
        <input
          type="email"
          name="email"
          placeholder="Type email & hit enter"
          required
        />
      </form>
    </section>
    <footer>
      <p class="copyright">Copyright 2022 Star Wars fan Club</p>
    </footer>
  </body>
</html>

```

4). Create a `styles.css` file.

This is where we will add our CSS rules

```sh
touch styles.css
```

5). Paste the following line in the head of the ```index.html``` file. This will link our html with our css rules

```css
<link rel="stylesheet" href="styles.css">

```

6). Let's verify that our files are linked correctly by creating a CSS rule for the h1.

Paste the following code in the ```styles.css``` file.

```css
h1{
    color: red;
}
```

If you h1 changed from black to red, that means that everything is wired correctly.

---

## Position & Layout

Now lets take a look at how we change change the layout and postion of elements on the page.

The **position** property can have 1 of 5 values

- static - html element have this as a default value
- fixed - positions an element relative to the view port
- relative - shifts the element around, relative to it's original position
- absolute - postions an element absolutely, relative to it's closest parent
- sticky -  a mixture of static and fixed

Let's take a look at static position.

1). In the chrome dev tool, add ```css position: static;``` to the CSS rule for the h1.

Notice that nothing has changes. Static simply puts the element in its normal document flow, which is the default way that documents are displayed. Position static can be used to reset the position of an element that has been previously moved.

2). Now let's take a look at relative. Change the postion from static to relative by copying the following.

```css
 h1{
    color: red;
    position: relative;
    left: 100px;
}
```

Notice the h1 moves away from the left by 100px, relative to its original position.

3). Try moving it away from the top by 100px.

4). Remove the CSS rules for the h1.

5). Now let's add class called banner to the ```html<section>``` element. In the ```index.html file```, modify the ```html<section>``` so it looks like the following.

```html
<section class="banner">
```

6). Make the postion of the banner relative by copying the following into your ```styles.css``` file.

```css
.banner{
  position: relative;
}
```

7). Now let's target the image inside the banner and set the max-width to the 100%.

```css
.banner img{
  max-width: 100%
}
```

This will make it so that the max-width that the image is able to go, is 100% of the parent-div. If a parent-div is not set, then the max width will be 100% of the view-port.

Next we will position the welcome message so that it has an absolute position, relative to the banner. It should sit on top of the image. First we need to verify that the parent does not have a position of ```static```. We did this step when we made the banner ```relative```.

1). Give the ```html div``` that is wrapped around the welcome message a class, and set it equal to "welcome". It should look like the following.

```html
<div class="welcome">
```

2). Inside the css paste the following:

```css
.banner .welcome{
  position: absolute;
  left: 0px;
  top: 30%
}
```

---

Our fan page still needs more styling, but let's stop here, and save our code.

## Push to Github

1). Add your files.

2). Make your commit.

3). Push to Github.
