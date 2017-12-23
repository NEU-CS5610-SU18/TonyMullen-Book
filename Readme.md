# Getting MEAN 2nd Edition book project

This is the project described in the book Getting MEAN (2nd Ed) by Simon Holmes. Your Readme.md should look something approximately like this one.

For each chapter, add a note with the following:
* A description in your own words (>= 80 words) of the functionality you implemented and how it works, and list any challenges or problems you encountered.
* The answer to all **readme questions** listed on this page for the chapter. 
* A screenshot of the current state of your work (see my chapter notes on this page for each chapter for specifics on what you should include in the screenshot).

Add your chapter notes **in descending order, with the latest on top,** as I've done below. Scroll to the bottom of this readme to see some tips on how to use the Markdown notation to get the elements you need.

**Submit the link to Moodle** by the appropriate assignment deadline. 

### Committing and tagging

While working through the book, you should be doing **regular Git commits** (at least 4 per chapter) so I can view the specifics of your progress. This is done like this:

```
git add .
git commit -m "your comment here"
```

Always include a brief but *meaningful* comment. Do not make comments like "blahblah" or "some stuff". [Here's some good advice on commit messages](http://chris.beams.io/posts/git-commit/).

In addition, as you complete each chapter, you should **commit and tag** the release representing that chapter, so I can quickly go to the last commit for each chapter. Look at the commit history of this repository to see an example. [Here's the documentation on tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging). You must also push your commits to GitHub and Heroku. Pushing to GitHub (with tags) should look something like this:

```
git push origin master --tags
```

**Always ensure that your code is working before committing it.** You should be manually testing your work **frequently** so that you don't write too much code to quickly debug it if it's not working properly.

## Chapter notes

This Readme has been modified throughout the process of implementing the project, so please always refer to the latest version of the Readme, rather than tagged chapter releases. The notes for the 2nd Edition of the book are based upon a work-in-progress copy of the book, so issues described in the notes may have been fixed by the time you read the book. Please let me know if the notes need updating.  

# <a name="ch4"></a>Chapter 4

For your own Chapter 4 work, you should replace the author's *Starcups* cafe with an existing nearby cafe. I've used Oppenheimer cafe. You should be sure to also replace the latitude and longitude in the controller, so that by the end of the chapter, the correct location is displayed on your webpage's map, as shown in my screenshot below. 

Don't forget to include the link to the [Heroku app](https://getting-mean2e.herokuapp.com/) near the top of the readme section for each chapter!

Notes:

* At the time I'm going through it, the WIP version of the book uses Bootstrap version 4.0.0-alpha.6 (this is mentioned in Appendix B). However, Bootstrap version 4.0 is now out of alpha stage and the layout of the navbar element has changed. I had some problems with the alpha version described in the book, and since the non-alpha version is probably going to be more future proof, I've updated my code to use it. I'm using Bootstrap 4.0.0-beta.2. The documentation I'm following is [here](https://getbootstrap.com/docs/4.0/components/navbar/). The Pug code for the navbar is as follows (starting with the `body` tag above the navbar)
    ```
  body
    nav.navbar.navbar-fixed-top.navbar-expand-lg.navbar-dark
      .container
        a.navbar-brand(href='/ ') Loc8r
        button.navbar-toggler(type='button', data-toggle='collapse', data-target='#navbarMain')
          span.navbar-toggler-icon
        #navbarMain.navbar-collapse.collapse
          ul.navbar-nav.mr-auto
            li.nav-item
              a.nav-link(href='/about/') About
    .container
      block content
    ```

* This doesn't seem to be mentioned outright in the text, but you'll need to add the appropriate styles to your `style.css` file in order to get the app looking right. You can find the styles in my `style.css`. My own css is slightly modified from what I'm currently seeing in the author's GitHub.
* Finishing hooking up the views to the controllers as described in Appendix C is part of the Chapter 4 assignment. Make sure this is also done. 
* In Appendix C, the src value for the Google Maps element is enclosed in back ticks. These are not the same as single quotes, so be careful. 

**Ch 4 Readme Questions**

1. In class, we've talked about code re-use, and avoiding unnecessary repetition of code. How do the Pug templates you've worked with in Chapter 4 help to accomplish this?
2. According to the routing we have set up, what function is called when the `/location` url request is received? What file is this function defined in?

![ch3](/readme_images/ch4-1.png)

![ch3](/readme_images/ch4-2.png)

# <a name="ch3"></a>Chapter 3

Don't forget to include the link to the [Heroku app](https://getting-mean2e.herokuapp.com/)!

Notes:

* Installations from appendix A & Appendix B are necessary to get Ch 3 code working.
* Any reference to any file with the extension `.jade` should be changed to `.pug`.
* Jade/Pug files are indentation based. Wrong indentation in these files will throw your layout out of wack. Turn on Show Indent Guide and Show Invisibles in Atom (Preferences > Editor) to see the spaces in your editor. Also, refer to the author's GitHub code directly to check the indentation when the indentation is borked in the book or e-book (as I write this, Listing 3.7 in the epub version is an example of this).

**Ch 3 Readme Questions**

1. The default `app.js` file generated by Express declares variables using the `var` keyword. What are the two new keywords introduced in EcmaScript 6 that the author discusses, and what is his recommendation for declaring variables in `app.js`?
2. What do we call the process of mapping URL requests to the functionality we want to associate with the URL? For example, when the URL `/` is requested (this represents the base URL for our application's domain), we want to execute the controller function that renders our title page. What do we call the code that connects a URL request to our controller code?

The app so far should look like this on Heroku (include a screenshot with each chapter's update!):

![ch3](/readme_images/ch3.png)

### Markdown

This Readme file was written in the (GitHub Flavored) [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) (`.md`) language. Look at this Readme in "raw" view to see [the markup code](https://raw.githubusercontent.com/UPS-CSCI240-F16/GM/master/Readme.md).
