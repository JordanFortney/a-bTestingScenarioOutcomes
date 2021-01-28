# Evaluating Scenario Outcomes With A/B Testing

### Purpose
After I graduated from my Data Science Diploma program the job hunt became my new job. One thing that I noticed while applying for roles in my new field is that it was very common for employers to list A/B testing as a necessary experience. I had touched upon these tests during my program but never in great detail. This realization led me to produce this project and it was extremely beneficial. Not only did it provide me with proof of my skills at conducting A/B tests but it was a very good refresher in basic statistical theory. It also provided me with the opportunity to communicate the importance and meaning of that theory in a way that can be understood by those without prior knowledge.

### Introduction
A/B testing is a very common framework for comparing the outcomes of two scenarios and determining whether that comparison is significant and non-random. These could be two brand new scenarios or a new idea that you want to test against your current strategy. A/B testing will not only outright tell you which scenario is better but it will also tell you whether there is a statistical difference between the two.

This project will investigate two datasets with different inputs and goals. The subject of the first case study is a mobile game called Cookie Cats that looks at retention rate. The second case study that evaluates the effectiveness that an AdSmart advertisement has on the participation rate of a questionnaire for an online auction marketplace.

### Case Study 1: Cookie Cats - Mobile Game
Cookie Cats is a classic mobile puzzle game where you must connect three matching icons to get points and progress through the game's puzzles. As puzzles are completed users will gain experience points and level up their accounts which leads to them encountering more difficult puzzles and obtaining larger rewards. At certain levels there are content gates that require the user to wait a certain amount of time or make an in-game purchase before being able to continue solving puzzles and leveling up further. Cookie cats wants to test whether there is a difference between one scenario where the first content gate at level 30 and another scenario where the first content gate is at level 40. The metrics used to measure this potential difference are:

* total number of game rounds played
* retention after one day
* retention after seven days

The dataset was downloaded from Kaggle: https://www.kaggle.com/yufengsui/mobile-games-ab-testing

There was a 0.043 drop in game rounds played between the gate 30 group and the gate 40 group. Through a proportional z-test it was determined that the difference between the two scenarios was not statistically different.

There was a 0.59% drop in one day retention rate between the gate 30 group and the gate 40 group. Through a proportional z-test it was determined that the difference between the two scenarios was not statistically different.

There was a 0.82% drop in seven day retention rate between the gate 30 group and the gate 40 group. Through a proportional z-test it was determined that the difference between the two scenarios was statistically different.

This experiment was not able to conclude whether shifting the first content level gate from level 30 to level 40 had an affect on the mean game rounds played or the one day retention rate. It was able to determine that there was a decrease in seven day retention rate of 0.82% that was proven to be statistically significant based on a p-value threshold of 0.05. Based on those results this report would suggest that the first content level gate be placed at level 30 to avoid the significant drop in seven day retention.

### Case Study 2: AdSmart Questionnaire Participation

AdSmart is a marketing company who was hired by an online auction marketplace to create an ad that would increase participation in their customer satisfaction questionnaire. AdSmart created a creative and interactive ad to promote this questionnaire and the data resulting from the users who saw that ad and those who saw a generic dummy ad is the subject of the this case study. The focus points of this dataset are the experiment group, exposed or control, and whether or not they interacted with the questionnaire ,yes or no. There is also a number of other metrics included that can be used to pinpoint whether the AdSmart ads were performing better in some environments versus others.

This dataset was downloaded from Kaggle: https://www.kaggle.com/osuolaleemmanuel/ad-ab-testing

There was a 1.21% increase in the participation rate by the users who were presented the AdSmart ad versus those in the control group. Through a proportional z-test it was determined that the difference between the two scenarios

With the positive influence of the AdSmart ad confirmed we could dig a little deeper and test whether there was a difference in participation based on the time of day or browser used to interact with the ad.

There was a 0.88% increase in the participation rate by the users who were presented the AdSmart ad during the night compared to those who were presented the ad in the evening. Through a proportional z-test it was determined that the difference between the two scenarios

Finally, there was a 2.36% increase in the participation rate by the users who were presented the AdSmart ad in an application compared to those who were presented the ad on mobile. Through a proportional z-test it was determined that the difference between the two scenarios The differences between all other platform type pairs were not determined to be significant.

Based on the results of this report, it would be suggested that the AdSmart ad be implemented for all users. It is also likely that there would be an increase in participation if resources were focused on ads in application platforms over those on mobile platforms.

### Final Thoughts
Determining whether or not there is a numerical difference between the outcomes of two scenarios is not a difficult thing to calculate. You simply subtract the results or rates of one scenario from the another. The difficult part is parsing out which outcomes could have occurred on their own had no changes been made at all. Randomness will always be present when taking samples for analysis and it should be taken into account when using data to make decisions regarding any change to a system or product. When making even relatively small changes, such as the positioning or size of an ad, statistical methods must be used to verify that the differences in the scenario outcomes was not due to the randomness that is ever present in data analysis. The application of A/B testing will provide confidence in the results of an experiment and allow those changes to be applied without hesitation or worry that they are not truly significant.
