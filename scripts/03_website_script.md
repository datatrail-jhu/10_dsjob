In an earlier lesson of this course, we generated a basic website where you could write about yourself, your interests, and the projects you've worked on. However, this was created before you were looking for jobs and before you were comfortable working with R and R Studio Cloud! In this lesson, now that you have these skills and are more comfortable, we'll update the look of your website using the blog down package. In this lesson, we'll cover both how to add more information to your website and how to make it more professional. In doing this, we'll provide examples from others' websites. We hope that by the end of this lesson you'll have a website is helpful to those interested in hiring you!This will be a long lesson, but it will be worth it. Go through each step in R Studio Cloud as you read through the lesson to update your professional website!

blog down is an R package that helps create websites with R Markdown. There is a whole book dedicated to helping users use this package, so if you want to learn more about blog down beyond what is covered in this lesson, that book is a great place to start. Simply though, blog down allows users to generate static websites. This means that you will generate HTML files within blog down that visitors to your website will be able to view. The content will appear the same to the viewer no matter who it is visiting your site. This is perfect for a personal website!

In an earlier course in this Course Set, you developed a basic website within R Studio Cloud. At the end of that lesson, you had a website that looked something like this. It contained some basic information about you and had information about where to contact you; however, it was pretty basic and not very visually appealing. In this lesson, we'll improve both the content and look of your personal website.

To get started, create a new project in R Studio Cloud! Once you've got a new project, you'll want to run the following code in the R Console to install blog down and start a new wite. Note: it may take a few minutes for this code to run and for all the dependencies to install. 

For this site, we're using the Hugo theme "Academic", specified as an argument within the blog down new underscore site function. At the end of this lesson, you'll have a website that looks something like what you see here!There are many other themes that can be used within the blog down package. We've chosen to use this one because it does a good job displaying information about your skills and qualifications as well as your projects, which will be important when you are looking for jobs. 

Once you run this code, an "Edit" window will pop up.

Replace the text you see in this document, with a brief introduction about yourself, something similar to what you see here. Click Save. Note that nothing here is permanent. You'll be able to edit all of this later!

A new tab will open up with a preview of your website. But, this doesn't exactly look like that website we were looking at before...what's going on?

Well, in order for the preview to appear correctly, we have to make a slight change to how the website looks for links on the website. To do this, open up the config dot toml file within the project directory.

Search for the line of code that starts with base u r l. After this line, add the following two lines of code highlighted here.Save these changes. The preview of your website should update automatically in that tab that appeared. 

However, if it doesn't, you'll want to run the function you see here. When blog down serve site is run, every time you save a change to the files of your website, the preview will update and you'll be able to see what changes have been made and how they'll appear on your website!

Now that you've edited those two lines of code in config dot toml, your preview should look something like this! 

Now that we have the skeleton of the webiste ready and our theme preview looks as we expected, we're ready to start editing the content of the website. This is where you should edit the text to match your information. Thus, where it says "Jane Doe" in this lesson, put your name in your files. When a description is included, make sure you're writing information about yourself, and not word for word what's in this lesson. You really want employers to know about you! We'll continue to make edits to the config dot toml file. You'll want to edit the name that appears on your website. To do this, edit the name field by placing your name within the quotes. Then, in the role field, delete the text between the quotes, but leave the quotes there. This way, in the future, you'll be able to edit this text and include a role once you have a job! Note that the line numbers within the config dot toml file are shown. For example, the name field is at line 60. You can use these line numbers to help guide you to the approximate spot within each file where edits will need to be made, but note that if you add extra lines, the numbers may not be exact, and that's ok!  The correct At this time, you should also edit the organizations field by adding "Chromebook Data Science" and adding the URL for this program's website in the u r l field. Note that all of this text should be within quotes.

Once you save this file, the changes should be visible on your website preview! On this preview, you may notice that there's a big blank space above your name. There should be a picture there! Because of the way things are set up on R Studio Cloud, a change has to be made before this image can be visible. 

