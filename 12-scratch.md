# EXERCISE 12: Scratch

## Description

This Exercise introduces [Scratch](https://scratch.mit.edu/)
Scratch is a high-level block-based visual programming language and website aimed primarily at children as an educational tool for programming, with a target audience of ages 8 to 16. Users on the site, called Scratchers, can create projects on the website using a block-like interface













Now that you are familiar with Karel and it's commands, your objective is to modify the function to complete a set of exercises.

If you haven't completed the previous lesson which introduces Karel and how to use it, go [back](https://creating-coding-careers.gitbook.io/the-basics/10-karel-the-robot) and do so.

We mentioned before that Karel has a set of commands that it follows.

1. Move (moves Karel 1 space forward in the direction she's facing)
2. Turn Left (turns Karal 90 degrees to the left)
3. Pick Beeper (Karel picks up beeper)
4. Put Beeper (Karel puts down beeper)

There's also

1. Turn right (turns Karal 90 degrees to the right)
2. Turn around (Karel turns 180 degrees)
3. Paint Corner

You can acces the command by click the `Reference` button in the top-right corner of the page.

---

### Let's get started

Let's start by going to [Stanford Karel](https://stanford.edu/~cpiech/karel/ide.html) and changing Karel's world to `5x5`.

1\). Move Karel to the center of the grid, put a beeper down, then return to the starting position.

[Beeper Center](./.gitbook/assets/beeper-center.png)

Good job!

2\). Move Karel to the top-right corner of the grid and put a beeper down. Return to the starting position.

[Beeper-Top-Right](./.gitbook/assets/beeper-top-right.png)

By now, you're probable tired of entering all those command, especially the ones that repeat themselves. When programming, it's not a good idea to repeat yourself when you don't have to. We can shorten the ammount of code we write by creating functions that contains the commands we want Karel to perform. Whenever we want Karel to perform those commands we can call the functions. For example:

Let's say we wanted Karel to go around the perimeter of the grid. We know that on a `5x5` grid, Karel needs to move `4`, turn left, the repeat `3` times. Since the commands repeat themselves, we can just add them to our function.

3\). Above the `main` function create a function called `getToCorner`. In that function is where we'll add our commands. It should look like the the following.

```text
function getToCorner(){

}
```

Inside the function, add the following.

```text
move();
move();
move();
move();
turnLeft();
```

In the `main` function call the function `4` times. Since

```text
getToCorner();
getToCorner();
getToCorner();
getToCorner();
```

Notice, Karel made it around the grid with less code this time.

4\). Now switch Karel's world from `4x4` to `15x15` and move Karel from the bottom-left corner of the grid to the top-right corner of the grid in a diagonal direction.

---

### Bonus

Switch the world to the `maze`. Complete the maze and bring the beeper back to the starting position.
