## Machine-Learning - Exoplanet Exploration

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

Use Jupyter Notebook, Pandas, Matplotlib, and Scikit-Learn to create machine learning models capable of classifying candidate exoplanets from the raw dataset.

#### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

#### Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

## Analysis

### Model-1 SVM

* Didn't need to remove any columns initially from the data set as all appeared to be relevant. Had to remove the`koi_disposition` column for the X scaler
 

* Next step was assigning X and y values for the model to perform split data to get train and test data for the model. 

* Scaled and normalised the data to create more accurate model that has less gap between data points so they all have acurate weights for the model. Initially, used MinMaxScaler on the data with `SVM` model. The train and test scores were around `0.85`. Changed to StandardScaler to scale the improved results for both scores: `Training Data Score: 0.8922372687392714`, `Testing Data Score: 0.0.8884439359267735`. 

* Using GridSearchCV to tune the model's parameters and changing the grid parameters `C` and `gamma` didn't get any score improvement. 

### Model-2 Logistic Regression

* For this model, data cleaning and preprocessing steps were the same as SVM model.

* Using StandardScaler resulted better scores again as they were better than than MinMax

* The scores for training and testing data were: `Training Data Score: 0.887659736791913`, `Testing Data Score: 0.8895881006864989`.

* Using GridSearchCV to tune the model's parameters, and changing `C` values, and increasing the number of iterations `max_iter` didn't improve scores sufficiently. 

The two models `SVM` and `LogisticRegression` didn't have any significant difference between them for this data, even hyperparameters tuning didn't help the differentiate the models.
We can say `SVM model` performs marginally better but the the models are so close that they are essentially as effective as each other.