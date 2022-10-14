# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Samy Mohsen

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
actually I didn't face any problems with my first submission. Checked the output for negative values in order to change it to 0 ,but there were not any negative values. but I included the replacment code to ensure that the script can handle this in future runs.

### What was the top ranked model that performed?
WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
First the datetime column was object not datetime format , the columns season and weather was int but in facts they are int represents a catagory. so I changed the type for datetime column to datetime and for the seasons and weather to catagory. lastley I checked for any NAN values and there was none.

About the new feature ,I wanted to make something diffrent from the suggestion was included in the templete( separate out the datetime into hour, day, or month parts.) so I made a new featur "weekday" that represenst the day of the week by index (monday= 0 , satrday = 6) using the method dt.dayofweek from the datetime column. after that I changed the column from int to catagory (they are int represents catagories)
combnations
### How much better did your model preform after adding additional features and why do you think that is?
My model preformed better in fact not that much but still there was a change , and I think that because I helped the model first to use new feature to the predict, second I helped him to understand that season, weather features are catagories.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Overall there are better resultes after trying different HPO ,but the perfomance was not that smooth. plus the leaderboard model was limited.

Update :

-The HPO model with the last chosen Hyperparameters was slightly better than others but less than the first HPO model I used hyperparameter_tune_kwargs in it , but the leaderboard was much bigger.(and that means there are a lot of combination can be used and any changes will delivers diffrent results)

-The preformance still the same less smooth than others with the default Parameters.

### If you were given more time with this dataset, where do you think you would spend more time?
First spend more time on the data try to add more useful features like seprate the datetime column to add new features or add another featue as peak hour maybe. over all spend more time on EDA process. 
Second spend more time on HPO because there was many options and many combination need to try.
I think with both of these points the model will perform better and gives more accurate target values.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

model         Time_limit   num_bag_folds  num_stack_levels     score
initial             600         0                0            1.81195
add_features        600         0                0            1.78926
hpo                 720         5                2            1.74548

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](/nd009t-c1-intro-to-ml-project-starter/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](/nd009t-c1-intro-to-ml-project-starter/model_test_score.png)

## Summary
1- EDA is really important and it's the core of MLE.
2- adding more usful features can impact the quialty and accuracy of my model. 
3- HPO is really matter , many options with the best combination will get great results and great performance.

It was such an exprince to do myself all this work , I think I could do better was more learning and training , but it was a great opportunity to explore kaggle , get data , analyze it , creat models , change prametares to get better results and working on AWS platform. sure I learned and ready to keep more learning because it's really intersting for me.
