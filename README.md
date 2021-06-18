Introduction:

This project contains an analysis for the Venture Captalist industry on the basis of identified features.
This project is done for a Venture Fund investing in pre-IPO technology startups who have reached or are poised to reach Unicorn status.
This project can identify funds investing in venture capital secondaries in the top tier, tech-enabled companies. (Arowanaco.com, 2021).
This project appeared of the need of VC Funds to have a full analytical analysis, including predictive analytics, to validate their next investment in the Software DevOps sector. 
There we three datasets provided containing data from 2015 to 2020 years.


Specific Goals:

1.	To develop analytics around the Software-DevOps sector based on historical VC deals and Exits from 2015 to 2021.
2.	Given the target investment company's specific characteristics, build applicable predictive models for critical metrics using the datasets provided.
3.	Validate the Outcomes above in comparison or as complementary to the existing expert-driven due diligence and investment process.


Hypothesis:

According to our analysis objectives, our group has two assumptions.
First, whether the average target variable is consistent with the number of model variables this time; 
second, the factors that show a strong correlation among the variables may be Exit Size and Exit Type. 
The factors that show a weak relationship may be MOIC and %Preferred Capital Raised.


Scope of the project:

I.	A predictive model for the estimated ROI of each company.
II.	A Machine Learning algorithm to filter the possible future investments.
III.	An interactive User Interface (Dashboard) to show startups prompts in real-time.
IV.	A conclusion to summarize the outcomes from EDA.


Data & Sources:

In this project, relevant data obtained in three datasets: VC deals(transactions), VC-backed exits, and investor returns by series.
1.	The VC deals(transactions) dataset contains updated data from 2015 to 2020 in Software-DevOps companies. It has 2184 records and 55 columns.
2.	The backed exits dataset consisted of updated data of VC-backed exits of Software-DevOps companies from 2015 to 2020. It has 349 records with 20 variables.
3.	The investor returns by series dataset contain the updated data about investor returns from 2015 to 2020. This dataset has 245 rows and ten features.


•	Features Engineering


Generally, there are three types of features engineering in this project:
1.	Remove. When a feature is not related to the response or has co-linearity with other features, it may be removed from our model.
2.	Merge. When a type of value is very similar to other types, they may be merged and generate a new type. For example, in the feature “Last VC Deal Type,” the value “series A,” “series A1”, and “series A2” will be merged to “series A.”
3.	Transform. For numeric features they may be Standardized if necessary. For category features, they will be transformed into dummy variables before adding to models.


•	Model selection

We will merge the VC deals(transactions) dataset and the backed exits dataset by “Company PBID” after data cleansing to build prediction models.
The merged dataset is the training set, and the rest records in the VC deals(transactions) dataset should be the testing set.
Because of the response, MOIC, is a numeric variable, we will create several regression models to predict.
The model candidates are linear regression, polynomial regression, stepwise regression, ridge regression, lasso regression, elastic net regression, and extreme gradient boosting regression.
Before training models, we will implement the grid search process to find the best parameters for each model.


Conclusion

In this research paper an analysis of VC Fund were conducted using datasets provided. Data was cleaned and 
preformed Exploratory Data Analysis (EDA) which includes checking distribution of dataset, correlation among 
features to ensure no multicollinearity and feature selection based on intuition and correlation among features.  
Based on the initial draft, our average of the target variable lies around 9.5. At the same time, our model shows an RMSE of 10.5,
indicating the use of a more complex model and regularization of features. However, this initial exploration is limited to features present in the VC_Exits dataset.
We are still visualizing feature selection by introducing another dataset for better model prediction.



