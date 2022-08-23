# EXERCISE 14: Snake Workshop

## Description

This workshop will walk us through creating a Snake Game. The game is built with Javascript and the purpose is to see and understand the different functions and components necessary to create the game.

JavaScript is a text-based programming language that allows you to make web pages interactive. JavaScript adds functionality to elements to engage users.

The object of Snake is to safely navigate a snake and eat as many apples as possible without touching the snake’s body or the walls.

![Snake Game]()

---

## Let's get started

### Create the stage and the snake

1\. Go to [Code Pen](https://codepen.io/) and click the `Start Coding` button.

We need to create a stage and the snake.

2\. Paste the folllowing in the section labeled `HTML`.

```html
<canvas id="gameStage" width="400" height="400"><canvas>
```

The `id="gamestage"` is a unique identifier for the stage. We can use this `id` when we need to target the stage.
The stage doesn't display bby default. We'll need to add some style before we can interact with it.

3\. In the section titled `CSS`, add the following.

```css
#gamestage {
         position: absolute;
         top: 50%;
         left: 50%;
         transform: translate(-50%, -50%);
}

```

4\. In the JS section, add the following

```js
    const board_border = 'black';
    const board_background = "white";
    const snake_col = 'lightblue';
    const snake_border = 'darkblue';
```

---

### Add the Obstacle

.

---

### Stop the game

---

### Keep Score

---

### Bonus
