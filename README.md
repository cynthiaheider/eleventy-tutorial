# README

This repo contains the bare bones of what you will probably need to quickly start up a new Eleventy site. You can fork this repo and build upon it, or choose it as the "Repository template" when creating a new repo.

## Before you start!
Before you can make a site with this repo, you will need to install and run some commands in the [terminal/command line](https://www.11ty.dev/docs/terminal-window/) of your computer. The [Quickstart page in the 11ty documentation](https://www.11ty.dev/) and the more detailed [Get Started page](https://www.11ty.dev/docs/) are great copy-and-paste guides to this setup process.

## Structure
- The '_includes' folder will contain templates (sometimes called layouts or partials) that streamline your site and maintain consistency by breaking elements of the site's HTML into parts like "header," "footer," and "menu."
- The '_site' folder contains the files that will show to a user who visits your site on the web. Eleventy generates the files in this folder from the files at the top level of your file directory. You shouldn't need to touch anything in this folder and it's probably best to just leave it alone!
- The 'assets' folder is where you'll put any images, videos, or other files like that. It also holds CSS, JavaScript, Sass, and other similar files that change the way the site looks and functions.
- The 'node_modules' folder contains a bunch of extensions for the site's performance. It is a big folder and you may not need everything in it for your project, but be careful about deleting things that might break your site.
- The 'index.html' file contains the homepage of your site. Make sure to edit this file rather than the one inside the _site folder. The same goes for any other editable site files you might want to create (like about.html or contact.html) that should be stored at this "top" level of the files directory.
- Leave 'package-lock.json' alone.
- The 'package.json' file is here because Eleventy uses node.js to construct the site. It contains basic metadata about your site, including the author, site name, and any software dependencies it requires to function.
- The 'README.md' file can be deleted after you fork or create your own new site using this repo template.
- The 'CITATION.cff' file is an optional way for you to provide a preferred citation for your project which will show up in your repository. Learn more about the options for populating this file in the [GitHub Docs: About CITATION files](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files).

## Learning more
This repo does not contain a tutorial on using or setting up Eleventy. There are plenty of those out there - ask for help if you need guidance finding them.
