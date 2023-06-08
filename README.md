# Cat-pstone
### Capstone 2 for Springboard Data Science Career Track
#### Predicting Wool-Sucking Behavior in Cats

**Scenario:** My "client," a cat adoption agency, has been receiving a lot of complaints that they can't filter available cats by wool-sucking. Apparently one cat that does this went viral on ClickClack and now everyone wants one. However, our kennel managers, who complete the intake forms and behavior assessments, say it takes too many resources (namely time) to assess this trait.   

**Proposal:** Using existing, public data, develop a machine learning model to identify which cats are likely to display the target behavior.   

**Project Summary:**   

If you don't know what wool-sucking is and you have 30 seconds available, please go watch a clip on YouTube. 

Unless you hate cats, then just take a gander at a me implementing skills in data manipulation, cleaning, visualization. My raw target feature rated each feline friend on a scale of 0-7 with the following key: 
0 = Never, 1 = 1-3x/lifetime, 2 = 1-12x/yr, 3 = 1-4x/month, 4 = 1-3x/week, 5 = daily, 6 = many times/day, 7 = most of the day. 

This dataset is unique and challenging in that there is some extreme class imbalance (there are only 2 kitties/~5700 that were 7's) and that most of my features were Likert Questionnaire responses. Ordinal, and discrete data in general, produces some challenges in EDA, especially when assessing the degree of multicollinearity.
 
Because of these unique challenges, especially the class imbalance, I decided to binarize my target feature into suckers and non-suckers. I then used a Logistic Regression model with balanced class weights, as even with the binarization there was a stark contrast between class distrubtions.  

**Findings and Future Research:**   
I found that some of the most predictive features were breed, neuter status, (excessive) grooming behavior, and self- or vet-identified behavior problems.   
I will recommend that my client ensures they have someone on staff that can accurately identify breed group during intake. Additionally, I recommend they have their kennel technicians monitor and record hairball incidents with the idea being that those that excessively groom are more likely to have hairball problems. 



I would like to continue research on this to see if I can capture a bit more variability in suckers: non-suckers, mild suckers, and extreme (daily) suckers. 
I think some other models, such as a couple ensemble models, might be able to handle this unqiue dataset a bit better.  


**DATA:** 
I used [this dataset](https://figshare.com/articles/dataset/Salonen_et_al_Breed_differences_of_heritable_behaviour_traits_in_cats_-_data/8143835/1) from Salonen et al. on Breed differences of heritable behaviour traits in cats. 
