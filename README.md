# Network_Analysis_on_Global_Offshoring_and_Tax_Avoidance_Behaviour
[Python] This project used network analytics methodologies to construct and analyse the global offshoring network contained in the Offshore Leaks papers.

### Models Deployed
Spinglass, Leading Eigenvector,

### Techniques Employed
Exploratory Data Analysis, Feature Engineering, Data Visualization, Network Analysis, Distributed Network Disruption, Community Detection

### Tools Employed
SMOTE, sklearn, TensorFlow, Keras, seaborn, plotly

### Context
Financial offshoring activity is a worldwide phenomenon. While some of these activities are done under a legal context, many have been discovered to lean towards criminal activities such as money laundering, tax evasion and fraud. The tangible costs of these activities are colossal; it is estimated that countries worldwide lose over USD$4271 billion in tax each year due to tax evasion and abuse. Multinational corporations shifted more than USD$650 billion – about 40% of their profit – worth of profit into tax havens, while private tax evaders stored more than USD$10 trillion in financial assets offshore to avoid paying taxes. The social costs are also exigent, lower-income countries’ tax losses are equivalent to nearly 52% of their combined public health budget. <br>

Many governments are now willing to cooperate to combat offshoring by imposing region-wide sanctions or residual tax payments towards tax havens. However, these policies still fall short – recovering only 0.4% of the annual offshoring costs. This project used network analytics methodologies to construct and analyse the global offshoring network contained in the Offshore Leaks papers. <br>

The Offshore Leaks papers span over 80 years and contain relationships between more than 200 countries and territories worldwide. The key objectives of this project are: (1) To discover global offshoring network structures and behaviours; (2) To explore and test the network’s resilience; and (3) To identify the top countries and financial regions.

### Datasets
The dataset was acquired from the ICIJ Panama Papers Offshore Leaks Database and contained information from all of the Offshore Leaks papers. There were 5 Offshore Leaks papers: Offshore Leaks (2013), Panama Papers (2016), Bahamas Leaks (2016), Paradise Leaks (2017) and Pandora Papers (2021). Each paper contained information on more than 100,000 entities or individuals along with their links to large intermediaries, offshore providers or law firms. The papers have a coverage of more than 200 countries. The dataset acquired combined entries from the aforementioned papers into 4 tables: Entities, Intermediaries, Officers and Relationships. To construct the network, we assigned countries to become nodes while the edges are the relationships that these countries have with each other. <br>

The final dataset contains 196 countries or independent states with 338,124 unique edges and 5 relationship types that were weighted based on importance to the network. For this study, a directed network was adopted since identifying capital inflow and outflow between countries is key to understanding offshoring behaviours.

### Chosen Model & Performance
Four classification and 1 stacked models were explored to make the prediction: Logistic Regression, Random Forest, XGBoost, Neural Network and Stacked models. The selected performance metrics were ROC-AUC score as it is immune to bias due to size of test data and F1-score as it is robust against imbalanced dataset. Model hyperparameter tuning with Bayes Search CV and Grid Search CV were done to improve performance. <br>

All models have better AUC score when compared to simple OLS, the baseline model. When over-sampling with SMOTE was applied to accommodate for imbalance dataset, all models had better F1 score except for Neural Network model. <br>

The final model which was adopted was Random Forest (with SMOTE) which gave the most balanced score between its F1 and AUC score of 0.68 and 0.917 as compared to other models.
<br>

### Results & Business Impact
Cost-benefit values were derived from the confusion matrix computed from the final model. As compared to the baseline expected revenue, which was based on average industry performance, the classification model will increase revenue by $17.74 per user. <br>

The improvement could be attained from: (a) preventing churn by introducing targeted marketing campaigns and advertisements to high value pages; and (b) from increasing purchasing conversion by improving low value or leaky webpage.

### Collaborators
Susan Koruthu <br>
Widya Salim <br>
Hpone Myat Khine <br>
Sae Jin Jang