To make this edit, you'll want to navigate to the directory highlighted here within the "Files" tab of R Studio Cloud. There, you'll click on about dot html. Within this file, go to line 13. Here you'll see some unfamiliar code. It's ok not to fully understand this at this point -- we're just going to make two small changes. 

First, add dot slash, as highlighed on the video. Then, edit rel U R L to be abs U R L in that same line. The code should look just as you see here.

Once you save this file, the avatar image should now be visible! 

That's great, but you want this to be a picture of yourself! To do this, you'll want to navigate to the directory highlighted here within the "Files" tab on R Studio Cloud. This is where images you want to display on your website should be stored. 

Upload a image file of yourself to this directory! Then return to the config dot toml file we were editing previously and search for the line that says avatar equals "portrait dot jpg". Change "portrait.jpg" to the name of your image file, as you see here. Specifically, here, we're going to specify that we want to use the "female.png" image. 

Once these changes are saved, the preview of your website should have your image on it!

With the basic information for our website edited and a picture of ourselves now visible on the preview, it's time to edit all our contact information. To do this, we'll continue to make edits within the config dot toml file. Find the lines of code shown here, and delete the highlighted text. By deleting this text, you're removing the icon from below your name that links to your Google Scholar profile, since this won't be necessary for a data scientist.

With that deleted, you'll want to include your information for the other three contact pieces. You should include your email address after mail to colon, your twitter handle after twitter dot com slash and your Git Hub username after github dot com. This is important, since you'll want potential employers to be able to easily jump from one of your professional social media accounts to another and because they should be able to contact you easily!

Once these changes are saved, your preview will be edited. There will now be three icons underneath your name (Google Scholar has been removed) and they will, if clicked, go to your profiles! Here, you see that there are currently six tabs at the top of the preview. However, we won't need all of those tabs. We're going to pare down these tabs to only include the most important information. But, in the future, should you want to add any of these back in, you'll know how to do so.

To start customizing these tabs, we'll want to be sure that your most-recent resume is available on our website! To get started on this, you'll need to upload your resume into the directory highlighted here. Here, our resume is saved as resume dot p d f.

Now, we're ready to start tweaking the tabs available on our website! To do this, we'll still be making edits to config dot toml. Navigate to the portion of the file shown here. Delete the four lines related to "Publications" and the four lines related to "Teaching". The lines you shoudl delete are highlighted here. 

Then, make the following changes. Flip the order of Projects and Post. Then, Change the "weight" for each tab so that they match what you see in the video here. Then, remove the comments from the four lines related to your "Resume", And last, specify the filename of the resume you updated.

Now, once these changes are saved, you'll have five tabs on your website preview. Publications and Talks will have been removed, but Resume will have been added! We're making progress, but information in our Biography, Interests, and Education all have to be edited!

We'll start by editing our interests and education. To do so, we'll have to move from making edits in config dot toml and will start editing a different file. Navigate to the directory highlighted here in the "Files" tab of R Studio Cloud. Click on about dot m d to open that file.

In this directory, change the text within interests to match your interests. You can include more than three interests, but be sure that each interest is in quotes and separated by a comma, as you see here. Be sure to include professional interests here, but it is ok to include a personal interest that you have, such as reading, writing, or a sport you're passionate about! You'll also want to edit your education section. You'll at the very least want to include this program on your website. You can do so using the edits you see here. If you have other educational information to add, you can edit the information included to include your information. Otherwise, delete the second two following sets of code, as you see here.

Upon saving these changes, the following edits will be viewable on the preview. Now it's time to edit your biography! Your biography section should a little bit of information briefly describing your current positions and data science interests! To see exactly what we mean, let's look at a few examples from the websites from people currently working in data science.

Here we're looking at the about section from Nathan Yau's website. In his about me section, Nathan briefly explains what he does followed by where to find some of his work. He finishes with some of his interests outside of work. If you want to see more of Nathan's work, check out flowing data dot com.

