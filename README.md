# A/B-Testing
Perform pairwise chi-square tests on five tested website versions based on the Montana Library case study

![grafik](https://user-images.githubusercontent.com/100354393/208067598-55360558-c73a-4246-a0ae-36bb607f7603.png)

# Use Case
Data and use case for this project is taken from a Case study that tried to improve library user experience with A/B testing. Process and principles of this
study have been published by the author Scott W. H. Young in the Journal of Library User Experience here:   
[Young, Scott W.H. (2014). Improving Library User Experience with A/B Testing: Principles and Process. Weave, Journal of Library User Experience, Volume 1(Issue 1), doi:https://doi.org/10.3998/weave.12535642.0001.101.](https://doi.org/10.3998/weave.12535642.0001.101)

The library tried to improve their website. The analysing team found the following interaction pattern: Below the library picture, there was search bar and three big items: “Find”, “Request” and “Interact” (like in the picture at the top of this file). All three of them contained access to important information and services that the library prides itself in offering. However, the Website Analytics show that the “Interact” button has, ironically, almost no interactions. 

We cite from the report:       

      The click-through rate for Find was 35%, Request was 6%, and Interact was 2%. This observation prompted a question: “Why are Interact clicks so low?”   
      At this time, the content beneath Interact included links to Reference Services, Instruction Services, Subject Liaisons, Writing Center, About,    
      Staff Directory, Library FAQ, Give to the Library, and Floor Maps. The library’s web committee surmised that introducing this category with the    
      abstract term “Interact” added difficulty and confusion for users trying to navigate into the library website homepage. Four    
      different category titles were then proposed as variations to be tested: Connect, Learn, Help, and Services.

So after conduction further interviews with the users and some brainstorming, the website team settled on 4 different new versions to test against the original “Interact” button:
- Connect
- Learn
- Help
- Services

The metrics that were deemed relevant enough to be tracked were the following: 
- Click-through rate (CTR) for the homepage. Amount of clicks on the button divided by the total visits to the page. Selected as a measure of the initial ability of the category title to attract users
- Drop-off rate for the category pages. Percentage of visitors who leave the site from a given page, selected as a measure of the ability of the category page to meet user expectations.
- Homepage-return rate for the category pages. Percentage of users who navigated from the library homepage to the category page, then returned back to the homepage. This sequence of actions provides clues as to whether a user discovered the desired option on the category page; if not, the user would likely return to the homepage to continue navigation. Homepage-return rate was therefore selected as a measure of the ability of the category page to meet user expectations.   

# Goal
The goal is to perform pairwise chi-square tests on the five tested website versions from Montana Library case study to find out 
which of the five tested versions performed best in the A/B-Testing the UX-Team performed.

But: To run the test comparing the CTRs for all the versions does not tell us the real winner yet. It only tells us that some version(s) indeed performed better (or worse) than others. We can be sure that the best version, if statistically significant, performed better than the worst one, but we cannot be certain that the differences between the best and the second best performer e.g.

One possible approach to solve this is to narrow down the candidates: simply kick out the worst performer, and run the test again. 
We will drop candidates until we only have two candidates left to test on and then identify the winner or until the differences in performance are below the chosen significance level.  

While all the metrics will be relevant for the decision-making process, it was decided that for a version to be considered superior, a **minimum increase in click-through rate of 30%** had to be detected.   

The hypotheses to be tested in the experiment are the following:
- Null Hypothesis: all versions have the same Click Through Rate (CTR).
- Alternative Hypothesis: there is a difference in the CTR for the different versions.

The desired Statistical Significance was chosen to be 90%: it is a bit lower than the usual scientific standard of 95% because the consequences of rejecting the null hypothesis when it is true (i.e. concluding there is an effect when there is none) are not tragic, and there are constraints in the amount of time the team of experimenters have: quickness was prioritized over certainty.


# Data Set 
- The data for this case study can be downloaded on the Montana State University library webpage, [here](https://scholarworks.montana.edu/xmlui/handle/1/3507).
- It has bee prepared by Scott W. H. Young, Digital Initiatives Librarian at Montana State University.
- The folders contain data exported from Google Analytics and [crazyegg](https://www.crazyegg.com/), a service that tracks traffic to websites and provides insights and well-structured data.
- The data has been sampled from April 3, 2013 – April 10, 2013 and included 10.819 visits to the library homepage,

In the readme-file is stated the following: "Together these files may be used to reconstruct results and
to guide the design of additional A/B tests. This data is licensed CC BY-SA, http://creativecommons.org/licenses/by-sa/4.0/"


# Skills/Methods
- Prepare dataset to perform statistical testing.
- Understand how hypothesis testing can be used in the digital industry.
- Use the scipy module in Python to perform Chi-Square-Tests on the results from A/B-Testing.
- apply, understand and interpret inferential statistics.
- automate the process of using repeated statistical testing on the different tested versions using functions and loops in Python.

# Basic Steps in this Project: 
1. Load and prepare data for applying statistical test
2. Apply Chi-Square test and interpret the results
3. To find the winner between the five tested versions we repeat the whole statistical testing over and over again with each time dropping the worst candidate. 


# Files and Folders in this repository
- [Notebook for this project](../main/notebook/chi_square_test_find_winner.ipynb)
- [CSV file HP Version 1](../main/data_crazy_egg/HomepageVersion1.csv)
- [CSV file HP Version 2](../main/data_crazy_egg/HomepageVersion2.csv)
- [CSV file HP Version 3](../main/data_crazy_egg/HomepageVersion3.csv) 
- [CSV file HP Version 4](../main/data_crazy_egg/HomepageVersion4.csv)
- [CSV file HP Version 5](../main/data_crazy_egg/HomepageVersion5.csv) 
- [Folders for each Version to find also find Heatmap and Confetti pictures for visualisation](../main/data_crazy_egg)
