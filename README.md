# Carlifornia_House_pricing_prediction
House pricing prediction for the state of Carlifornia in the year 1994

## 1. Frame the Problem
--------------------

Quizzes:
	? Business objective
	? How does the company expect to use and benefit from the model
	? What current solution looks like if any
	? What kind of model it would be: supervised, unsupervised, reinforcement, classification, regression, online, batch, univariate, multivariate


### Pipelines
--------------
A sequence of data processing components is called a data pipeline.

Pipelines are very common in ML systems since there is a lot of data to manipulate and many data transformations to apply

Components typically run asynchronously. Each component pulls in a large amount of data, processes it, and spits out the result in another data store, and then some time later the next component in the pipeline pulls this data and spits out its own output, an so on.


## 2. Select a Performance Measure
---------------------------------
A typical performance measure for regression problem is the Root Means Square Error(RMSE)

Even though the RMSE is generally the preferred performance measure for regression tasks, in some conaxts you may prefer to use another function, such as Mean Absolute Error(also called Averaage Absolute Deviation)

Both the RMSE and MAE are ways to measure the distance between two vectors: The vector of predctios and the vector of the target values.

Various distance measures or norms, are possible:

	- Computinf the root of RMSE corresponds to he Euclidean norm.
	- Computing the sum of the absolutes (MAE) corresponds to the l1 norm, also called Manhattan norm
	- The higher the norm index, the more it focuses on large values and neglects small ones. This is why the RMSE is more sensitive to outliers than the MAE. But wheb outliers are exponentially rare (like in a bell shaped vurve), the RMSE performs very well and generally preferred.


## 3. Check the Assumptions
-------------------------------
Lastly its good to lsit and verify the assumptions that were made so far (by you or others); this can catch some serrious issues early on.


## 4. Get The Data
------------------
	- create the workspace
	- Download the data
	- Take a Quick look at the Data Struture
	- Create a Test Set

## 5. Discover and Visualize the Data to gain Insights
-----------------------------------------

	- Visualizing Geographical Data
	-Looking for Correlations
	- Experimenting with Attribute Comibinations

****************************************

# Scikit-Learn Design
---------------------
Its main design principles are:

Consistency: All objects share consistent and simple interface:
	- Estimators: any object that can estimate some parameter based on a dataset; eg imputer.
	 	the estimation itself is performed by the fit() method, and it takes only a dataet as a parameter. any other parameter needed to guide the estimation process is considered a hyperparameter( such as an imputer's startegy), and it must be set as an instance variable.

	- Transformers. Some estimators (such as imputer) can also transform a dataset; The transformation process is performed by tge transform() method with the dataset to transform as a parameter

	- Predictors: estimators capable of making predictions given a dataset: eg LinearRegression
		A predictor has a predict() method and takes a dataset of new instances and returns a dataset of correspondng predictions. It also has a score() method that measures the quality of the predictions given a test set.


### inspection

### Nonproliferation of classes

Composition: Existing building blocks are resused as much as possible

Sensible defaults: Scikit-Learn provides reasonable default values for most parameters, making it easy to create a baseline working system quickly.


****************************************



## 6. Prepare the Data for Machine Learning Algorithms
--------------------------------------

	- Data Cleaning
	- Handling text and categorial Attributes
	- Custom Transformers
	- feature Scaling
	- Transformation Pipelines


## 7. Select and Train a Model
---------------------------------------
	- Training and Evaluating on the Training Set
	- Better Evaluation Using Cross-Validation


## 8. Fine-Tune Your Model
-----------------------------------------

	- Grid Search
	- randomized Search
	- Ensemble Methods
	- Analyze the Best Models and their Errors
	- Evaluate Your system on the Test Set
