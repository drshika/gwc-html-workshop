# Workshop #1 - HTML Hello World!
## Girls Who Code Club @ Dekalb Library

Today we're going to learn how to build a basic HTML website.

## What is HTML?

HTML, which stands for Hypertext Markup Language, helps to organize and categorize content on a website. HTML is made up of elements, which are represented by tags. Tags tell the browser how to display the content on the page. Tags also can have attributes, which are used to provide additional information about the element.

## How do you organize your content?

Sectioning tags help us create the larger structure of our website by dividing our content into sections (sort of like a beginning, middle, and end). We can use these tags to group elements together based on where they live on the webpage.

- The `<body>` tag holds the content of an HTML document. There can only be one `<body>` tag.
- The `<nav>` tag holds the navigation bar in an HTML document.
- The `<header>` tag holds the introductory content in an HTML document.
- The `<main>` tag holds the dominant content of the `<body>` of an HTML document. There can only be one `<main>` tag on a page. We don't want to put anything in here that repeats on other pages, like the navigation bar.

## Simple HTML Structure

Start by creating an index.html file in this directory. 

If you're doing this in Github Codespaces or VS Code, you can create a new file by clicking the `+` button on the left sidebar and selecting `New file`.
![Github Codespaces New File](./images/vscode-new-text-file.png)

If you're doing this in Trinket, you can create a new file by clicking the `+` button on the left sidebar and selecting `New file`.
![Trinket New File](./images/trinket-new-text-file.png)

1. Add the doctype declaration: `<!DOCTYPE html>`
    - This tells the browser that this is an HTML document.
2. Add the html tag: `<html lang="en">`
    - This is the root element of the HTML document. It also sets the language of the document to English.
3. Add the head tag: `<head>`
    - This is the container for the metadata of the HTML document.
4. Within the head tag, add the meta tag: `<meta charset="UTF-8">` and `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
    - The charset attribute is used to specify the character encoding of the document.
    - The viewport attribute is used to specify the viewport of the document.
5. Add the body tag: `<body>`
    - This is the container for the content of the HTML document.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    hello world
</body>
```

That should look like this:

![HTML Structure](./images/demo1.png)

Congratulations! You've just created your first HTML document and said hello to the world! Now let's give your site a fun name.

## Adding a Title

The `<title>` tag is used to specify the title of the HTML document. When you hover over the tab of the browser, you'll see the title of the page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drshika's Awesome Website!</title>
</head>
<body>
    hello world
</body>
```

## Styling

The website looks a bit plain right now. Let's add an external stylesheet to make it look a bit nicer.

Add these two lines to the head tag. This will load the external stylesheet and font when the page loads.
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
<link rel="stylesheet" href="https://fonts.xz.style/serve/inter.css">
```

Let's add our website title and give it a fun color.

- The `<header>` tag is used to create a header for the webpage.
- The `<h1>` tag is used to create a heading for the webpage.
    - The `style` attribute is used to specify the style of the element.
    - The `color` property is used to specify the color of the text.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drshika's Awesome Website!</title>   
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
    <link rel="stylesheet" href="https://fonts.xz.style/serve/inter.css">
</head>
<body>
    <header>
        <h1 style="color: #008B8B;">Drshika's Awesome Website!</h1>
    </header>
</body>
```

That should look like this:

![Styling](./images/demo2.png)

## Adding Content

We can also start to add some information to our webpage. Let's start by adding our school name and and some fun facts about ourselves.

- The `<p>` tag is used to create a paragraph of text.
- The `<a>` tag is used to create a hyperlink.  
    - The `href` attribute is used to specify the URL of the page to link to.
- The `<ul>` tag is used to create an unordered list.
- The `<li>` tag is used to create a list item.

```html
<body>
    <header>
        <h1>Drshika's Awesome Website!</h1>
    </header>
    <p>I'm currently a 17th grader at the <a href="https://www.bklynlibrary.org/">Brooklyn Public Library's</a> Girls Who Code Club.</p>
    <p>Some fun facts about me:</p>
    <ul>
        <li>I love to eat pesto pasta</li>
        <li>My favorite TV show is <a href="https://www.apple.com/tv-plus/series/severance/">Severance</a></li>
        <li>My favorite sport is swimming</li>
    </ul>
</body>
```

That should look like this:

![Content](./images/demo3.png)

## Adding Images

The `<img>` tag is used to embed an image in an HTML document. Let's add an image of our favorite animal to our webpage. Mine is a penguin. Make sure to add the `alt` attribute to the image. This information is important for people who use screen readers to navigate the web.

```html 
<img src="https://www.pewtrusts.org/-/media/post-launch-images/2022/11/gettyimages1198849037jpgmaster/16x9_m.jpg" alt="Three baby emperor penguin chicks.">
```

That should look like this:

![Images](./images/demo4.png)  

## Adding another Page

To add another page to our website, we need to create a new HTML file. Let's create a new file called `projects.html`. 

- The `<nav>` tag is used to create a navigation bar.
    - make sure to add the same navigation bar to the new page as well so that we can navigate between the pages.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projects</title>
</head>
<body>
    <h1>Projects</h1>
    <nav>
        <a href="index.html">Home</a>
        <a href="projects.html">Projects</a>
    </nav>
</body>
</html>
```

![Project Page](./images/demo5.png)
Now let's add a link in the navigation bar to the projects page from the index.html page.

```html
<body>
    <header>
        <h1>Drshika's Awesome Website!</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="projects.html">Projects</a>
        </nav>
    </header>
    <!-- Everything else stays the same -->
</body>
```

That should look like this:

![New Page](./images/demo6.png)

## HTML Element: Tables

The `<table>` tag is used to create a table. Let's add a table to our webpage to display some of the projects we will build together

- The `<tr>` tag is used to create a table row.
- The `<th>` tag is used to create a table header.
- The `<td>` tag is used to create a table cell.

```html
<table>
    <tr>
        <th>Project</th>    
        <th>Description</th>
    </tr>
    <tr>
        <td>Girls Who Code Website</td>
        <td>A website to showcase the projects we will build together!</td>
    </tr>
    <tr>
        <td>Recipes Website</td>
        <td>A collection of my favorite recipes!</td>
</table>
```

That should look like this:

![HTML Structure](./images/demo7.png)

## [BONUS] Adding a Button

HTML websites are static, meaning they don't have any interactivity. If we want the users to be able to interact with our website, we can use JavaScript. Let's make the cute animal picture a suprise when the user clicks on the button.

- The `<button>` tag is used to create a button.
- The `onclick` attribute is used to specify the JavaScript code to execute when the button is clicked.

```html
<button onclick="document.getElementById('animal').style.display='block'">Click me for cute suprise!</button>
<img id="animal" src="https://www.pewtrusts.org/-/media/post-launch-images/2022/11/gettyimages1198849037jpgmaster/16x9_m.jpg" alt="Three baby emperor penguin chicks" style="display:none;">
```

That should look like this:

![HTML Structure](./images/Untitled.gif)

## Acknowledgements

- [New.css](https://newcss.net/)
- [Inter Font](https://fonts.google.com/specimen/Inter)
- [Penguin Image](https://www.pewtrusts.org/-/media/post-launch-images/2022/11/gettyimages1198849037jpgmaster/16x9_m.jpg)
- [Girls Who Code HTML Tutorial](https://girlswhocode.com/programs/code-at-home)