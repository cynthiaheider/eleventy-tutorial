---
title: Pt. 1 - Making Pages
description:  New pages
date: 2024-02-23
tags:
  - posts
layout: layouts/post.njk
---
# This post was made on Glitch and should be changed before going live!

## Goals:

- Learn about the structure of a website and how to create, edit, and delete individual pages on a site.
- Practice using HTML and Markdown, two languages that are used to format text and layout of web pages.
- Practice uploading files to Glitch.

## Steps:
Eleventy is a very flexible system. It understands multiple kinds of languages used in making webpages and it's not too picky about them. We'll create two new pages and get some experience using HTML and Markdown. 
1. Navigate to the ```src/``` folder on the left and click the three dots that appear when you hover over it. Select "Add file to folder."
2. Name this first file ```html-page.html```. On line 1 of this file, enter the following:
    ```
    This is a huge headline.
    This is the smallest headline.
    This is a paragraph of content.
    This is a link to another website.
    This is a picture.
    This is an ordered list.
    This line is bolded.
    This line is italicized.
    This is an unordered list.
    This line is underlined.
    This line is struck through.
    ```
3. Now we'll add formatting using the corresponding language, which in this case is HTML. [Here's a cheat sheet if you need it](https://developer.mozilla.org/en-US/docs/Learn/HTML/Cheatsheet).
    - HTML formatting rules are indicated by surrounding a piece of text with an instruction for how the computer should display it. These instructions are surrounded by brackets, like so: ```<b>Demo bold text</b>```. Note that Glitch will perform an "autocomplete" and insert the "closing" tag as soon as you type the corresponding "opening" tag. This can get annoying and confusing, so you might want to 
    - For line 3, [generate a paragraph](https://loremipsum.io) of "lorum ipsum" text and paste it here.
    - For line 4, enter any link you want.
    - For line 5, drag any image file(s) onto the Assets icon in your Glitch interface. Click on the image and copy its URL.
Click the three dots that appear when you hover over ```html-page.html``` in the left-hand menu. Choose "Duplicate" and when prompted, name this file ```markdown-file.md```.
4. Now we'll add formatting using the corresponding language. In ```markdown-page.md```, practice adding formatting to the lines using what you learned in the [Markdown tutorial](https://www.markdowntutorial.com/). 
    - [Here's a cheat-sheet if you need it](https://www.markdownguide.org/cheat-sheet/).
    - For line 3, [generate a paragraph](https://loremipsum.io) of "lorum ipsum" text and paste it here.
    - For line 4, enter any link you want.
    - For line 5, drag any image file(s) onto the Assets icon in your Glitch interface. Click on the image and copy its URL.

Each page will look identical when looked at in the Preview pane of Glitch. This demonstrates that either system, or both, can be used in one Eleventy website with minimal fuss.

## Homework:
For the next Eleventy tutorial session, go ahead and create some base pages that we will use to learn about styling and creating “partials” (elements that are consistent across the entire webpage, like headers, footers, and menus). 

You can follow along with the __source code__ of what I’ve created at [https://glitch.com/edit/#!/famous-carpal-eyeliner](https://glitch.com/edit/#!/famous-carpal-eyeliner). If you want a preview of __what it will look like to a site user__, you can view that at [https://famous-carpal-eyeliner.glitch.me](https://famous-carpal-eyeliner.glitch.me).

We are going to jump right in by creating a sample site for a fake/real business of your choice. The example I’m using is a fake bakery called “Soggy Bottoms.” 

Create the following pages in your Glitch project’s “src” folder:
- __notes.md__: This page is just for us and will not show up on your final product. Use this space to make notes if you have trouble doing something or figuring something out. Also use this space to record the URLs where you originally find your uploaded images so that we can cite them properly later on.
- __contact.md__: A place where you will put your fake/real business’s contact information. Write at least three lines of text for what you want this page to say. Look around online for two images/pictures/icons that you want to display on the page and upload them to the “assets” section of your interface.
- __portfolio.md__: A page where you will display several items that might fit into your project’s “portfolio.” For now, just write at least three lines of text, and upload three images that could represent each different item in your portfolio.
- __404.md__: Most websites have a special page that will display if someone tries to navigate to a URL that doesn’t exist on your website. Write a line of text to let them know they messed up. Upload a picture that indicates the same.
- __about.md__: Your Glitch project already has one of these, but change the text so that it fits your business. Write at least three lines of text and upload 2 images.
- __index.md__: Again, your Glitch project already has one of these, but you will change it so it fits your own project. The index (or “splash”) page is the one that usually appears when someone first comes to a website, so make it a good introduction to someone who might be discovering your business for the first time. Make sure it has at least three lines of text and upload a picture that could serve as a logo.