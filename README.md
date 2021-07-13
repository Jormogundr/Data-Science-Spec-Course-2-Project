# Data-Science-Spec-Course-2-Project
Applied Data Science with Python Specialization Course 2 project.

This repo contains my submission for the final project in  ourse 2 of 5 in the Applied Data Science with Python Specialization on Coursera. The project description is below.

# Assignment 4

Before working on this assignment please read these instructions fully. In the submission area, you will notice that you can click the link to **Preview the Grading** for each step of the assignment. This is the criteria that will be used for peer grading. Please familiarize yourself with the criteria before beginning the assignment.

This assignment requires that you to find **at least** two datasets on the web which are related, and that you visualize these datasets to answer a question with the broad topic of **sports or athletics** (see below) for the region of **Ann Arbor, Michigan, United States**, or **United States** more broadly.

You can merge these datasets with data from different regions if you like! For instance, you might want to compare **Ann Arbor, Michigan, United States** to Ann Arbor, USA. In that case at least one source file must be about **Ann Arbor, Michigan, United States**.

You are welcome to choose datasets at your discretion, but keep in mind **they will be shared with your peers**, so choose appropriate datasets. Sensitive, confidential, illicit, and proprietary materials are not good choices for datasets for this assignment. You are welcome to upload datasets of your own as well, and link to them using a third party repository such as github, bitbucket, pastebin, etc. Please be aware of the Coursera terms of service with respect to intellectual property.

Also, you are welcome to preserve data in its original language, but for the purposes of grading you should provide english translations. You are welcome to provide multiple visuals in different languages if you would like!

As this assignment is for the whole course, you must incorporate principles discussed in the first week, such as having as high data-ink ratio (Tufte) and aligning with Cairo’s principles of truth, beauty, function, and insight.

Here are the assignment instructions:

 * State the region and the domain category that your data sets are about (e.g., **Ann Arbor, Michigan, United States** and **sports or athletics**).
 * You must state a question about the domain category and region that you identified as being interesting.
 * You must provide at least two links to available datasets. These could be links to files such as CSV or Excel files, or links to websites which might have data in tabular form, such as Wikipedia pages.
 * You must upload an image which addresses the research question you stated. In addition to addressing the question, this visual should follow Cairo's principles of truthfulness, functionality, beauty, and insightfulness.
 * You must contribute a short (1-2 paragraph) written justification of how your visualization addresses your stated research question.

What do we mean by **sports or athletics**?  For this category we are interested in sporting events or athletics broadly, please feel free to creatively interpret the category when building your research question!

## Tips
* Wikipedia is an excellent source of data, and I strongly encourage you to explore it for new data sources.
* Many governments run open data initiatives at the city, region, and country levels, and these are wonderful resources for localized data sources.
* Several international agencies, such as the [United Nations](http://data.un.org/), the [World Bank](http://data.worldbank.org/), the [Global Open Data Index](http://index.okfn.org/place/) are other great places to look for data.
* This assignment requires you to convert and clean datafiles. Check out the discussion forums for tips on how to do this from various sources, and share your successes with your fellow students!

## Example
Looking for an example? Here's what our course assistant put together for the **Ann Arbor, MI, USA** area using **sports and athletics** as the topic. [Example Solution File](./readonly/Assignment4_example.pdf)


######################


Q. State the region and the domain category that your data sets are about (e.g., Chaohu, China and sports or athletics).
A. Michigan collegiate sports including Ann Arbor and Lansing

Q. Create a research question about the domain category and region that you identified.
A. This visualization examines the win rates of two local universities (famous rivals) across four different sports leagues, namely: soccer, football, hockey, and basketball. Only the men's divisions are considered. Historical data freely available on Wikipedia is examined.

Q. Provide at least two links to publicly accessible datasets. These could be links to files such as CSV or Excel files, or links to websites which might have data in tabular form, such as Wikipedia pages.
A. 

https://en.wikipedia.org/wiki/Michigan%E2%80%93Michigan_State_men%27s_ice_hockey_rivalry

https://en.wikipedia.org/wiki/Michigan%E2%80%93Michigan_State_men%27s_basketball_rivalry

https://en.wikipedia.org/wiki/Michigan%E2%80%93Michigan_State_football_rivalry

https://en.wikipedia.org/wiki/Michigan%E2%80%93Michigan_State_men%27s_soccer_rivalry

Q. Provide a short (1-2 paragraphs) justification of how your visual addresses your research question.
A. The goal of this visualization was to provide an easy visual method to compare win percentages of the football, soccer, basketball, and hockey leagues for the University of Michigan and Michigan State University rivalry. Note that data for the soccer league did not start (according to the Wikipedia page) until 2000. The rolling average was tabulated from data collected prior to the minimum x-axis range shown on the graph for football, hockey, and basketball. A 10 year average helps to identify trends in the performance of either team (the win percentage of Michigan state is simply the complement of the plotted win percentage for U of M).

We can see that the early history of the leagues shows U of M dominating (except for soccer), while in more recent decades the balance has shifted toward Michigan State's favor. Within the past decade, we can easily see which team has excelled (winning more than half the games).


Q. As this assignment is for the whole course, you must incorporate and defend the principles discussed in the first week, specifically, Cairo’s principles of truth, beauty, function, and insight.

For each of the following prompts, please provide a response that links each principle to one or more elements of your visual. 

Describe your design choices for your visual in regards to Cairo's principle of truthfulness.
Describe your design choices for your visual in regards to Cairo's principle of beauty.
Describe your design choices for your visual in regards to Cairo's principle of functionality. 
Describe your design choices for your visual in regards to Cairo's principle of insightfulness. 

A. 
truthfulness - a large swath of historical data is used in tabulating the win rates, and 1930 is around the time when the hockey, basketball, and football matches were played between the two universities on at least an annual basis. This data is displayed to give the whole story.

beauty - A large graph is generated, with a larger width since the plot of the x axis data covers a larger range of interest than the y data. The y axis labels are duplicated on the right hand side of the figure to allow easy comparison of recent win rates. Font sizes were increased to increase readability. This choice of duplicate axes means I did not have to include a grid, which might increase visual fatigue on the part of the decoder

functionality - tick marks including 0.5 on the y-axis were chosen to allow for the vital comparison of which team wins most of the time (obviously it's the better university, UM )

insightfulness - the combined principles add up to give the decoder an effective visual for comparing items of potential interest

Q. How did you go about creating the visualiztion?
A. First, Selenium was used to scrape HTML sources (wikipedia articles) for tables. The tables were stored as pandas dataframes. 

Next, the data was cleaned. This included using regular expressions to clean the data from footnotes and uncessary characters. The tables were indexed by date.

Then, the rolling average was tabulated for each sport, and finally displayed using matplotlib.
