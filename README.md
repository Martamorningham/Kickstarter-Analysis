# Kickstarter-Analysis
## Overview of Kickstarter Analysis Project
The goal of this project was to help Louise analyze various Kickstarter campaigns to help her determine how successful other Kickstarter campaigns were based on their launch dates and funding goals. In this analysis I focused on campaigns that were in the same parent or subcategory as Louise’s Play, Fever. I then drew conclusions based on the campaigns launch dates and funding goals. 
I started with 9 parent categories and 41 subcategories, that were combined in one column. Since Louise’s Kickstarter was a Play, we wanted to focus on the theater parent category and the play subcategory. To do this, I broke Column N “Category and Subcategory” into two different columns Q “Parent Category” and Column R “Subcategory” so I could filter the out other campaigns and focus on the same industry as Louise. I also color-coded campaigns based on their percentage funded, which was done as a gradient from red to blue. As you can see in the picture below, campaigns under 100% funded are in red, while anything over 100 is in Blue. If a campaign was right at 100% it came through as purple. 
   
## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
I took the data and created a pivot table that showed Canceled, Failed, and Successful campaigns by month. At the end of this pivot table, I also created the % success for each month. This made it even easier to notice trends throughout the year. 
1: Campaigns launched in the summer are more successful, especially when launched at the beginning of the summer. The four most successful months in order are May, June, July, and August. However, August has a below average success rate, and is also the fourth least successful month to start a campaign. 
 
2: Kickstarts are not only less likely to succeed in the winter, they are less likely to be started. Particularly over the holiday months of November, December, and January. The average theater Kickstarter is successful 60.46% of the time. While December is the only month that drops below 50%, January, October, and august are all below the Mean success rate. 
### Analysis of Outcomes Based Goals
Instead of creating a pivot table, this time I created my own worksheet that pulled data from the Kickstarter worksheet, to illustrate the success rate of campaigns based on their funding goals.  The first line of campaigns with goals under $1,000 was pretty easy to create. Using COUNTIFS(Kickstarter!D:D,"<1000", Kickstarter!F:F, "successful",Kickstarter!R:R, "plays") 
This told excel to look at the Kickstarter worksheet and pull any transaction that met all three conditions. It had to be less than $1,00, successful, and a play. The second line is where I had some challenges creating this table. This will be further addressed in the Challenges and Difficulties section. 
Plays under $5,000 are far more frequent and successful than any other goal. While plays with funding goals between $35,000 and $45,000 were the next most successful group, they only had a total of 9 projects compared to the 720 campaigns with a goal less than $5,000.  
 
### Challenges and Difficulties Encountered
I ran into issues using Countifs greater than, less than. In particular, I had a hard time determining where to put the less than. I first tried it as one argument, and then added it to the end. I was finally able to understand that I was looking for the count of “successful” Kickstarter’s based on play. So the less than, needed to be my third criteria, as seen here:
 =COUNTIFS(Kickstarter!D:D,">=1000", Kickstarter!F:F, "successful",Kickstarter!D:D, "<5000",Kickstarter!R:R, "plays")

## Results
Upon reviewing the data, I was able to make a few conclusions based off both the theater outcomes by launch date graph and the outcome based on goals graph. The first conclusion, is that early summer is the most popular time to start a theater Kickstarter. It is also the most successful time to start a theater campaign, possibly because people are more likely to spend their summer break engaging in experiences like going to the theater. From this data you can also tell that most (more than half) of theater campaigns are successful, no matter the time of year. In fact, the main dips tend to coincide with Holiday months like November, December, and January, which could be a result of holiday spending leading people to not contribute as much to Kickstarter’s in these months. When looking at the Outcomes based on Goals table, it becomes clear that a smaller Goal is much more likely to meet its goals than Goals over $5,000. That said there are 9 campaigns with goals between 35000 and 45000 that were successful 67% (rounded up) of the time. However, these are outliers and skew our data since the majority of play campaigns have a goal of less than $10,000. I believe the data could be even stronger if we had more understanding into the reasons that campaigns did not reach their goals. That said the data provided, could have also been used to create a table that shows the outcome based on the average donation size or number of contributors. I believe both of these graphs could have helped to determine what metrics best indicate the chance of success for a Kickstarter campaign. 
