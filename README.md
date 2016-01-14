# VisualizationProject
This below is a link to my intial proof of concept, that I ended up sharing so that I could get feedback on it.
http://bl.ocks.org/datalord123/4ab8e1c4ec83a7ced3bd

Summary: I had read a story a little while back about population growth slowing down in developed countries and that one of the reasons this was happening was because women were choosing to have children later in their lives(http://www.theatlantic.com/business/archive/2014/09/the-recessions-baby-bust/380909/). So this made me curious as to the scale of how this change has happened over time. To answer this question I pulled the past and projected data from the UN population division's website, and tidyied it up(double entrendre intentional) so that I could visualize it in d3. The results I found were actually pretty interesting. You can see that not only is this trend extremely strong in terms of magnitude, but it also is projected to continue over the foreseable future.

Design: While i played around with using a time series graph(line),I ended up deciding to make a horizontal bar chart because I thought it was easier to interpret iterating over the different periods. Other notable design features included having the play all button be colored different(indicating interactivity),having the curser change into a pointer when hovering, and bolding the period button that was currently activated. The next major design decision I made, was changing the maximum range on the x axis, so that it represented the maximum range for the entire dataset, vs just the different periods. I did this because it ended up being too confusing having the x axis change with different iterations, as it was more difficult to compare periods together apples to apples. This focus on ease of comparison was also why I decided list the age groups on the Y axis in ascending order. In the course of my research, I came across a couple of articles that stated that the standard for portaying age in vertical bar chart like this is to list the age(age groups) in descending order. However, after testing this out, I realized that most of the changes were taking place at the lower age brackets. So in this case, I decided to list the age groups in ascending order, because I wanted viewers to see the incremental changes as easily as possible.

My design also changed a couple times based on reviewer feedback. For instance, I intially had data going back to 1950, but a couple of people noticed that between the years 1950-1975 the percentage of younger people actually increased. Since the purpose of this graph was to portray the trend of US women choosing to have chilren later in life, i thought having effectively 30% the visualization show the opposite trend might be confusing. Also, removing these six buttons had the added bonus of elimating some of the crowding that was occuring from having so many periods. Another thing I did based off this feedback was to clarify the remaining periods a little bit better. Intially the periods were listed as follows (1950-1955,1955-1960,etc). While the intent was that the reader would understand that they were 5 year periods starting from the first year, it actually came off as a little confusing and reviewers had trouble easily discerning the ranges. 

Feedback: 

The first feedback I received was from rommel_1715287040. His advice was extremly useful, and I actually included most of his comments as changes to my Project. Specifically, he was the first to notice that the first couple periods in my visualization included an INCREASE in the percentage of births by younger women. He also asked me to clarify a number of points re: my projections, and the process through which I acquired my data. Other points that he made related to overcrowding for the periods, and including a pause button. I ended up addressing all of his points, minus the last one. While my code has the ability to stop the PlayAll loop by clicking a year, I decided against emphasising this with a dedicated button for two reasons. 1) I had already removed around 30% of the initial periods, which dramatically shortened the total play time 2) I wanted to do as much as possible to encourage viewers to watch the whole playthrough. While the graph was fully interactive, I wanted to first make sure viewers watched the story I wnanted to tell, before I let them play around with the chart themselves. 

The second feedback I got was from michael_201137. After reviewing my the iteration that resulted from rommels comments, his reaction essentially boiled down as follows: 1) The story behind the narrative of the visualization was much clearer and could easily be interpreted. 2) The title of the chart "Births by Age of Mother-USA " was slightly confusing to him, as he could also interpret it as "Mother USA" similar to "Mother Russia". 3) It would be helpful to add text explaining the reasons behind some of the trends, namely why 45 year olds weren't having any kids, and thoughts as to why younger women were having less kids. 

As a result of his comments I changed decided to make a slight change to my Title, that i thought could help with his dual interpretation issue. Specifically I replaced the dash with a colon so that it looked like the following "Births by Age of Mother:USA". More significantly, I decided to add expalantory text certain periods in the visualization, so that I could better explain what I,and others,think may be going on. 

The third feedback I received was from zai_feng_241600 who looked at my chart and decided he couln't think of anything he'd change. While I appreciated the compliment, I really wanted to see if i could do something else to improve my visualization, so I asked my brother. When my brother looked at the visualization, he actually pointed out something really useful, which was that the X axis ticks were incremented by pretty large values relative to the data set, additionally, there were frequent cases during the playthrough where the maximum bar width went beyond the maximum assigned D3 tick value. To fix this, I changed the number of ticks from 5 to 10. D3, being the helpful tool that it is, used this new input to decide that the chart would actually look better with 8 ticks instead, with the new maximum tick going up to .35 (from .30 previously).


Resources: In addition to the udacity course, I had to read an absurd number of articles(to many to list here) by Mike Bostock, Scott Murry and others. Some of the helpful articles were
The Let's Make a BarChart Series
http://bost.ocks.org/mike/bar/
The Dashing D3 Tutorials
https://www.dashingd3js.com/svg-basic-shapes-and-d3js
Thinking with Joins(This was huge)
http://bost.ocks.org/mike/join/
Jerome Cukier's
http://www.jeromecukier.net/blog/2012/05/28/manipulating-data-like-a-boss-with-d3/

I also ended up reading 2 Very Large e books in order to get a better macro
perspective of the language

D3-Tips and Tricks by Malcolm Maclean 
Visual StoryTelling with D3 by Ricthie S. King