Here we have another example from Mona Chalabi, a journalist who generates illustrations from data. Mona introduces what she does, describes where to find her work, and then provides some background information about her professional work.

Our final example comes from someone whose work you've seen throughout this course, David Robinson. In his about me, he mentions his current position and interests, describes briefly some of his work, and provides a bit of background.

These three examples should give you an idea of what to include in the "About Me" section of your website. Generally, consider including you current position, some background information, and what projects you've worked on or would like to work on!

Having looked at a few other individuals' websites, write your biography text in the Biography section of the about dot md document. 

Once these changes are saved, your website preview will reflect these edits.

Things are really coming along! We have all of our contact and necessary information included on our homepage now! But, there are lots of changes we will still want to make before our website is ready. Now, we'll focus on how to improve the overall appearance of our website! While the contact information looks great, there's information at the top of our website that doesn't need to be there. 

We'll remove this text by opening up hero dot m d within the directory highlighted here.. 

In this file, we'll first remove the text between the quotes in the title field. Then, we're going to turn off any image that may display in this portion of the website. Do this by adding a comment before the overlay dash i m g variable.  We'll aslo comment out the call to action button by adding comments  before the last three lines of highlighted code.The last thing you'll want to do is delete everything after the final three plus signs in that file.

Once the file looks as you see above, you're ready to save your changes and preview! The information about the theme will no longer be there!

With those changes, let's edit the skills section of the website. Navigate to direcotry highlighted here and open skills dot m d. This is where you highlight all of your job-pertinent skills! Here, we're suggesting you highlight your "R", "data visualization", and "Data Wrangling" skills. But, you could highlight more than three skills or three different skills! Think about what skills you want employers to know you have and include them here. To add the three skills you see here, edit this document to include the code shown here. Note that the text that will be displayed on your website underneat each icon is specified in name. We've removed the text from the description variable for each skill, but you could shoose to include text here explaining the skill. Then, the icons displayed are specified in icon and icon_pack. Which icon to display on the website is defined in the icon argument and refers to the names of the icons found at Font Awesome Brand, Font Awesome Standard, and Academic Icons. You can search for other icons you'd like to use to highlight your skills throughout these icon packs . If you use an icon from Font Awesome Brand, you would then specify f a b in the icon underscore pack variable. From Font Awesome Standard, you'd specify f a s. And, from Academic Icons, you'd specify a i. 

Once these changes are saved, you'll be able to see the edits on your website preview.

While demonstrating your skills and interests are important on your website, at this point, it's not important to include all of the sections included by default on this theme. So, at this point, we're going to go in and turn a bunch of these sections "off." We won't delete the content. This way, in the future, if you're interested in adding any of this information back in, you'll be able to do so! We'll remove the "Publications," "Selected Publications", "Talks," and "Teaching" sections from your website in this section. The process will be the same for each. First, navigate to the directory highlighted here and open publications dot m d. In this document, where you see active equals true, set that to be active equals false. This will remove this section from your homepage. Save these changes.

In that same directory, open publications underscore selected dot m d. Set active equals false and save your changes.

In that same directory, open talks dot md. Set active equals false and save your changes.

In that same directory, open teaching dot md. Set active equals false and save your changes. Now, when you preview your website and scroll through your homepage, these sections will have been removed.

We opted not to turn off the posts section of your website. Now, we won't specify in this course what to specifically include in this section, but we will encourage you to write blog posts and include them in this section. For now, we'll delete the posts that are already in there, since they're not your blog posts and show you how to write blog posts in the future. 

Navigate to the directory highlighted here. In this directory, you'll se a few files. One of them will be getting dash started dot md If you were to open this file, you'd see all the contents used to write that "Getting Started" post currently on your website. 

While there's lots of helpful information in this post, you didn't write it, so you'll want to delete this file. Another file in there will be 20 15 dash 0 7 dash 2 3 dash r dash markdown dot R m d. This will contain the text we included at the beginning of the lesson in the "Edit" box. You can leave this file for now. There will be time to edit and write new posts later!

