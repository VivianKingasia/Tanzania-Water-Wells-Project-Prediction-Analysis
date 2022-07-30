
# Tanzania Water Wells Project Prediction Analysis

A study by World Bank Group in 2019 showed that 29% of all waterpoints in Tanzania are non functional with 20% of them failing in the first year of installation and 40% failing within 20 years(long-term). This is a major problem for NGOs who invest funds in addressing the clean water crisis in this country.

Ensuring access to clean water and functionality of waterpoints are therefore objectives of many NGOs as a form of intervention to address this public health crisis and development challenge. NGOs tasked with contributing towards the Sustainable Development Goals in relation to the water crisis need to understand the physical infrastructure conditions of these water sources, why they fail in order to develop better interventions needed to sustainably address this water crisis. NGOs also need to understand where to direct funds either towards maintaining existing functional water systems and types of technologies to invest in to ensure continued access to clean water.

NGOs are our main stakeholders in this predictive analysis. There are some aspects that need to be explored and answered through this project analysis. Through machine learning predictive analysis with data collected by the Tanzanian Ministry of Water and Taarifa(technological company), we will able to predict which water pumps are functional and which are not to determine which need to be maintained or repaired. We will also explore the cost of water consumption for the people of Tanzania (do people pay to access water or not), whether management schemes, waterpoint technology and aspects such as population affect conditions of the waterpoint. This information will inform the role that NGOs as well as what kind of support they need from other stakeholders such as the Tanzanian Government, local communities and private firms to close the gap in water access and help Tanzania meet its 2030 SDG goal of providing universal clean and safe water.

In this classification problem, recall is extremely important. This is because, NGOs; the stakeholders are keen on identifying non_functional waterpoints to have them quickly repaired to ensure that people continue to access water. Even if precision is low, and some wells are identified as non_function when they are functional, it will still save people from catching diseases from poor sanitation and from starvation and low development.

This binary classification analysis is a Moringa school phase 3 summative assessment project that needs to be completed in the span of 7days.

## Authors

- [@Vivian Kingasia](https://www.github.com/VivianKingasia)


## Objectives

1. To be able to predict which water pump systems are functional.
2. To determine what features can be improved to ensure high functionality or better conditions of water pumps.
## Questions to be addressed

1. Can we predict which water systems are functional and which are not with a high recall score?
2. Does the type of scheme management determine the condition of the waterpoint?
3. Does the type of waterpoint technology determine the condition of the waterpoint?
## Model

Business understanding – Determined business objectives

Data understanding – Data was derived from TAARIFA website as posted for a competition. 

Data preparation – Data was cleaned, missing values and duplicates
address. OHE and scaling were also applied before modelling.

Modeling – We used four algorithms in this analysis.

Baseline logistic model as well as a tuned model using different
parameters through a pipeline and gridsearch CV.

Baseline decision tree model as well as a tuned model using different
parameters through a pipeline and gridsearch CV.

Baseline Random Forest model as well as a tuned model using different
parameters through a pipeline and gridsearch CV.

Baseline XGBoost model as well as a tuned model using different
parameters through a pipeline and gridsearch CV.

Evaluation – Several metrics were used to meet the objectives.
We used log loss to ensure a high predictive ability, recall score
as our objective was that our model to be output sensitive and auc curve.
## Data Understanding
Our data for this analysis comes from TAARIFA (a technological data company) and the Tanzanian Ministry of Water and is in the CSV format. The data mainly came from Taarifa waterpoints dashboard. The tech company aggregates data from the Tanzania Ministry of Water and the combined dataset has 59400 rows and 42 columns.

Four CSV files have been provided. One titled(Training set values) contains training set values with data on the independent features for the training set. The training set labels file (Training set labels) contains data on the dependent variable. The test set values (Test set values) contains values that will be used for prediction. A submission format (Submission format) has also been provided as this was a data science competition and the results of the analysis need to be in a specific format.

The dependent or target variable which is known as status_group is a categorical variable with three categories;

Functional-which means that the waterpoint is functional and does not needrepairs.

Functional needs repairs-the waterpoint is operational, but needs repairs

Non functional - the waterpoint is not operational

This ternary analysis will be convered to a binary analysis by combining the functional need repairs category and the non functional category to represent poor condition and functional to represent waterpoints in good condition.

There are 40 independent features in this dataset.
## Conclusion

Tanzania faces a huge challenge of water crisis exercabeted by high failure rates of the waterpoints.
The analysis was able to predict test data with an accuracy of 0.73, a precision of 0.7 and recall of 0.89. The accuracy of 73% tells us that our model will assign the correct label; functional as 1 or non functional as 0 73% of the time.Our recall of 89% means that our model is able to identify 89% of the true positives 73% of the time. The recall is the true positive rate.


This analysis did not support literature that scheme management affects failure rates of waterpoints.
However, it showed that type of waterpoint technology, type of extraction and amount paid for water affects the failure rates of these waterpoint types. The results therefore show that NGOs should focus on investing in communal standpipes, extraction types and analyzing water quantity in order to ensure reduction of failure rates of waterpoints. Most of these features highlight the 'other' type which means that more information needs to be collected to explore which other types of extraction_type and waterpoint type technologies that would help reduce failure rates.
## Recommendations

It is evident that effective interventions are needed to address the challenges of water shortages in Tanzania. The model provided can be used to predict data points and determine whether they are functional or not with a recall of 89%. 
This predictive analysis showed that NGOs need to pay more attention to waterpoint technologies, the payment
made by population to access water, the extraction type and quantity of water that population access.
Factors such as quantity, extraction type and water point technologies can be modified by NGOs. NGOs should 
invest in better water pump technologies, address payment which can also equate populations that access these water points
and also quantity of water. This analysis was converted to a binary classification and hence there is a level 
of predictive error when it comes to distinguishing between pumps that are functional that need repair and those 
that are completely non_functional. Furthermore, the high rate of false positives would need to be reduced 
so that we can better improve predicting non_functional pumps as non_functional.
