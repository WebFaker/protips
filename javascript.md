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
![alt text](https://mdn.mozillademos.org/files/9543/hello-world.png "Here's an example.")

## 3. Variables
