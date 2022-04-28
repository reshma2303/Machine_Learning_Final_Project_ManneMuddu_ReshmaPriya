# Machine_Learning_Final_Project_ManneMuddu_ReshmaPriya


**1. Problem: Intrusion Detection (Finding Anamolies) Analysis**

The KDD Cup 1999 dataset has been chosen for this data analysis project. This dataset was used in the fifth international conference for the data mining and knowledge discovery competition and contains a huge variety of network intrusion data that is simulated in an environment equipped with a military network setting.

KDD Cup 1999 dataset will be used to build a machine learning based intrusion detection problem to predict (classify) whether a network connection is "normal" or "abnormal". As this is a categorical prediction, this is a binary classification problem

The original source of the dataset is from the official KDD website (http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html) and can also be found in the kaggle website. The dataset contains about 494,000 records of network readings with details like source bytes, destination connection information, type of attacks and so on. Below are the list of features (columns) and their data types in the dataset.

The task description can be found here - http://kdd.ics.uci.edu/databases/kddcup99/task.html

The data dictionary can be found here - http://kdd.ics.uci.edu/databases/kddcup99/kddcup.names

**2. Findings Summary**

- From categorical columns distribution plots, the column/feature 'is_host_login' will not be useful for the prediction as all of its values are 0s.
- From the statistics of the continous variables, the column/feature 'num_outbound_cmds' will be of no use for analysis/prediction since all of its values are 0s
- There are no missing values in any column so as in whole dataset.
- There is some high correlatin found in the continous columns. Some of the correlated features can be removed inorder to avoid curse-of-dimensionality and multicollinearity problem
- Recommendation: Among all server rate columns, one server rate column will be sufficient since all of them are 100% correlated. Therefore, dst_host_serror_rate can be selected for final prediction modeling
- There is some relation (valid) between all categorical columns. Hence, these columns need not be dropped for analysis and prediction
- There are no as such very highly correlated independent variables (features) to the dependent variable. Therefoe, no subselection is required in this analysis from this perspective.

![alt text](https://github.com/reshma2303/Machine_Learning_Final_Project_ManneMuddu_ReshmaPriya/blob/master/plots/plot-1.png)

- As seen in the above, plot, the services IRC, telnet have higher mean duration times compared to other type of services
- As seen above, as duration increases the count of connection gets reduced
- As seen above the flag tupes S0, REJ, SF, RSTR have higher number of unique services being utilized for the malware connections


**3. Plan for Prediction**


