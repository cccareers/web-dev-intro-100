# Exercise 2: Semantic HTML

## Semantics

In programming, Semantics refers to the meaning of a piece of code — for example "what effect does running that line of JavaScript have?", or "what purpose or role does that HTML element have" (rather than "what does it look like?".)

In HTML, for example, the ```<h1>``` element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

A semantic element clearly describes its meaning to both the browser and the developer.

Examples of non-semantic elements: ```<div>``` and ```<span>``` - Tells nothing about its content.

Examples of semantic elements: ```<form>```, ```<table>```, and ```<article>``` - Clearly defines its content.

```html

<h1>This is a top level heading</h1>

```

By default, most browser's user agent stylesheet will style an ```<h1>``` with a large font size to make it look like a heading (although you could style it to look like anything you wanted).

On the other hand, you could make any element look like a top level heading. Consider the following:

```html

<span style="font-size: 32px; margin: 21px 0;">Is this a top level heading?</span>

```

This will render it to look like a top level heading, but it has no semantic value, so it will not get any extra benefits as described above. It is therefore a good idea to use the right HTML element for the right job.

HTML should be coded to represent the data that will be populated and not based on its default presentation styling. Presentation (how it should look), is the sole responsibility of CSS.

Many web sites contain HTML code like: ```<div id="nav">``` ```<div class="header">``` ```<div id="footer">``` to indicate navigation, header, and footer.

In HTML there are some semantic elements that can be used to define different parts of a web page:
Below is a list of some of the semantic elements in HTML.

> ```<article>``` - Defines independent, self-contained content
> ```<aside>``` - Defines content aside from the page content
> ```<details>``` - Defines additional details that the user can view or hide
> ```<figcaption>``` - Defines a caption for a ```<figure>``` element
> ```<figure>``` - Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
>```<footer>``` - Defines a footer for a document or section
>```<header>``` - Specifies a header for a document or section
>```<main>``` - Specifies the main content of a document
>```<mark>``` - Defines marked/highlighted text
>```<nav>``` - Defines navigation links
>```<section>``` - Defines a section in a document
>```<summary>``` - Defines a visible heading for a ```<details>``` element
>```<time>``` - Defines a date/time

---

## HTML ```<section>``` Element

The ```<section>``` element defines a section in a document.

```html
<section>
<h1>WWF</h1>
<p>The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.</p>
</section>

<section>
<h1>WWF's Panda symbol</h1>
<p>The Panda has become the symbol of WWF. The well-known panda logo of WWF originated from a panda named Chi Chi that was transferred from the Beijing Zoo to the London Zoo in the same year of the establishment of WWF.</p>
</section>
```

## HTML ```<article>``` Element

The ```<article>``` element specifies independent, self-contained content.

An article should make sense on its own, and it should be possible to distribute it independently from the rest of the web site.

Examples of where the ```<article>``` element can be used:

> Forum posts
> Blog posts
> User comments
> Product cards
> Newspaper articles

```html
<article>
<h2>Google Chrome</h2>
<p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
</article>

<article>
<h2>Mozilla Firefox</h2>
<p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
</article>

<article>
<h2>Microsoft Edge</h2>
<p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
</article>
```

## HTML ```<footer>``` Element

The ```<footer>``` element defines a footer for a document or section.

A ```<footer>``` element typically contains:

> authorship information
> copyright information
> contact information
> sitemap
> back to top links
> related documents
> You can have several ```<footer>``` elements in one document.

```html
<footer>
  <p>Author: Your Name</p>
  <p><a href="mailto:yourname@example.com">yourname@example.com</a></p>
</footer>
```

---

## Exercise

Now that we have  a good idea of what Semantic Elements are and how to use them, dulicate this simple static site. [Link](https://yahshemi.github.io/Star-Wars-Fan-Club/index.html). Let's do the set up together.

## Setup

1). Create a new folder;

```sh
mkdir semanticHtml
```

2). Change directory into the new folder:

```sh
cd semanticHtml
```

3). Create a `index.html` file from the terminal, using the following command.

```sh
touch index.html
```

4). Create a `images` folder from the terminal, using the following command.

```sh
mkdir images
```

5). Open VS Code in the current folder.

```sh
code .
```

6). Save the images from the `lesson-6-images` folder in this repository and pull them into the `images` folder.

7). Paste the following code in the ```index.html``` file.

```html
<!DOCTYPE html>
<html> 
    <head>
            
    </head>
    <body>

    </body>
</html>
```

8). Add the following lines to the ```<head>``` tag.

```html
<meta charset="utf-8" name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Star Wars Fan Club</title>
```

---

## Commit your work

1). Initialize a version control (git) for your project.

```sh
git init
```

2). Add your initial files

```sh
git add .
git commit -m "adds initial files"
```

---

Perfect. Now continue to build the site on your own. Remember to use the resources at you disposal like the chrome dev tools.

It should have:

1. A header tag with with a h1

2. A section tag that contains the Star Wars Logo

3. An h2 with Welcome to the Star Wars Fan Club

4. Nav links

5. A main tag that contains an article
Good Luck.

6. An unordered list with the images as list items

7. A section tag with a paragragh tag

8. A form with an email input

9. A footer

---

## Push to Github

1. Add your files.

2. Make your commit.

3. Create a repository on Github.

4. Follow the steps provided.
