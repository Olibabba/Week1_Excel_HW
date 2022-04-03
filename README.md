# Kickstarting with Excel

## Overview of Project

In a previous analysis I looked at the success of kickstarters in the US, and of kickstarters for theatre projects, and plays specifically. I was then able to determine an ideal fundraising goal to increase the odds of success for a new play. After this analysis my client launched their kickstarter and has raised a significant portion of their goal. 

### Purpose

Now, to give my client some expectations of the path ahead and to strategize for success, I will continue my analysis. This analysis will look at the outcomes of other kickstarters based on launch date and based on initial goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

In order to analyze the outcomes based on launch date I made a pivot table and chart. With the results filtered so only theatre kickstarters are included, I made years as a filter and removed it from the table. This way all the outcomes could be condensed into a single year to see which times of year prove more or less successful to launch a kickstarter. 

![Outcomes BAsed on Launch Date](https://github.com/Olibabba/Week1_Excel_HW/blob/homework_prep/Resources/Theatre_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

In order to analyze the outcomes based on goals I manually made a table to compare outcomes depending on different ranges of goals. The ranges used are below 1000, then increments of 5000 up to 50000, and then above 5000. This analysis was done only on the "plays" subcategory. 

![Outcomes Based on Goals](https://github.com/Olibabba/Week1_Excel_HW/blob/homework_prep/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

I came acrosss a few challenges and difficulties in this process. In particular some graph formatting and formula challenges.

#### Graph Challenges

The outcomes based on goals graph gave me some trouble. First it didn't lok like the example given in the module, and I jus couldn't pinpoint why that was. Then I realized that the table sorted "less than 1000" to the last row, which put that entry at the end of the graph. It took some more time to figure out that I could manually reorder table items. 

![Out of Order Table]()

Then I had some frustration trying to remove the markers on the same graph. This was probably not a make or break issue. But the example given in the module had smooth lines without markers, and doggon it mine was going to look the same. After some trial and error I finally found the correct setting.

#### Formula Challenges

Putting together the table for outcomes based on goals was a challenge.

In order to arrive at the final formula to calculate the number of successful, failed, and cancelled plays, based on various fundraising goals, I ran into a few hang ups.

The final formula, example shown below, has the goal range broken into two seperate conditionals. But this solution was not initially apparent to me, and it took some trial and error and some time on Google to arrive here.
```
=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<=4999",Kickstarter!$R:$R,"plays")
```
I also got stuck trying to save myself some work retyping the formula over and over, and spent quite a while getting the cell parameters locked in using the "$". This was one of those silly issues that took a little too long to figure out.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

 THe primary conclusion drawn from this analysis is that May is the best month to start a kickstarter, followed closely by June. The second conclusion is that winter is not a good time to begin a kickstarter. While it is clear that there are many more campaigns started in the summer than in the winter, the number of failed campaigns remains relatively stable, so these conclusions are sound.

- What can you conclude about the Outcomes based on Goals?


- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
