# EXERCISE 03: Loops

In this lesson, we will take a look at what JavaScript loops are. We will also go over the syntax and use cases for a For Loop.

---

## What are Loops?

Loops provide a quick and easy way to repeatedly run a command.

```javascript
for (let i = 0; i < 6; i++) {
  // Runs 6 times, with values of step 0 through 5.
  console.log('Plus 1');
}

```

In Javascript there are many different kinds of loops however, but they all do essentially the same thing, which is repeat an action a number of times. (Keep in mind that it's possible that number could be zero!)

---

## `for` Loops

A `for` loop will repeats until a condition is false. A `for` loop looks like this:

```javascript
for ([initialExpression]; [conditionExpression]; [incrementExpression]) {
  statement
  }
```

- The inital expression is executed (one time) before the execution of the code block.

- The condition expression defines the condition for executing the code block.

- The increment expression is executed (every time) after the code block has been executed.

```javascript
for (let i = 0; i < 7; i++) {
  text += "The number is " + i + "<br>";
}
```

From the example above, you can read:

The first section sets a variable before the loop starts (let i = 0).

The second section defines the condition for the loop to run (i must be less than 7).

The third section increases a value (i++) each time the code block in the loop has been executed.

When a `for` loop executes, the following occurs:

1. The initializing expression `initialExpression`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.

2. The `conditionExpression`  is evaluated. If the value of `conditionExpression` is true, the loop statements execute. If the value of `condition` is false, the `for` loop terminates. (If the `condition` expression is omitted entirely, the condition is assumed to be true.)

3. The `statement` executes. To execute multiple statements, use a block statement (`{ ... }`) to group those statements.

4. If present, the update expression `incrementExpression` is executed.

5. Control returns to Step 2.

### Example

In the example below, the function contains a `for` statement that counts the number of selected options in a scrolling list (a `<select>` element that allows multiple selections). The for statement declares the variable `i` and initializes it to 0. It checks that `i` is less than the number of options in the `<select>` element, performs the succeeding if statement, and increments `i` by 1 after each pass through the loop.

```javascript
<form name="selectForm">
  <p>
    <label for="musicTypes">Choose some music types, then click the button below:</label>
    <select id="musicTypes" name="musicTypes" multiple="multiple">
      <option selected="selected">Pop</option>
      <option>Dance</option>
      <option>HipHop</option>
      <option>Alternative</option>
      <option>Classical</option>
      <option>Contemporary</option>
    </select>
  </p>
  <p><input id="btn" type="button" value="How many are selected?" /></p>
</form>

<script>
function howMany(selectObject) {
  let numberSelected = 0;
  for (let i = 0; i < selectObject.options.length; i++) {
    if (selectObject.options[i].selected) {
      numberSelected++;
    }
  }
  return numberSelected;
}

let btn = document.getElementById('btn');
btn.addEventListener('click', function() {
  alert('Number of options selected: ' + howMany(document.selectForm.musicTypes));
});
</script>

```

---

## `do while` Statement

The `do...while` statement will continue to repeats until a specified condition evaluates to false.

Below is an example.

```js
do
  statement
while (condition);

```

The statement is always executed once before the condition is checked. In order to execute multiple statements, use a block statement (`{ ... }`) to group those statements together.

If the `condition` is true, the statement executes again. At the end of every execution, the condition is checked. When the condition is `false`, execution stops, and control passes to the statement following `do...while`.

### Example 2

In the following example, the `do` loop iterates at least once and reiterates until `i` is no longer less than 9.

```js
let i = 0;
do {
  i += 1;
  console.log(i);
} while (i < 9);
```

---

## `while` statement

A `while` statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:

```js
while (condition)
  statement
```

If the condition becomes `false`, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns `false`, execution stops, and control is passed to the statement following `while`.

To execute multiple statements, use a block statement (`{ ... }`) to group those statements.

### Example 3

The following `while` loop iterates as long as n is less than 3:

```js
let y = 0;
let z = 0;
while (y < 3) {
  y++;
  z += y;
}
```

With each iteration, the loop increments `y` and adds that value to `z`. Therefore, `z` and `y` take on the following values:

After the first pass: y = 1 and z = 1
After the second pass: y = 2 and z = 3
After the third pass: y = 3 and z = 6
After completing the third pass, the condition y < 3 is no longer true, so the loop terminates.

### Example 4

Avoid infinite loops. Make sure the condition in a loop eventually becomes false—otherwise, the loop will never terminate! The statements in the following while loop execute forever because the condition never becomes false:

```js
// Infinite loops are not good!
while (true) {
  console.log('Hello, world!');
}
```
