# SCSS | SASS

https://sass-lang.com/guide

## Preprocessing :

If your stylesheets are getting larger, more complex, and harder to maintain, this is where a preprocessor like SASS can help. It lets you use features that don't exist in CSS yet like **variables**, **mixins**, **inheritance** and other things that make writing CSS much easier.

Once you start tinkering with Sass, it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your website.

The most direct way to make this happen is in your terminal. Once Sass is installed, you can compile your Sass to CSS using the sass command. You'll need to tell Sass which file to build from, and where to output CSS to. For example, running sass ```input.scss``` ```output.css``` from your terminal would take a single Sass file, ```input.scss```, and compile that file to ```output.css```.

## Variables :

Yes, you read right, you can put **variables** into a SCSS file.
Think of variables as a way to store information that you want to reuse throughout your whole stylesheet. You can store things like **colors**, **font stacks**, or any CSS value you think you'll want to reuse. Sass uses the ```$``` symbol to make something a variable. Here's an example:

```SCSS
$font-stack:    Roboto, sans-serif;
$primary-color: #FFD500;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```
When the Sass is processed, it takes the variables we define for the ```$font-stack``` and ```$primary-color``` and outputs normal CSS with our variable values placed in the CSS. This can be extremely powerful when working with brand colors and keeping them consistent throughout the site.

```SCSS
body {
  font: 100% Rototo, sans-serif;
  color: #FFD500;
}
```

## Imports :

Sass builds on top of the current CSS ```@import```. But instead of requiring an HTTP request like normal CSS, Sass will take the file that you want to import and combine it with the file you're importing into so you can serve a single CSS file to the web browser.

Imagine that you have two Sass files, ```_reset.scss``` and ```base.scss```. We want to import ```_reset.scss``` into ```base.scss```.

```SCSS
// _reset.scss

html,
body,
ul,
ol {
  margin:  0;
  padding: 0;
}
```

Now we import it into ```_base.scss```

```SCSS
// base.scss

@import 'reset';

body {
  font: 100% Roboto, sans-serif;
  background-color: #FFD500;
}
```

**TIP :** We're using ```@import 'reset';``` in the ```base.scss``` file. When you import a file you don't need to include the file extension ```.scss```, because Sass will figure it out automatically. When you generate the CSS you'll get:

```css
html, body, ul, ol {
  margin: 0;
  padding: 0;
}

body {
  font: 100% Roboto, sans-serif;
  background-color: #FFD500;
}
```
