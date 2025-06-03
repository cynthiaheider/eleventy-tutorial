---
title: Pt. 5 - Groupings
description: Pages of a feather flock together
date: 2024-02-23
tags:
  - posts
layout: layouts/post.njk
---
# This post was made on Glitch and should be changed before going live!

## Goals:
- Apply knowledge gained so far to set up the portfolio page's requirements.
- Create a "collection" (grouping) of pages in Eleventy and control its behavior.
- Apply this method to the portfolio's pages and optionally a navigation partial.

## Steps:

1. We practiced with the Bootstrap CSS in the ```demo-404.html``` page we created, but now we are going to apply this CSS to the rest of the website. In the ```_includes/layouts/base.njk``` file, add in the Bootstrap connectors at line 13 by pasting the following:
```
    <!-- Bootstrap CSS stylesheet and JavaScript files --
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
      crossorigin="anonymous"
    />
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
    
    <!-- end Bootstrap files --> 
```
2. The arrows around the text you just pasted indicate that the text inside is a human-readable "comment" that will not be processed onto the website. Now add a closing `>` at the end of line 13, and either delete the Glitch CSS reference above it on line 11, or (preferably) surround it with comment tags ```<!-- -->``` so that it won't be read on the website, but will still be there for you if you want to use it later on. P.S. This will make your site look pretty bland for now!

3. To make the Bootstrap format correctly, you need to wrap the ```<div class="container"></div>``` around the page's content. Add it at line 30, right after the opening ```<main>``` tag, and close it with a ```</div>``` right before the ```</main>``` tag.

4. We are going to make a "collection" grouping for portfolio items. Eleventy understands that pages in a collection are related to each other (like blog posts) and can display them all together. We want portfolio items to show on the ```portfolio.md``` page underneath the page content you have already entered there. Create a new folder in ```src``` called "portfolio" and inside it, create 2 Markdown files.

5. In the frontmatter of these files, paste the following and then change the title and description so they are unique to the file: 
```
---
title: Your title
description: Your description
tags:
  - items
layout: layouts/portfolio-item.njk
---
```

6. Create a file in the new ```portfolio``` folder called ```portfolio.json``` and paste the following:
```
{
  "tags": ["items"]
}
```

7. Now we'll create the collection. In the ```eleventy.js``` file, paste the following at line 73:
```
  eleventyConfig.addCollection("portfolio", function(collection) {
    
    /* The portfolio collection includes all portfolio items that list 'items' in the front matter 'tags'
       - https://www.11ty.dev/docs/collections/
    */
    
    // EDIT HERE WITH THE CODE FROM THE NEXT STEPS PAGE TO REVERSE CHRONOLOGICAL ORDER
    // (inspired by https://github.com/11ty/eleventy/issues/898#issuecomment-581738415)
    const coll = collection
      .getFilteredByTag("items");

    // From: https://github.com/11ty/eleventy/issues/529#issuecomment-568257426 
    // Adds {{ prevPost.url }} {{ prevPost.data.title }}, etc, to our njks templates
    for (let i = 0; i < coll.length; i++) {
      const prevItem = coll[i - 1];
      const nextItem = coll[i + 1];

      coll[i].data["prevItem"] = prevItem;
      coll[i].data["nextItem"] = nextItem;
    }

    return coll;
  });
```

8. We have to tell Eleventy how to format the portfolio splash page and the individual portfolio pages. To do that, we must create files in the ```_includes/layouts``` folder. Create a new file there called ```portfolio.njk``` and paste the following into it:

  ```

9. This made the splash page formatting, but we also have to format the individual pages. Create another file in ```_includes/layouts``` called ```portfolio-item.njk``` and paste the following:
  ```



## Homework: