---
title: Pt. 3 - Styling Fundamentals
description:  Time to make things prettier
date: 2024-02-23
tags:
  - posts
layout: layouts/post.njk
---
# This post was made on Glitch and should be changed before going live!

## Goals:
- Learn about basic page composition using the grid method and sketch out the structure of your site's individual pages.
- Learn the basics about Cascading Style Sheets (CSS) and how it controls what things look like on our pages.
- Make style choices for your project and begin to bring them to life.


## Steps:
To take greater control of what your site will look like, it's good to get an idea of what the canvas is. As you've seen, it is possible to make a web page with very little structure beyond text headings. But to make full use of the space you have to work with, you will need to start thinking in terms of components and their alignment.
1. The [grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout) is a framework for planning site layouts and interaction between different components with different purposes. The grid divides a website's canvas into up to 12 equal-width columns (and infinite rows, since web pages can scroll). First, let's take a few moments to draw out the structure of how you might want your 404 page to be structured and designed using the grid's constraints of up to 12 columns. What elements are necessary, and how do you want them to be arranged in relationship to one another.
2. We'll now walk through the official Mozilla documentation for basic concepts in the [grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout). There are a few activities which should help you see how the grid is defined, and serve as a gentle introduction to using CSS for styling.
3. Now we'll take a peek at the CSS file that already exists in your Glitch project. Navigate to the ```public``` folder and choose ```style.css```. This is the only CSS document used in this project, but it is important to know that you could also use multiple stylesheets to keep things organized, especially if you have A LOT of customizations. To some extent, the number of stylesheets you use is a matter of personal preference.
4. Notice how the CSS directions in ```style.css``` correspond to different HTML notations like ```<body>```, ```<h1>```, ```<ul>```, etc. This is called a "declaration." There will be other references there that may not be as familiar. This is actually a somewhat complex stylesheet, so rest assured that either we'll get around to explaining them or they aren't necessary to master just yet in order to do what you need.
5. On line 11, notice that ```color-bg:``` is assigned to #D7F5EF. This is a shorthand notation for a color in hexadecimal code, which is a standard used across the web. #D7F5EF is a minty-green color, which you can see by checking out its entry on a site like [htmlcolorcodes.com](https://htmlcolorcodes.com/). Some hex codes have named alternatives, such as "black" and "red", which CSS will also understand. Pick a color on the htmlcolorcodes.com that you like, and replace the value in the CSS declaration with its respective code (which will always be six characters and be preceded by a #). Check out how your site's background color immediately changes.
6. We'll practice working with these declarations for specific elements within a page, called "selectors", using the [official Mozilla documentation for them](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors). There are some activities which can help you understand how to assign styling directions to specific elements of your site.
7. Returning to your drawn grid layout, write a name for each block and indicate what styles you might like to govern them. This could include design choices like whether sections have a border around them and what it looks like, how big you'd like different text elements to be, the color of the font, and the alignment of the textual or image elements. You can also indicate if you would like styles to apply to all elements of that category on the page.



## Homework:
1. There was a lot of new material introduced this week. In order for it to feel more comfortable, you should get some practice applying CSS to specific parts of your website. Anticipating the drawn layout's use, create a new file in ```_includes/layouts``` called ```404.njk```. Copy everything from line 1 down from the ```base.njk``` layout and paste it into ```404.njk``` so it has a basic structure.
2. Create a new file in the ```public``` folder called ```404-style.css``` and leave it blank for now.
3. On line 11 of ```404.njk```, replace ```href="/public/style.css"``` with ```href="/public/404-style.css"```.
4. In the frontmatter of ```404.md```, define the layout it should use as ```404.njk```. If you preview your 404 page now, it will look a lot different.
    - remember that although there is no direct link to your 404 page from your site, you can access it by appending ```/404``` to your site URL.
5. We're now building your CSS styling up from scratch! The first element we are going to practice with is the border around the image. In your empty ```404-style.css``` file, set a declaration for the [HTML img tag](https://www.w3schools.com/tags/tag_img.asp) using the knowledge you gained in the tutorial. There are a number of declarations you could make here that would control the way an image is displayed on your site; one of these options is the [CSS border property](https://www.w3schools.com/css/css_border_shorthand.asp).
