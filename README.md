# 2025 March Madness Tournament Predictor
Machine Learning project that guesses the outcome of the 2025 NCAA March Madness Tournament using past results. This was created as a side project to further my machine learning skills, focusing on predictive modeling, feature engineering and data analysis.

## Files Used
- **mm.ipynb**: Main notebook with data preprocessing, analysis and predictions
  
- **tournament_results.txt**: First text file with every round and their results, predictions created with Gradient Boosting Random Forest Classifier
  
- **tournament_results2.txt**: Second text file with every round and their results, predictions created with Gradient Boosting Classifier
  
	- These results were chosen, as the accuracy was a bit higher than the first model
   
-  **mm_predictor.py**: Python file that consolidates all of the notebook's work into a more organized, documented Python file

 **NOTE**: The notebook was used for the development of the project, and lacks full documentation and clear organization. The Python file with these changes will be added soon. 

 ## Data
 Data used was historical NCAA March Madness data since 2008 taken from https://www.kaggle.com/datasets/nishaanamin/march-madness-data/data
 
 - **KenPom Barttorvik.csv**: Combination of KenPom and Torvik ratings. Also has many basic stats such as 3P%, TOV%, etc.
   
 - **Resumes.csv**: Seed, Resume ranking, Wins above Bubble, and ELO ranking
   
 - **Tournament Matchups.csv**: Every past matchup in the tournaments since 2008 and round of 64 matchups for 2025
   
 - **Seed Results.csv**: Each seed and their past total win rate, and total wins per round

## Models
There were two models used: Gradient Boosting Random Forest Classifier (xgboost) and scikit learn's Gradient Boosting Classifier. As inspiration from https://github.com/uclaacmai/Machine-Learning-for-March-Madness/blob/master, these models resulted in the two highest accuracy scores.
After tuning countless features, the final features chosen to train these models were:

**'Diff_AdjO', 'Diff_AdjD', 'Diff_TOV%_T1', 'Diff_TOV%_T2','Diff_Exp', 'Upset_Rate', #'Diff_Adj_T1', 'Diff_Adj_T2','Diff_Tempo', 'Diff_EFG%', 'Diff_OREB%', 'Diff_Bal', 'Diff_ELO','Team1_Seed', 'Team2_Seed', 'Is_Giant_Killer','Team1_juggernaut', 'Team2_juggernaut', 'Diff_Trap'**

The features are described deeper in the code.

## Results
The Gradient Boosting Random Forest Classifier achieved .7833 accuracy and .5288 log-loss, while the Gradient Boosting Classifier achieved .7667 accuracy with .518 log-loss.
The baseline for March Madness predictors fall around .76 accuracy and .5 log loss.

## Future
Detailed results for the 2025 predictions can be found [here](mm_report.md).

In the future some possible extensions would be to engineer even better data using more advanced metrics, or even using different predictive models, such as ratings on evanmiya.com, the heatcheckcbb.com Tournament Index, and much more. Also, creating further prediction visuals such as a full bracket instead of a .txt file would increase overall visibility and ease of use for users.

## LICENSE
Distributed under the Unlicense License. See [License](LICENSE.txt) for more information.

## Contact
Matthew Evitts | [LinkedIn](https://www.linkedin.com/in/matthew-evitts/) | [email](martevitts@gmail.com)


[Project Link](https://github.com/mevitts/March_Madness)

