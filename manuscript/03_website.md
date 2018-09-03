# Making Your Website More Professional

In an earlier lesson of this course, we generated a basic website where you could write about yourself, your interests, and the projects you've worked on. However, this was created before you were looking for jobs! In this lesson, we'll review how to add more information to your website to make it more professional and provide examples from others' websites. We hope that by the end of this lesson you'll have a website is helpful to those interested in hiring you!

Note: If you weren't able to successfully create a website previously, this was covered in the [Introduction to R](https://leanpub.com/universities/courses/jhu/introduction-to-r) course, so feel free to return to the "Creating Websites with R" lesson now to see if you have more success now that you have more experience!


### Getting Started

To follow along with this lesson, be sure to navigate to the RStudio Cloud space where you created your website. (If you can't find that space, you can use `git clone https://github.com/username.github.com.git` to cone your website repository into a new space. Note that you'll need to change "username" to your GitHub username). 

Navigate to the directory of your repository. You should be in `/cloud/project/username.github.com` at this point. Then, in the Terminal use `git pull` to be sure that you have the most updated version from GitHub.

### A Picture

In the last lesson where we generated your basic website, we reviewed how to include a picture of yourself. However, maybe at that point you hadn't yet decided on what picture you would use across all your professional accounts. We'll discuss at this point again how to include a picture of yourself on your website before moving onto further customizations. If you've already added an image of yourself and are happy with it, move onto the next section, "About."

If you don't have one already, you'll want to create a `img` directory within your repository. You can use `mkdir` (make directory) in the terminal to do so:

```
mkdir img
```

In that directory, you'll want upload a picture. You can Upload the image into this directory using the "Upload" icon in the Files tab of RStudio Cloud. For our example, we have uploaded a file called `Jane.png`. If you don't have an image, take a screenshot of your GitHub profile and rename it accordingly. You can verify your upload worked using `ls`. 

```
$ ls img
Jane.png
```

If `ls img` returns the name of the file you uploaded, you're ready to go! (If it doesn't, go ahead and make sure that the picture was successfully uploaded *and* that it is in the `img` directory.)

Now that we have the image, you'll have to add the following code to your `index.Rmd` file to have the image display on your website:

```
![](img/Jane.png){width=100px}
```

This code introduces the image and specifies the width of the image in pixels. We want a small image, so we are setting it to 100 pixels (`100px`).

![website with image](images/03_website/03_dsjob_website-3.png)

After knitting and pushing to GitHub, you will now have a website with an image! This is about where we left off in the last lesson.

You should have a website that looks very similar to what you see here:

![Website at this point](images/03_website/03_dsjob_website-4.png)

### About 

That's about where we left off in the last lesson. We had you add some About text, but now you really want to make sure this is up-to-date and complete. Your about section should be a line or two briefly describing your current positions and data science interests.

To see exactly what we mean, let's look at a few examples from the websites from people currently working in data science.

Here we're looking at the about section from [Nathan Yau's website](https://flowingdata.com/about-nathan/). In his about me section, Nathan briefly explains what he does followed by where to find some of his work. He finishes with some of his interests outside of work. If you want to see more of Nathan's work, check out [flowingdata.com](https://flowingdata.com/).

![Nathan Yau](images/03_website/03_dsjob_website-5.png)

Here we have another example from [Mona Chalabi](https://monachalabi.com/), a journalist who generates illustrations from data. Mona introduces what she does, describes where to find her work, and then provides some background information about her professional work.

![Mona Chalabi](images/03_website/03_dsjob_website-6.png)

Our final example comes from someone whose work you've seen throughout this course, [David Robinson](http://varianceexplained.org/about/). In his about me, he mentions his current position and interests, describes briefly some of his work, and provides a bit of background.

![David Robinson](images/03_website/03_dsjob_website-7.png)

These three examples should give you an idea of what to include in the "About Me" section of your website. Generally, consider including:

- current position (if applicable)
- background information
- where to find projects you've worked on

You'll additionally want to add a few interests in the "Interests" section. This should include at least a few data science-centric interests, but if you would like, you can also include a few additional interests here, as you saw some people did in the previous examples. 

To edit this on your website, you would edit the text in the "About" and "Interests" section of your `index.Rmd` file. Once you are done editing, click on the "Knit" button to update the index.html. 

![Edits to About section](images/03_website/03_dsjob_website-9.png)

### Links Elsewhere

If someone looking to hire you found your website, they should be able to easily navigate to your other professional social media platforms from your website. Thus, if you haven't already, you'll want to be sure that you include links to your GitHub, your LinkedIn, and your Twitter in the "Profiles" section of your `index.Rmd` file. 

Additionally, in the Projects section, you'll want to include links to (and images from if possible!) any complete projects. We'll discuss this more in the next lesson!

![Links elsewhere](images/03_website/03_dsjob_website-10.png)

After you've updated your links and projects, be sure to "Knit" your file before pushing your changes to GitHub. You'll get to see a preview of your updates before you put them on the Internet.

![HTML preview](images/03_website/03_dsjob_website-11.png)

Once you've pushed to GitHub, the changes should be visible on your website! (Note: you may have to wait a minute or two after pushing to GitHub to see them).

![Updates to website](images/03_website/03_dsjob_website-12.png)

### Summary

In this lesson, we've discussed the basics of what information should be on your professional website. However, there are lots of ways to customize your website beyond what was covered in this lesson. There are [tutorials](http://www.emilyzabor.com/tutorials/rmarkdown_websites_tutorial.html) you can use to learn more. In fact, the [website for this program](http://jhudatascience.org/chromebookdatascience/index.html) was created with R Markdown. Feel free to use the tutorial and to check out the [GitHub](https://github.com/jhudsl/chromebookdatascience) for the website to see what changes you would need to make to add additional pages to or to change the formatting of your website.

### Additional Resources

* [GitHub Pages](https://pages.github.com/)
* [Emily Zabor's great tutorial](http://www.emilyzabor.com/tutorials/rmarkdown_websites_tutorial.html)
* [GitHub for Chromebook Data Science website](https://github.com/jhudsl/chromebookdatascience) 

### Slides and Video

![Making Your Website More Professional](YouTube Link)

* [Slides](https://docs.google.com/presentation/d/1mIrb5R60b20WdUb2wjHstb1W0fky-DUgu_rW6yP0C70/edit?usp=sharing)


{quiz, id: quiz_03_website}

###Making Your Website More Professional quiz

{choose-answers: 4}
? Which of the following should NOT be included on your professional website?

C) home address
C) link to Facebook 
o) professional interests
o) appropriate personal interests
o) background
o) current position
o) projects you've worked on
o) contact information
o) link to GitHub
o) link to LinkedIn
o) an image

{choose-answers: 4}
? After making changes to your R Markdown document, what do you have to do before the changes will be visible on your website?

C) knit and push to GitHub
C) knit the document ; push to GitHub
o) push and pull to GitHub
o) save the document
o) write HTML code
o) knit to a PDF ; push to GitHub

{/quiz}

