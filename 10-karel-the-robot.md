# EXERCISE 10: Karel the Robot

## Description

We mentioned before that HTML provides the content for the page, CSS provides the layout and structure of the page, and Javascript provides the functionality. We write functions to carry out the set of actions we want completed. In this exercise we'll learn about writing functions using [Karel the Robot](https://stanford.edu/~cpiech/karel/ide.html) from Stanford.

Karel is an IDE (Intergrated Development Environment), created by Stanford graduate Rich Pattis to help students learn the fundamentals of programming.

Karel was named after the Czech playwright Karel Čapek. Čapek's 1923 play, Rossum’s Universal Robots gave the word robot to the English language.

---

### Karel’s world

Karel lives in a grid-like world defined by rows and columns. Each intersection of a row and a column is called a corner. Karel can only be positioned on corners and must be facing one of the four standard compass directions (north, south, east, west). A sample Karel world is shown below. Here Karel is located at the corner of 1st row and 1st column, facing east.

![Karel](./images/kareltherobot.png)

---

### Let's get started

1\). Go to [Stanford Karel](https://stanford.edu/~cpiech/karel/ide.html).

You'll see a function like this.

```js
function main(){
   //your code here
}
```

The example above is a function declaration. To create a function, you first write the keyword `function`, next is the name of the function. In this case it's `main`. Followed by

```js
(){

}
```

The space between the two curly brackets is where your code will go. The code will run, whenever the **green play button** is clicked.

![Runs Code](./images/runscode2.png)

This executes the function.

![Karel](./images/karel.png)

---

### Karel's commands

Karel has a `Reference` sheet that has some buit-in commands, conditions, loops , etc. The commands are

1. Move (moves Karel 1 space forward in the direction she's facing)
2. Turn Left (turns Karal 90 degrees to the left)
3. Pick Beeper (Karel picks up beeper)
4. Put Beeper (Karel puts down beeper)

There's also

1. Turn right (turns Karal 90 degrees to the right)
2. Turn around (Karel turns 180 degrees)
3. Paint Corner

---

Now let's give it a try.
1\) Let's start by changing the `World` to `4 x 4` to make it easier to work with.
2\) We'll move Karel to the top-right corner of the page, by adding the following lines in the function and clicking Run.

```text
move();
move();
move();
turnLeft();
move();
move();
move();
```

Great!

Now try this on your own.

Get back to the starting position in the bottom left corner, but  go diagonally.

---

Great!

Now that you know how to use the robot. Switch the `World` to `maze` and solve the maze.

![Maze](./images/maze.png)

Great job! You're on your way to becoming a programmer.
