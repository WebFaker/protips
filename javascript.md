# JavaScript

## 1. In brief

JavaScript (also called "JS") is a full-fledged dynamic programming language that, when applied to an HTML document, can provide dynamic interactivity on websites, like carousels, image galleries, fluctuating layouts, and responses to button clicks. With more experience, you'll be able to create games, animated 2D and 3D graphics, comprehensive database-driven apps, and much more.

## 2. Getting started

- First, go to your test site and create a new folder named 'scripts' (without the quotes). Then, within the new scripts folder you just created, create a new file called main.js. Save it in your scripts folder.
- Next, in your index.html file enter the following element on a new line just before the closing </body> tag: 
```HTML
<script src="scripts/main.js"></script>
```
- This is basically doing the same job as the <link> element for CSS — it applies the JavaScript to the page, so it can have an effect on the HTML (along with the CSS, and anything else on the page).
- Now add the following code to the main.js file: 
```JS
var header = document.querySelector('h1');
header.textContent = 'Hello world!';
```
- Finally, make sure the HTML and JavaScript files are saved as usual, then load index.html in the browser. You should see something like the following:

![alt text](https://cdn-images-1.medium.com/max/1600/1*cY2ahrsNP_gUtQKYlaUvZw.png "Here's an example.")

## 3. Variables

Variables are containers that you can store values in. You start by declaring a variable with the `var` keyword, followed by any name you want to call it:

```JS
var awesomeVariable;
```

After declaring a variable, you can give it a value:

```JS
awesomeVariable = 'Bob';
```

You can do both these operations on the same line if you wish:

```JS
var awesomeVariable = 'Bob';
```

You can retrieve the value by just calling the variable by name:

```JS
awesomeVariable;
```

After giving a variable a value, you can later choose to change it:

```JS
var myVariable = 'Bob';
myVariable = 'Steve';
```

Note that variables may hold values that have different data types, like `numbers`, `boolean`, `array`, etc...

## 4. Comment your code

You can put comments into JavaScript code, just like in CSS:

```JS
/*
Everything in between is a comment.
*/
```

If your comment contains no line breaks, it's easier to put it behind two slashes :

```JS
// This is a comment
```

## 5. Operators

An `operator` is a mathematical symbol which produces a result based on two values (or variables). In the following table you can see some of the simplest operators, along with some examples to try out in the JavaScript console.
You can do additions, substractions, and all the other things you do in maths.

## 6. Conditionals

Conditionals are code structures which allow you to test if an expression returns true or not, running alternative code revealed by its result. A very common form of conditionals is the `if ... else` statement. For example:

```JS
var iceCream = 'chocolate';
if (iceCream === 'chocolate') {
  alert('Yay, I love chocolate ice cream!');    
} else {
  alert('Awwww, but chocolate is my favorite...');    
}
```

The expression inside the `if ( ... )` is the test — this uses the identity operator (as described above) to compare the variable `iceCream` with the string `chocolate` to see if the two are equal. If this comparison returns `true`, the first block of code is run. If the comparison is not true, the first block is skipped and the second code block, after the `else` statement, is run instead.

## 7. Functions 

Functions are a way of packaging functionality that you wish to reuse. When you need the procedure you can call a function, with the function name, instead of rewriting the entire code each time. You have already seen some uses of functions above, for example:

    ```JS
    var myVariable = document.querySelector('h1');
    ```

    ```JS
    alert('hello!');
    ```

These functions, `document.querySelector` and `alert`, are built into the browser for you to use whenever you desire.

If you see something which looks like a variable name, but has parentheses — `()` — after it, it is likely a function. Functions often take arguments — bits of data they need to do their job. These go inside the parentheses, separated by commas if there is more than one argument.

For example, the `alert()` function makes a pop-up box appear inside the browser window, but we need to give it a string as an argument to tell the function what to write in the pop-up box.

The good news is you can define your own functions — in this next example we write a simple function which takes two numbers as arguments and multiplies them:

```JS
function multiply(num1,num2) {
  var result = num1 * num2;
  return result;
}
```

Try running the above function in the console, then test with several arguments. For example:

```JS
multiply(4,7);
multiply(20,20);
multiply(0.5,3);
```

## 8. Events 

Real interactivity on a website needs events. These are code structures which listen for things happening in browser, running code in response. The most obvious example is the click event, which is fired by the browser when you click on something with your mouse. To demonstrate this, enter the following into your console, then click on the current webpage:

```JS
document.querySelector('html').onclick = function() {
    alert('Ouch! Stop poking me!');
}
```

There are many ways to attach an event to an element. Here we select the <html> element, setting its onclick handler property equal to an anonymous (i.e. nameless) function, which contains the code we want the click event to run.

Note that

```JS
document.querySelector('html').onclick = function() {};
```

is equivalent to

```JS
var myHTML = document.querySelector('html');
myHTML.onclick = function() {};
```

It's just shorter.
