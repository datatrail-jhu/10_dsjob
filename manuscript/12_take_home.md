# Practice Take-Home Data Analysis

A common part of a data science interview often involves some type of take-home analysis. Sometimes, the analysis will take a few hours to a few days and you'll be given a week from time of receipt to when you have to return the analysis to the company. Other times, you'll have two hours from time of receipt. The company will inform you of the format and then you'll be off to complete the project!  

### Read the Instructions

Think of the take-home as a homework assignment. You have your notes and resources (aka the Internet) at your disposal and will be working from the comfort of your computer. This means that when you get the project, the first thing you should do is read the instructions. Then, *read the instructions again*. Keep reading the instructions throughout the process. You wouldn't want to do poorly on this assignment because you were unable to follow instructions.

![Read the Instructions](images/12_take_home/12_dsjob_take_home-1.png)

Often these projects will describe a scenario that you may find yourself in at the company. This is helpful for two reasons: 1. It makes the project realistic, since it's based off something that actually happened in real life and 2. it gives you an idea of the types of problems and data you'd be working with at the company. It gives you a chance to see if you'd like the work!

For example, consider the hypothetical situation that data scientists at [Etsy](www.etsy.com) - "a global online marketplace, where people come together to make, sell, buy, and collect unique items."- give you a take-home assignment during your interview where they provide sales data from their site and information about changes to their site over time. It is then your job to determine what changes were most effective. It would be your job to read the instructions, determine what you need and what you have to answer the question and then to analyze the data.

### Plan 

After reading the instructions through *at least* twice, it's **time to plan**. Take time to think about the question and devise a plan. Think about:

* What information would I want to have in a perfect world to answer this question?
* What variables do I actually have? 
* How many observations do I have?
* What type of analysis should I use? Predictive? Inferential? 
* What statistical analysis would be appropriate for this type of data?
* How do I plan to visualize the results? What would that look like?

As you begin to answer these questions and devise an approach, you'll want to **keep it simple**. Remember, this is only supposed to take you a few hours so you're limited in how much you'll be able to get done. Start with simple models and then work toward more complex. This is how all analyses should be done, so this will demonstrate that you have a reasonable approach to analysis, rather than just starting with the most complex, confusing, and newest approach out there. 

Finally, you should be **forming your data science question** at this point in time. The questions you'll want to ask in your analysis will likely not be spelled out explicitly in the assignment. It will be your job to determine what the right questions to ask are and what you'll do to answer them. Consider what the instructions say, form the specific questions you'll ask in your analysis and be sure that these questions are in-line with what the instructions ask of you. 

For our hypothetical Etsy example, maybe we decide we're most interested in answering the question: "Do large overhauls to the website increase sales more than small changes?" This seems like a reasonable place to start and a fairly straightforward question to answer. For this question we'd need to determine from the data we've been given which changes were large and which were small. Then, we'd need to calculate changes in sales associated with each website change. We'd use these data in our analysis to answer our question of interest.

However, this is not the *only* question we could have asked. Thus, we would want at this point to refer back to the instructions to make sure the questions we're asking *actually* fit with what was asked of us in the assignment. We'd want to determine all the question (or questions!) we'll answer with our analysis at this point in time and ensure that they're **appropriate for the assignment**.

At this point you should also be deciding on **what tools you'll use**. In an ideal world you'll know at this point what tools and programming languages the company uses and you would demonstrate knowledge of those. However, do not use tools with which you're unfamiliar if you won't be able to complete the assignment. Better to use tools you know and complete the project than to flail trying to learn a completely new language while completing this project.

### Analyze

After determining the questions we'll ask during the analysis and with a general plan in hand, it's time to do the analysis! 

#### Data Cleaning

The first step should *always* be data cleaning. Be sure that the data are what you expect them to be. Are there missing values? Do the values you have make sense? Are there outliers in your variables of interest? Explore the data and become comfortable with the information you have before moving on.

![Clean the data](images/12_take_home/12_dsjob_take_home-7.png)

The amount of cleaning you'll have to do will depend on the data you've been given. For shorter assignments you will likely be required to do less than longer assignments, but you'll always want to check clean the data before moving on to analyses. Trusting the data and not checking it before an analysis is a red flag to any data scientist -- you *always* want to check the data before analysis.

#### Exploratory Data Analysis

Once you have your dataset in a workable format, you'll *always* want to do an exploratory data analysis. Generate some exploratory plots that help you better understand your data. How many observations do you have? What are the typical values taken for each of your variables of interest? How are they related to one another?  

![Explore the data](images/12_take_home/12_dsjob_take_home-8.png)

In our hypothetical Etsy example from above, maybe you would plan to do an exploratory analysis looking at sales over time. You'd generate a plot to look at the relationship between these two variables.

![Sales over time dummy plot](images/12_take_home/12_dsjob_take_home-9.png)

You'd determine whether or not there are outliers. You'd work to understand any spikes or dips in sales. You'd consider seasonal effects. 

![Considering the data](images/12_take_home/12_dsjob_take_home-10.png)

Basically, you'd *think* about any results you generate. Then, after understanding this relationship, you could add in information about when changes to the site were made and start to understand how those affected sales.

#### Regression Analysis