After these changes are saved, your Recent Posts section of your website should look like this:

The last thing we'll note is the following. When you are ready to write a blog post, you'll want to use the "New Post" Add-in. To find this, click on "Addins" in R Studio Cloud. Then select "New Post" from the drop-down menu.

This will open up a box where you'll enter the title, author, date, and other information about your post. After entering all the necessary information and clicking "Done," the Add-in will create the file for you to edit it. This is where you will write your blog post!

Aside from including blog posts, you'll also want to include information on projects you've worked on and completed in the projects section. By default, there are two projects included in the highlighted directory: deep dash learning dot m d and example dash external dash project dot m d. Navigate to this direcotry and click on deep dash learning dot m d to open that file. We're going to edit the information in that file to include information about your findl project for this Course Set. Edit the date to today's date. Change the title to the title of your final project. Edit the summary to include a short description of the findings from your project. And, change the tags to match what you did in your analysis. Each tag should be in quotes and separated by a comma. 

Safe this file as atus dash survey dot m d. 

Now, you can delete the other two projects there, as they are not your projects.

The skeleton for your project will then be visible on the preview of your website in the Projects section! But, what are those tags above your project? We'll want to customize those as well!

To do so, navigate to the directory highlighted here and open projects dot m d. Find the section of this file where you see filter within double brackets. Leave the first filter alone, but edit the second filter to look for the tag "R" in your prjects. The last one can be "Other" for now. Use the syntax you see here. Note that these tags correspond to the tags specified in the YAML of your post. These filters will search for any projects with the specified tag. You can have more than three tags as you include more projects over time! 

Once these changes are saved, the new tags will be visible on your preview!

Okay, we've done a lot, but there's one last thing we want to do. At this point, it's more important that future employers see the projects you've worked on than the blog posts you've written. Thus, we want projects to show up before posts. To do this we'll edit the weight argument. Return to projects dot m d. Toward the top, change weight equals 50 to weight equals 40. Save these changes.

Then, within posts.md within the same diretory, change weight equals 40 to weight equal 50. Save these changes. 

Recent posts will now be displayed after projects on your preview:

Your website is now ready for prime time. The only problem is it's only visible on your R Studio Cloud project. So, we have to deploy your website. There are a number of different ways to do this, but we're going to use the workflow with which we're most familiar: GitHub Pages. This is how your website is currently deployed. Your current website is hosted on GitHub at username dot github dot com and the file structure should look something like what you see here:


We're going to delete the current website and replace it with this updated website! To do so, within your current project on R Studio Cloud (where your new blog down website files are), go to the Terminal and run the code  you see here at the top left ...but replace jane everyday doe  with your GitHub username. This will clone your current website repo into the R Studio Cloud project where your new webiste files are.

Click on the directory of the repo where your old website contents are. Then, click on More and select "Show Hidden Files"

Within this directory, you'll see two hidden files dot git and dot no jekyll. Do NOT delete these files, but select everything else, and delete the files from your old website.

Now, we'll need to add all the new files! But, you should NOT add every file you just generated. You only want to add the contents of the public directory. The path to this directory is highlighted in the video. What's great about blog down is that everytime the blog down serve underscore site function nis run, a new preview of your website is generated and all the files needed to deploy your website are updated and added to this public directory. Thus, everything you need to deploy your website is right there. 

Move all the files from this public directory to the repository you just cloned by selecting "Move..." from the "More" drop-down menu. Then, click Choose.

All of your new website files from public should be within the username dot github dot com directory.

We're ready to push these changes to GitHub. To do so, change username in the code here to your GitHub username and run the code in the Terminal. In this code, you're changing your directory to the version controlled directory you just cloned. You're then staging the files using git add  minus A, which will stage all new, modified and deleted files. You're then committing these changes and pushing to GitHub.

On GitHub, these changes will all be visible! 

And, when you go to username dot github dot io, you will be able to see all the changes you've made to make your website more professional! Awesome!