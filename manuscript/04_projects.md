# Project Gallery

When looking for a job in data science, it's best that those interested in hiring you can get a sense for your work easily on the Internet. By displaying projects you've worked on on your website, hiring managers can quickly see what skills you have and what you're interested in. 

Arguably, this could be seen on GitHub (we'll get to this in the next lesson!), and hiring managers will likely look there as well; however, by writing up a short report that tells the whole story for a few of your data science projects, (including visualizations!), and including them on your website, you're making it even easier on hiring managers to see what you can do!

In this lesson, we'll discuss two different ways of displaying your projects on your website, discuss what you'll want to include on your website, and walk through step-by-step of turning one of the projects in this course into a project included on your website.

### Project List 

The simplest way to display projects on your website is by including bullet points that link to your projects on GitHub; however, looking through multiple folders on your GitHub to figure out what you did on a project is asking a lot of someone. Thus, while it's better than nothing to include links to your GitHub, you want to make it easier on your readers. 

To do this, you'll want to turn your projects into a report or blog post that you'll then publish on your website. By telling a story about your project, including the results in figures and tables, and making what you did in the analysis very clear, you're demonstrating both your technical and communication skills all at once. 

In the last lesson on updating your website, we looked at David Robinson's ["about me" section](http://varianceexplained.org/about/). In this lesson, we can see that as he carries out projects, he writes blog posts and posts them to his website. 

![David Robinson's Projects](images/04_projects/04_dsjob_projects-1.png)

On his website, his most recent posts are displayed, and the contents of each can be found by clicking on any of the titles. Then, visitors to his site can see the story of his analysis!

![Blog posts tell analytical stories](images/04_projects/04_dsjob_projects-2.png)

By including links to summaries (blog posts!) of your work on your website, you're helping individuals looking to learn more about your work or simply interested in your analyses

### Project Gallery 

Beyond providing links to blog posts, it can sometimes be helpful to provide readers with a visual cue as to what will be included in that link. Rather than a list of your projects, including an image along with the title of the post can be very helpful to attracting readers to your work.

For example, on Nathan Yau's site, [FlowingData.com](flowingdata.com), projects can be searched by topic. Then, images for each post are displayed with the title underneath the project and the first few words from the post displayed underneath the title. 

![Projects on Nathan Yau's website](images/04_projects/04_dsjob_projects-3.png)

One caveat here is that on this site, Nathan Yau often links to others' work to promote and support their work, so these aren't all his own projects. On your website, when looking for a job, you would want to be sure to include links to your work primarily. You can then use Twitter (we'll talk about this later!) to support and promote others' work, at least while you're looking for a job. Once you're more established (like Nathan Yau), it's OK to include links to others' work on your website, as long as you give them credit, of course!

Another great example of a project gallery can be seen on Mona Chalabi's website. We saw her about me section in the last lesson and learned that she visualizes data using creative and artistic drawings/visualizations. This type of work perfectly lends itself to a project gallery, as the visualizations are the story.

![Mona Chalabi's Project Gallery](images/04_projects/04_dsjob_projects-4.png)

However, Mona is also a writer. Her journalism pieces are also listed on her website, in list format! Both project lists and project galleries can be effective ways to share your work on your website! 

![Links to Mona Chalabi's Writing](images/04_projects/04_dsjob_projects-5.png)

### What To Include

As you're preparing your project gallery, you'll want links to a few blog posts about projects you've worked on. These posts should display your ability to:

* find a dataset
* wrangle a dataset
* explore a dataset
* analyze a dataset
* visualize a dataset
* tell a story 

You'll want at least a few examples of your work, meaning at least 3 different projects you've worked on. And, you'll want to make sure at least one of these is a project you've come up with and worked on on your own -- you don't want the projects you display to all come from the projects done in this Course Set, although some of them can be!

### What Not To Include

As you're looking for a job, it's best to **avoid criticizing the work of others** in your project gallery. You can certainly use a dataset that someone else has written about previously to do your own analysis; however, your post should *not* tear apart what that other individual did in theirs. 

Additionally, remember this is a blog post. (For details about what to include in a blog post, refer back to the [Written and Oral Communication in Data Science](https://leanpub.com/universities/courses/jhu/writtenandoralcommunicationindatascience) course.) This post should tell a story and include details about your analysis, but it **shouldn't include every detail about your analysis**. You should do the analysis and then pare down what you have to only what's necessary to communicate your story to your audience. 

Finally, remember that this should demonstrate your skills and abilities. **Do not take code or work from others without properly citing those individuals**. Giving attribution to others' work when deserved is incredibly important. Be sure that all writing and code portrayed are your own in your project gallery actually are your own work.

### Your Project

Now that we've seen a few examples of others' projects, let's get down to preparing one project you may want to include in your project gallery! In the last course, one of the quiz questions required you to create a presentation on Google Slides taking what you did in your Final project and turning it into a presentation that you'd present to a technical audience. 

Thus, you should have already thought a bit about how you would tell a story about this analysis. We'll use that same project (your Final Project from [Data Analysis](https://leanpub.com/universities/courses/jhu/dataanalysis)) here, but instead of generating a Google Slides presentation, we'll turn this project into a blog post that will be able to be included on your website! 

The link to this page on your website will be required in the quiz for this lesson, so it's best to follow along, create this blog post, and update your website as you work through this lesson!

#### Website Setup

Since over time you'll have more than a few projects, it's likely best to generate a new tab on your website for your projects, rather than including them on your home page.

To do this, navigate to your website on GitHub. You'll need to first generate a YAML file in the home directory of your website (/cloud/project/github_username.github.io). To do this, first go to File > New File > R Script.

![New Script](images/04_projects/04_dsjob_projects-9.png)

Paste the following contents into this file, but change "Jane Doe" to your name in both the `name` and `title` fields:

```
name: Jane Doe's Website
output_dir: '.'
navbar:
  title: Jane Doe's Website
  left:
  - text: Home
    href: index.html
  - text: Projects
    href: projects.html
```

![`_site.yml` on RStudio Cloud](images/04_projects/04_dsjob_projects-10.png)

Save this file as `_site.yml`. When asked if you want to change the file extension, click "Yes."

![Yes to change the extension](images/04_projects/04_dsjob_projects-11.png)

What this file does is specify what tabs you want displayed along the top of your website. "Home" will direct users to your home page, which is all the content in `index.html` (the file Knit from `index.Rmd`). We're additionally going to create a "Projects" tab. The content in this tab will be populated from the `projects.html` file. We'll create this later in this lesson.

Be sure to double check that you have saved `_site.yml` in the home directory of your website. If you haven't, move the file into the appropriate directory now.

![Correct directory](images/04_projects/04_dsjob_projects-12.png)

At this point, if you were to Knit your `index.Rmd file locally (meaning in RStudio Cloud but not on your website online since you haven't yet pushed the changes to GitHub), you would see your new Projects tab in the preview!

![New Tab Preview](images/04_projects/04_dsjob_projects-14.png)

However, if you were to click on that tab, there wouldn't be any content. This makes sense. We haven't told your website yet what will be in this document! We'll do that in just a second.

Before we move on to writing the content that will go in your Projects tab, one note on what we just did. When you Knit your document, a new directory will appear in your website directory called `site_libs`. This directory will be created automatically when you knit and should be in there. There's no need to delete it; however, if you do, when you re-knit, it will re-appear automatically.

![`site_libs`](images/04_projects/04_dsjob_projects-15.png)

Now that we have a projects tab, we likely don't want our projects on our home page anymore. So, let's edit our `index.Rmd` file by removing the Projects section. Simply delete the header for that section and the content underneath that header.

![Remove Projects from homepage](images/04_projects/04_dsjob_projects-16.png)

Once that's been removed and the file has been re-knit, there will no longer be a projects section!

![No Projects section](images/04_projects/04_dsjob_projects-17.png)

#### Setup

Now that we have the Projects tab set up, let's get to actually generating content for that tab! The goal of this lesson will be to get what you did in your final project into blog post format so that it can be included on your website. After this lesson you can do the same for the other two projects in this course set (Data Tidying and Data Visualization) as well as begin to complete projects on your own to be added to your project gallery.

To get started, let's create a directory called `projects` in our website directory. This will be the directory where we keep the files containing our projects.

Now that we have a directory, let's create a document for this first project and decide how to set up this project. Start a new R Markdown document and save it _within the `projects` directory_.

![ATUS Survey Analysis](images/04_projects/04_dsjob_projects-20.png)

For this lesson, we've titled this post "ATUS Survey Analysis", but as we've discussed in previous lessons, this is *not* a very good title. A better title would concisely convey the findings of the analysis. Be sure that your project title is better than "ATUS Survey Analysis."

With the file ready, we'll need to determine the general framework for this blog post. This means determining what sections to include in the project and what figures/results you'll present to tell your story. It's a good idea to open a new R Markdown document for this analysis and place the section headers in the document before you start adding content.

A general framework for this project and most analyses blog posts could be the following:

![General Framework](images/04_projects/04_dsjob_projects-21.png)

You want to be sure to explain why you're doing the analysis and what question you'll be answering in this post in the introduction. Following this, it's often a good idea to explain where the data came from and display the code you used to get the data into RStudio Cloud. The Exploratory Data Analysis section should explain how you wrangled the data and maybe show an explanatory plot or two. How you analyzed the data should be explained briefly after the data are explained. The Results section is the most important - this should summarize your findings, including figures and tables to guide the reader and help them understand your results. The sub-headers within the results section should tell the reader what your result was. Finally, a conclusion should pull everything together.

Within your R Markdown document, this framework would be entered as follows:

![Framework in R Markdown](images/04_projects/04_dsjob_projects-22.png)

#### Content

With the skeleton for your post in your R Markdown document, you would begin to include text and code throughout the post. For example, in the data section you'd explain where the data came from, describe how many observations are in the data and what variables you're most interested in.

You'd also include a code chunk that would read the data into R. Note that you'll need the data in this project in order for this R Markdown document to knit.

![Data section](images/04_projects/04_dsjob_projects-23.png)

If we were to knit this file at this point, it would be pretty bare bones.

![Skeleton with data section started](images/04_projects/04_dsjob_projects-24.png)

But, as you include more content for what you did in this analysis, it will become a full-fledged post. Be sure that there is text accompanying all code, figures and table, to explain to your readers what is being done throughout the project. Adapt the code from your projects into this document by using the code you've already written but adding text to explain to a reader what you've done.

#### Proofread

After you're happy with your post, it's always a good idea to proofread your writing for typos and errors.

#### Knit 

At this point, you're ready to knit your R Markdown document. Double check to make sure the .Rmd and the .html files are both within the `projects` directory you created.


### Projects

You now have a post and a website with a "Projects" tab, but you're missing the link telling the Projects tab where to find your projects! We'll fix that now. 

To tell the projects tab where to look for your Projects, you'll need to open a new R Markdown document. The title of this document will be "Projects." 

![projects.Rmd](images/04_projects/04_dsjob_projects-25.png)

Save this document as `projects.Rmd` in the main directory for your website - the name of this file should correspond to the file you stated in `_site.yml` (`projects.html`). Knit this document. `projects.html` will be generated and saved in the main directory for your website.

Within this document, you'll need to create a link that directs website to the .html document with this analysis.

![point to file](images/04_projects/04_dsjob_projects-26.png)

Note that you've saved this file within the `projects/` directory, so your relative link will have to specify that.

When you knit your `index.Rmd` document to preview your website and click on the Projects Tab, there is now content in there (thanks to `projects.Rmd`) and a link in there to your analysis!

![Projects Tab has content](images/04_projects/04_dsjob_projects-27.png)

Then, if you click on the link, you will be redirected to this project!

[Link opens up your analysis](images/04_projects/04_dsjob_projects-28.png)

A final note on edits to `projects.Rmd` is that this is like any R Markdown document. You can use headers to separate projects, add images (make sure you upload images you want to include) and include brief text to describe what one will find in the link. This will help make your list of projects more similar to a visually-enticing project gallery.

![updates to `projects.Rmd`](images/04_projects/04_dsjob_projects-29.png)

Just remember that to see any changes, the document has to be Knit. The changes will then be visible locally in the HTML preview!

![Knit to HTML](images/04_projects/04_dsjob_projects-30.png)

### Push to GitHub

Once you're happy with these changes, push all your changes to GitHub:

```
git add .
git commit -m "add projects tab"
git push
```

Your changes will now be viewable on your website!

![Changes to website](images/04_projects/04_dsjob_projects-32.png)

You'll want to create a blog post-like document for each of the projects you've completed in this course set *and* andy projects you've done on your own!


### Slides and Video

![Project Gallery](YouTube Link)

* [Slides](https://docs.google.com/presentation/d/1iE2IIefyB93TZkQWCZN5FORTj02SvCHZPMoqv6A8ngI/edit?usp=sharing)


{quiz, id: quiz_04_projects}

### Project Gallery quiz

{choose-answers: 4}
? Projects on my website should be most similar to...

C) blog posts
C) brief reports
o) GitHub repositories
o) full reports
o) technical presentations
o) general presentations
o) one-on-one meetings

{choose-answers: 4}
? The goal of including projects on my website is to...

C) Demonstrate my technical and data science communication skills
C) Show off my work and interests to hiring managers
o) Criticize others' work
o) Show off my HTML skills
o) Generate a Twitter following
o) Show every detail of what I did for an analysis
o) Help others make their own website

{points: 3}
? Throughout this lesson, you should have updated your website with a link to a blog post describing the analysis you did in the Final Project of this Course Set. **Paste the URL to the project on your website below**.


! /(.+github.io.+)/i

{/quiz}