Whether the assignment asks for an inferential or predictive analysis, you'll likely want to carry out some type of regression analysis to assess the relationship between variables. When you carry out your regression *start simple*. Your model can become more complex from here if need be, but always start with a simple model and understand and interpret that model before generating anything more complicated. 


![Start simple](images/12_take_home/12_dsjob_take_home-11.png)

For our hypothetical Etsy example, the prompt suggests that this is an inferential analysis looking to better understand the effects of website changes on sales. The assignment does not ask us to predict anything, so we wouldn't want to use predictive analysis tools. We'd start by assessing the relationship between sales and time. If sales have gone up linearly over time, we'd use linear regression. If there was not a linear relationship, then we'd consider a more appropriate analytical approach, but we'd start with the simplest (while still appropriate) approach possible.

![Use appropriate approach](images/12_take_home/12_dsjob_take_home-12.png)


#### Visualize

After you've carried out your analysis, you'll want to convey your results effectively -- this could require a few plots or tables. Regardless, you'll want to generate visualizations that demonstrate the results of your analysis in an effective an appropriate manner. Be sure that axes are labeled, that the text and points are large enough and that the appropriate graph has been used. 

![Visualize your results](images/12_take_home/12_dsjob_take_home-13.png)

For our hypothetical Etsy example, you'd certainly want to visualize sales over time. You'd want to be sure the axes are labeled clearly and that the title of your plot explained the important message being conveyed by the plot. You'd additionally want to include either a table of your regression results or a visualization demonstrating the regression line on the data. You'd want to **summarize all important results using effective tables and figures**.

![Communicate results through figures and tables](images/12_take_home/12_dsjob_take_home-14.png)

### Clean Up

With the analysis complete and your question answered, it's time to get the project ready to go back to the company. You don't want to hand them an analysis that is messy or a report that can't be easily followed. Refer to the information in the "Written and Oral Communication in Data Science" course in this course set to generate an effective report or presentation (depending upon what they ask you to do!).  Remember, communication is an important skill of a data scientist! Communicating the results of the take-home assignment effectively is *part of the interview*.

#### Organize

Throughout your analysis process you'll have written code and generated plots that do not need to be in your final report or presentation. After you've done the analysis, you'll want to take the time to determine what code and which plots you'll need to **tell a story**. Organize your thoughts and plan how you'll want your final report to be organized.

#### Write it Up

Once organized, it's time to write up your report. Be sure this report tells a story. It should include the questions you were asking, a description of the dataset, an explanation of your approach, your analysis, your results, and a conclusion.

Include clear explanations of what you did, the code, and all necessary graphs and tables. For our purposes, this will likely be an R Markdown report, which is a *great*  way to communicate an analysis effectively.

#### Proofread 

Last but not least, you'll likely be tired at this point in the process but *don't skip proofreading*. Take the last few minutes to read what you've written, to check for typos, and to make sure it all makes sense. Attention to detail is important for data scientists, so be sure to hand over an analysis that has been proofread and is clear. 

### Take-Home Assignment Example(s):

- https://github.com/wikimedia-research/Discovery-Hiring-Analyst-2016
- GovEx? 
- Kyle Scot Shank

### Summary

### Additional Resources

* [19 Free Public Data Sets for Your First Data Science Project](https://www.springboard.com/blog/free-public-data-sets-data-science-project/)
* [Ways to Prepare for the Data Challenge](https://www.quora.com/What-are-some-ways-to-prepare-for-a-data-challenge-with-a-Silicon-Valley-tech-company-How-do-I-make-sure-I-have-sufficient-fluency-with-data-munging-and-ML-in-Python)

### Slides and Video

![Practice Take-Home Data Analysis](YouTube Link)

* [Slides](https://docs.google.com/presentation/d/1TfGSuh2J-BqXJvqXRf-7548Lzr72eoYGny5R-Bb4n9w/edit?usp=sharing)


{quiz, id: quiz_11_take_home}

### Practice Take-Home Data Analysis quiz

{choose-answers: 4}
? Which of the following describes the *best* approach to carrying out a take-home data analysis project?

C) Read the Instructions x2 > Think & Plan > Clean the Data > Explore the Data > Analyze the Data Simply > Visualize the Data > Organize & Write
C) Read the Instructions > Read the Instructions agan > Think & Plan > Clean the Data > Explore the Data > Analyze the Data Simply > Visualize the Data > Organize & Write
o) Read the Instructions > Think & Plan > Clean the Data > Explore the Data > Analyze the Data Using the Most Complex Model You Know > Visualize the Data > Organize & Write
o) Explore the Data > Analyze the Data > Think & Plan > Clean the Data >  Visualize the Data > Organize & Write
o) Analyze the Data > Write The Report
o) Panic > Analyze furiously > Try to Organize Your Thoughts > Send the company whatever you have when your time limit is up

{choose-answers: 4}
? Which of the following statements is TRUE about take-home assignments?

C) Data Cleaning and Exploration are critical steps.
C) Effective communication is important, so take time to figure out how to tell a story. 
C) You should read the instructions multiple times.
o) Complex analyses are better than simple analyses.
o) The analysis is the most important part, so start there.
o) Your code matters most. Focus time there. Don't worry about explanations.
o) Visualizations should be quick and dirty.
o) Always use the tools used by the company.


{/quiz}

