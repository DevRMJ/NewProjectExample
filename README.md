## New Project Example
## Introduction

Thinking back to my days as a junior and not knowing much, I remember the one thing that always held me back. I never knew where to begin, how do I start a new project? How do I get that starting point and then continue from there onward? This article is a small tutorial on just how to get started with a basic shell of a project. 

This article will assume you are on a Microsoft Windows machine unless stated otherwise.

Let's get started

## Step by Step

Create a new folder somewhere that you will run your projects from. I prefer one of two options:

- Create a '`development`' folder on my C:/ drive
- Create a '`development`' folder on another partition or external HDD

> Normally at this stage, I would create a new project with GIT in [Bitbucket](https://bitbucket.com) or [GitHub](https://github.com), but in this tutorial, I will skip source control as this is a more advanced topic to discuss.

Let's create a new folder in our '`development`' folder which we just created. Let's call this new folder '`HelloWorld`' as it is customary to create our '`HelloWorld`' application as our first project. 

Next, open the folder in your favourite IDE or text editor. I prefer Visual Studio Code over other text editors due to its rich features and performance. 

![fileNewProject_vscode.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598285416471/anHld2Su5.png "vs code editor when you open it the first time")
You will now see something similar to this in your text editor.

Now let's create the structure of our first project.

We will need the following: 

- An index.html page. This will be our first page that loads when our website loads.
- A folder for all our `cascading style sheets(CSS)`. This will contain all our `CSS`. This will hold all the files that make our website look pretty.
- A folder for all our JavaScript files. This will contain all script files that will be in use by our website.

First, we will create the **index.html** page. Now the index page cannot just be empty. Every HTML page must have the standard format and skeleton of an HTML page. This includes the '`DOCTYPE`', '`head`' and `body`. Now we need to add this to our `index.html` as seen below.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HelloWorld</title>
</head>

<body>
    <h1>Hello World!</h1>
    <p>This is my first web application</p>
</body>

</html>
```

This is the basic shell of your `index.html` page. 

Next, we will create two folders in our project, one called `scripts` and one called `content`. The `content` folder will become the home for all your `CSS` and the `scripts` folder will become the home of all your `JavaScript` files. 


![fileNewProject_projectlayout.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598285437381/Ngn8X2jW4.png "project with content folder example")

This is the general idea of how your project folder would look at this stage if you followed all instructions.

Now that we have our basic structure lets go one step further and see how all this connects.

Create a new `JavaScript` file in the `scripts` folder and call it `index.js`. Now add this file to your `index.html`  to tell your browser that we need this file and that it must be loaded. We will add only `<script src="scripts/index.js"></script>` to the file to let the browser know that it must load this file.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HelloWorld</title>

    <script src="scripts/index.js"></script>
</head>

<body>
    <h1>Hello World!</h1>
    <p>This is my first web application</p>
</body>

</html>
```

In `index.js` we will just put something simple to know its there and loaded.

```javascript
console.log("Hello World!");
```

This will write to your developer console `Hello World!` when the `index.js` file has loaded. Now open up your `index.html` in the browser. You will see nothing for the moment but if you open up your developer tools, by pressing F12, and navigating to the `console` area you will see a `HelloWorld!` message. 

Let's get something onto the page to load and to make it pretty!

Create a new `CSS` file in your contents folder and call it `styles.css`. Now to add the stylesheet to `HTML` to allow the browser to load our stylesheet. We will need to add `<link rel="stylesheet" href="content/styles.css" />` to our `HTML` to allow the browser to load our `CSS`

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>HelloWorld</title>

    <script src="scripts/index.js"></script>
    <link rel="stylesheet" href="content/styles.css" />
</head>

<body>
    <h1>Hello World!</h1>
    <p>This is my first web application</p>
</body>

</html>
```

We will create a little dark mode stylesheet by adding the CSS below to our stylesheet.

```css
body {
    background: black;
    /* Changes the entire background color to black */
}

h1 {
    color: white;
    /* Changes the text color of all H1 tags to white */
}

p {
    color: gray;
    /* Changes the text color of all p tags to gray */
}
```

## Conclusion

That's all there is to it. We got to create our first 'skeleton' project and added some basics to it. Hope this helped someone else as this would have helped past me. 

Happy coding :)

o/
