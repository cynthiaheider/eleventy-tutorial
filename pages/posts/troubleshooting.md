---
title: Troubleshooting
description:  When things don't go the way you want them to
date: 2024-02-23
tags:
  - posts
layout: layouts/post.njk
---
# This post was made on Glitch and should be changed before going live!


## Goals:
- Cultivate basic skills in troubleshooting your project made with Eleventy
- Identify when you need to send up an S.O.S.

## Steps:

As you've probably already learned going through these lessons, sometimes things don't appear the way you want them to, and it can be hard to figure out why. Here are some steps that can help you narrow things down if you're having a problem.

1. __Check your Glitch interface.__ If the little "Status" face in the bottom left hand corner is red, it's trying to tell you that there is a problem processing your code. You can usually pinpoint the location (but not always the exact reason for) an issue by then looking at the "Logs" menu to the right of "Status".

2. __Check the demo site.__ 
In this case, you can follow along with the source code of what I’ve created at [https://glitch.com/edit/#!/famous-carpal-eyeliner](https://glitch.com/edit/#!/famous-carpal-eyeliner). If you want a preview of what it will look like to a site user, you can view that at [https://famous-carpal-eyeliner.glitch.me](https://glitch.com/edit/#!/famous-carpal-eyeliner).
    - Compare the code in the pages you were working on before your site stopped doing what you wanted it to (the "rewind" feature could be helpful here!). Some clues to finding the culprit could be:
      - a different amount of lines between the demo file and your file (are there fewer lines? more?)
      - a difference in the place the file is located in the directory (is the demo file in the ```_includes``` folder while your file is in the ```src``` folder?)
      - a difference in spelling or syntax between the demo file and your own. You may be able to tell at a glance, but you could also use a tool called a "diff" that compares two files and tells you what the difference between them is. I like [https://www.diffchecker.com/](https://www.diffchecker.com/) but there are many others out there.
      
3. __Quarantine your files.__ If all else fails, a relatively quick way to at least find the specific file that the problem is in is to quarantine your files. 
    - Create a "quarantine" folder outside of the ```src``` folder, so anything inside it won't be processed by the Eleventy pasta maker.
    - You could drag each file, one-by-one, into the quarantine folder and then check to see if your site is loading or otherwise doing what you want.   
      - When you have a project that has a lot of files in it, you can speed up this process by implementing the 50/50 method: Put half of your files into the quarantine folder; now check to see if the site works. If it does, you know that your problem(s) is/are in one of the files in quarantine, and the rest of them are (probably) ok. From here, you can narrow it down by halves again until you find the subset of files with the problem.
      
4. __Google it!__ Truly, this is a tried-and-trued method of most programmers and web developers everywhere. There is no shame in Googling your problem and implementing any suggestions (as long as you're keeping a copy of your original code safe somewhere else in case you need to go back). I often include the keyword "stack overflow" when searching for these kinds of things. This website (popular in the tech world) has [a whole section of questions here tagged about ELeventy](https://stackoverflow.com/questions/tagged/eleventy), for instance.