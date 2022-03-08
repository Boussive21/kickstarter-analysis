# kickstarter-analysis
## Overview Project: On 2/22/22 We where given a data set Kickstarter that have been that tracked a couple thousand projects since 2009 to 2017. The dataset kept track of how much was pledged the unix code of time it was launched and its deadline. The purpose of getting this data and analyzing it is to look at what Kickstarter in particular Theater and Play categories are successful, which failed, and which have been canceled. We also looked at what pledge goal range did these succeed or failed/canceled and how many. 
## Analysis and Process:
### Challange: We started of by changing the original launched and deadline values and putting those a different column which we called date created and date ended. We accomplished this by using this formula =(((J2/60)/60)/24)+DATE(1970,1,1) and inputting that into Date created column then used the same formula but changing J2 to I2. Completing this formula made it come out as decimals but formatting and into general dates. After this we where able to extract the Year using a year function(=year) on the Dates columns. I also changed the Category and Subcategory using Text to column function delimit then backslash. This created two categories which were called parent category and subcategory. The difficult part of this was converting the raw time that we get from our Dates created formula to dates because I did not know about having to +Date (1970,1,1) as well as changing it manually in excel 
### Theater: After completing these preliminary steps, I made a pivot chart which measured date created and count of outcomes and whether they were canceled, failed, and successful. I filtered out all other parent categories except theater. Leading to the result like may being the most times theaters Kickstarter get “started” as well as being the time of year that led to most success (111) and failures (52) in the theater category.  
### Process Outcomes:Lastly we created a table that measured goals from 1000.00 less than to greater than 50000.00 and whether they were successful or failed/canceled. I used and countifs statement that only measured if the goal was in a specific range and in the subcategory plays(ex,= =COUNTIFS('Kickstarter data'!$D:$D, "<1000",'Kickstarter data'!$O:$O,"plays",'Kickstarter data'!$F:$F,"successful")). Then measured the percentage success or failure by dividing that result over the grand total. What we can found that the most successful range in terms of total was between 1000.00 to 4999.00 range with 340 it also happens to have the most failures with 128. But in terms of percentages the most successful ranges as the less than 1000.00 range with 75.81 and the least successful was 40,000.00 to 49,999.00 with 100.00 percent failure rate but this can be viewed as an outlier because it only had 1 total that falls in that range as a whole. Eliminating that would leave greater than 50,000.00 with and 87.50 percent failure rate.
## Results:From the data that ran and made into tables we gathered two conclusions from the theater data sheet we can gather that starting in Theater category you are more or likely to succeed with your Kickstarter because most of the Kickstarter did succeed. Another thing that we can conclude from the data is that summer months (May through July) where when more Kickstarter started. As for the outcome plays data sheet, we can of the more expensive your goal the more or likely it is going to fail the threshold being around 20000.00 which is when the majority of Kickstarter failed more by percentages. While we did come up with those conclusions from the data it is difficult to say whether there was enough data to be substantive within context of the data given in the initial Kickstarter with over 4000 data entries Theaters making up only under 1500. Another limitation of the data set is for the sake of the dataset there is no respective difference between failed and canceled except probably a bruised ego from the Kickstarter team, for the sake of filtering they function very similarly and don’t provide enough difference to be worth being categorized. 
  ![Outcomes_vs_Goals](https://user-images.githubusercontent.com/99147715/155653858-f50eb652-6ed2-4a9a-bf86-7bbda8df0a4a.png)
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/99147715/155653913-8ae27c66-da44-4416-b516-78ae16ad743d.png)

[Kick_StarterChallange.zip](https://github.com/Boussive21/kickstarter-analysis/files/8202256/Kick_StarterChallange.zip)
