# EXERCISE 13: CSS Review

## Description

For this exercise we will review what CSS is and how we can implement it in our projects. Write out each step

## Let's get started

Let's practice styling some sqares.

1\. Go to [Code Pen](codepen.io) and click the `Start Coding` button.

In the ```HTML``` section create two ```div``` elements.

They should look like the following

```html
<div></div>
<div></div>
```

2\. In the fist div, add an ```h1``` element with the text **"Square1"**

```html
<div>
    <h1>Square1</h1>
</div>
<div></div>
```

3\. In the second div, add an ```h2``` element with the text **"Square2"**

```html
<div>
    <h1>Square1</h1>
</div>
<div>
    <h2>Square2</h2>
</div>
```

4\. To each ```div```, add a class and set it equal to square.

```html
<div class="square">
    <h1>Square1</h1>
</div>
<div class="square">
    <h2>Square2</h2>
</div>
```

5\. Paste the following to the ```css``` section. This section will add the style to our elements.

```css
.square{
  outline: 2px dashed black;
  width: 20vw;
  height: 20vw;
  position: relative;
}
```

6\. Make the first ```div``` green by adding an ```id```, setting it equal to ```square1```, and pasting the following in the ```css``` section.

```css
#square1{
  background-color: green;
}
```

 You should end up with the following

HTML

```html
<div id="square1" class="square">
    <h1>Square1</h1>
</div>
<div class="square">
    <h2>Square2</h2>
</div>
```

CSS

```css
.square{
  outline: 2px dashed black;
  width: 20vw;
  height: 20vw;
  position: relative;
}
#square1{
  background-color: green;
}
```

7\. Try making the background color of the second ```div`` blue on your own.

8\. Create squares for the remaining 4 header tags and set the colors to:

```h3``` yellow, ```h4``` red, ```h5``` brown, ```h6``` pink.

9\. Turn the squares into circle. You'll have to search Google to find the answer.

---
