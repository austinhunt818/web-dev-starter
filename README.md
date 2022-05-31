# lesson04

## Overview

In this lesson we are going to review the project layout that we will be using for the first half of
the semester. This project is all setup to make it easy to write and debug HTML, CSS, and
Javascript. In this lab your only objective is to go through each task and make sure your system
is all setup to start doing web development!

## Videos

- [Lab Overview]()
- [VSCode and Git Installed](https://www.youtube.com/watch?v=lix7G-S8ox8)
- [Class Coding standards](https://shanep-web.github.io/docs/coding-standards.html)
- [Cloning and Submitting](https://shanep-web.github.io/docs/github.html)


## Task 1 - Run the site

In order to run the website using the built in development server use the following steps:

```bash
$ npm install
$ npm start
```

Assuming the two commands above completed successfully you should see the starter webpage open up
in a browser. There are several cool features of the development server that will make your life
easier when authoring web pages. The development server will reload your browser window when it
detects changes! This means you can live in your editor, make changes to your HTML, CSS, or 
javascript files and those changes will automatically be reflected in the browser!

Let's test this out by modifying **index.html** to the following:

```html
<!doctype html>
<html>

<head>
  <meta charset="utf-8">
  <title></title>
  <meta name="description" content="">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="css/style.css">
  <link rel="stylesheet" href="https://code.jquery.com/qunit/qunit-2.19.1.css">
</head>

<body>
  <h1>HTML Rocks!</h1>
  <img src="img/compile.jpeg">
  <script type="module" src="js/main.js"></script>
  <!--
  <div id="qunit"></div>
  <div id="qunit-fixture"></div>
  <script src="https://code.jquery.com/qunit/qunit-2.19.1.js"></script>
  <script src="js/test.js"></script>
  -->
  
</body>

</html>
```

Assuming everything is working correctly you should see your webpage update without having to hit
the refresh button 😊!

## Task 2 - Debugging Javascript

We are going to make a few small modifications to the starter code and then make sure we can use
the built in debugger for VSCode! Generally speaking it doesn't make much sense to single step
through your HTML or CSS code, but any Javascript code can be debugged just like any other
programming language. 

- Step 1: Run your development server with `npm start`
- Step 2: Open the file **js/main.js**
- Step 3: Open the built-in [debugger](https://code.visualstudio.com/docs/editor/debugging)
- Step 4: Click on the debug icon in VSCode and then click the big green arrow that says "Launch
  Chrome against localhost" to start a debugging session. 
- Step 5: Modify the loaded function as shown below.
- Step 6: Set a breakpoint on the variable foo and refresh.
- Step 7: Step through the code to see the changes

```javascript
/**
 * Example function to test our debugger
 */
function loaded() {
    let foo = 1;
    let bar = 2;
    let foobar = foo + bar;
    console.log("Loaded main.js: foo + bar = " + foobar);
}
```

You can also use the built in Chrome debugger to debug your in Browser Javascript. However, it is
much easier to keep everything in VSCode instead of bouncing back and forth between your text editor
and browser. 

## Task 3 - Linting

Javascript is a interpreted language. This means we don't have to compile it like Java or C#, we
write it and then just run it directly. This means that any errors that we have will be found at
runtime. Even though we don't have a compiler to help us there are still tools available to help
us write better code. In this class we will be using [eslint](https://eslint.org/). You will be
required to fix **ALL** eslint errors in any code that you submit. Some errors are just style errors
while others will cause issues at runtime.

## Task 4 - Documentation

We will be using [JSDoc](https://jsdoc.app/) for all of our JavaScript code in this class. You are
required to document all your code just like you were in CS121 and CS221. For the code that we write
in this class JSDoc is almost identical to JavaDoc. Read the short [getting started
guide](https://jsdoc.app/about-getting-started.html) for all the details in using JSDoc.

## Task 5 - Running Grading Scripts

For each lab you will be given a set of grading scripts that you should run. These scripts are
[QUnit](https://qunitjs.com/intro/#in-the-browser) tests that are run in the browser. All you have
to do is uncomment them and they will run automatically! You can debug your unit tests just like
any other Javascript program as shown in Task 2.

```html
<!doctype html>
<html>

<head>
  <meta charset="utf-8">
  <title></title>
  <meta name="description" content="">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="css/style.css">
  <link rel="stylesheet" href="https://code.jquery.com/qunit/qunit-2.19.1.css">
</head>

<body>
  <h1>HTML Rocks!</h1>
  <img src="img/compile.jpeg">
  <script type="module" src="js/main.js"></script>

  <div id="qunit"></div>
  <div id="qunit-fixture"></div>
  <script src="https://code.jquery.com/qunit/qunit-2.19.1.js"></script>
  <script src="js/test.js"></script>
  
</body>

</html>
```

## Task 6 - Complete the Retrospective

Once you have completed all the tasks open the file **Retrospective.md** and complete each section
with a TODO comment. 

## Task 7 - Add, Commit, Push your code

Once you are finished you need to make sure that you have pushed all your code to GitHub for
grading!

