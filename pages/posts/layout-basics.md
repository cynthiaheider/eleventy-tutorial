---
title: Pt. 2 - Layout Basics
description: Some Eleventy layout basics
date: 2024-02-23
tags:
  - posts
layout: layouts/post.njk
---
# This post was made on Glitch and should be changed before going live!

## Goals:

- Learn about site layouts in Eleventy, and how to create and edit them according to the DRY (Don't Repeat Yourself) principle.
- Practice using the Nunjucks syntax for page formatting and YAML for page categorization.

## Steps:

After a brief review of Eleventy, we'll troubleshoot any issues that came up while doing the homework. Then we'll dive into how Eleventy works with chunks of the website to create various layouts.

### All about layouts

1. Navigate to the ```src/_includes/layouts``` folder in your Glitch project. There should be several files here that all end with ".njk," which is the file extension for Nunjucks, a language created by the Mozilla Foundation for automated templating in JavaScript. This isn't the only templating language Eleventy understands, but it's the one we will be working with in this tutorial.
2. Look at ```page.njk```. This is a "layout" for a type of content called a "page". What elements do you notice in the file? What do you think they do?
3. Compare this to ```home.njk```. What elements are the same? What elements are different?
4. In a separate browser window, open up the preview of your ```about.md``` file. This file uses ```page.njk``` as its layout, which you can see in the code at the very top in between the two "fences."
5. Now open the preview of ```index.md``` in another browser window. This file uses ```home.njk``` as its layout. As you can see, there are a bunch of links under the "Posts" heading, even though that isn't written in ```index.md``` like your business's description is.
6. Back in ```about.md```, change the layout to "layout: layouts/home.njk". When you preview the page again, you can see that the posts now appear at the bottom of the page just like they do in ```index.md```. This is templating in action! Rather than copying and pasting the list of blog posts on every page, you can define a specific template layout for certain kinds of pages that automatically includes it.
7. Templates and layouts, along with some other kinds of descriptive information, are contained in a page's frontmatter, which is the "fenced" space at the top of your file. The new pages that you created, like ```contact.md```, don't yet have any frontmatter. Let's add some so that the posts show up on those pages, too.
8. Along with the layout type "layout: layouts/home.njk", add a page description using the format "description: Your description here" to the frontmatter of your ```contact.md``` file.
9. In ```src/_includes/layouts/home.njk```, insert the following right after the `h1` element:
```
<p>
  <em>{dscription}}</em>
</p>
```
10. Fill in the missing "e" and front bracket in the above so that it'll display correctly.
11. Preview your ```contact.md``` page and check out the changes! 
    - Notice that even though the "description" attribute is now in the ```home.njk``` layout, pages using that layout that don't have a description in their frontmatter don't have that element show on the page, making it optional.
    - Even though the ```contact.md``` page has frontmatter written at the top of the file, it doesn't appear on your site's preview. Frontmatter is like an invisible sticky note!

### All about partials

1. Right now, all the pages have the same footer menu and no header, because that is what is defined in ```base.njk```, the layout template that all other layouts extend off of. If we want to change something sitewide, we can do it in this file. Can you identify where the footer is defined in the layout file?
2. We can also make what is called a "partial" from the footer content. Cut the footer element out of ```base.njk```. Now create a folder within ```src/_includes``` called "partials," create a new file called ```footer.njk```, and paste the text into that file.
3. In the place in ```base.njk``` where the footer element was before, paste ```{ inclde "partials/footer.njk" %}```. Fill in the missing "u" and add a percentage sign after the opening curly bracket.
4. None of the pages currently have a header element, but we want one that puts our featured logo at the top of every page. Grab the URL of your logo image from the "assets" folder.
5. Create a file in the partials folder called ```site-header.njk```. Inside it, paste the following and fill in the details from your own project:
```
<header class="site-header">
  <div class="title" align="right">
    <a href="/home">
      Your site name here
    </a>
  </div>
  <div class="logo">
    <img src="Your logo URL here" width="200" height="200" alt="" />
  </div>
</header>
```
6. In ```base.njk```, paste ```{ inclde "partials/site-header.njk" %}```. Fill in the missing "u" and add a percentage sign after the opening curly bracket. Now preview any of your site pages and look at your lovely site header on each of them!

## Homework:

Let's practice what we've learned while making your site more personalized. Don't forget to jot down any issues you encounter in your ```notes.md``` file to troubleshoot later.

1. In ```footer.njk```, enter the names of the new contact and portfolio pages you created before into the footer's site menu, following the pattern that is already there for the other pages.
2. Create a new additional header, using the directions for making partials, that will only appear on content pages of the "post" type. It can say whatever you want.
3. It doesn't make much sense for all the pages that are not the "home" page to use the layout ```home.njk```. Move the changes you made in this file over to ```page.njk```. Now assign the layout type of "page" to your 404, about, contact, and portfolio pages in their frontmatter.
4. If you haven't already, insert the images you found for each page into their respective .md files, placed in whatever order you like. If you need a reminder about how to do this in Markdown, peep the [cheat-sheet](https://www.markdownguide.org/cheat-sheet/).
5. Make a new partial that only includes the site logo. Replace the "logo" ```<div>``` in the ```site-header.njk``` file with an include direction to this new file.
6. Insert the new logo partial into the site footer as well.
7. Next week we'll start styling your site, so start thinking about what colors, fonts, and other design elements you might want to incorporate!