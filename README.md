<h1 align="center"> Appliance Energy Prediction- ML Regression Approach </h1>
<h3 align="center"> AlmaBetter Verfied Project - <a href="https://www.almabetter.com/"> AlmaBetter </a> </h5>

<p align="center"> 
	
![image](https://user-images.githubusercontent.com/114068950/212836653-3d003162-ea5b-496b-8187-b2491fb3209b.png)
</p>


<p> Experimental data used to create regression models of appliances energy use in a low energy building</p>

<h2> :floppy_disk: Project Files Description</h2>

<p>This Project includes 1 colab notebook, 1 CSV file as well as 1 presentation pdf</p>
<h4>Executable Files:</h4>
<ul>
  <li><b>Appliance_energy_prediction_Regression_final.ipynb
.ipynb</b> - Includes all functions required for clustering operations.</li>
</ul>

<h4>Input Files:</h4>
<ul>
  <li><b>data_application_energy.csv</b> - Input dataset having information about dependant and independant factors causing energy consumption</li>
</ul>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book:Introduction</h2>
As the energy crisis increasing day by day causes various factors to think for in todays scenario. It not only affecting the world energy requirement issues but also affects the economic and social health of any country, mostly in the countries which are going through developing phase. To overcome several related issues, it is necessary to have the outages in order to compensate the load demand. And hence the prediction of energy used by appliances plays a vital role in the study.
	This project illustrates the energy consumed by house and the data has been collected with the help of sensors. The readings have been taken for each 10 min interval for consecutive 4.5 months. Saving of energy can be done by controlling the energy usage. And thus, prediction of usage comes into picture. This study can save the money of consumer as well as if extra energy is generated then it can also fed back to Grid(Also called as regeneration). The project mainly concentrates over the study with the help of machine learning regression technique to find out the energy consumption prediction.



<h2> :book: Problem Statement</h2>
We have to predict Appliance energy consumption for a house based on factors like temperature, humidity & pressure . In order to achieve this, we need to develop a supervised learning model using regression algorithms. Regression algorithms are used as data consist of continuous features and there are no identification of appliances in dataset.

* Which algorithm is giving best R2 score and least RMSE?

* Is there any improvement in score after using hyperparameter tuning?

<h2> :book: Data Summery</h2>
The dataset collected contain various information regarding features by which energy is being used. The features incorporated by temperature, humidity, wind speed, pressure, etc. Our main target is to analyze the data and predict the energy consumed by the house using the given dataset. For the same, we need to develop a supervised machine learning model based on regression approach.  Illustration of the some major feature contained is given below:

*	date: time: given date time month and day
*	lights : energy used by lights in Wh
*	T1 : Temperature given in kitchen area, in Celsius
*	T2 : Temperature given in living room area, in Celsius
*	T3 : Temperature mentioned in laundry room area
*	T4 : Temperature of office room, given in Celsius
*	T5 : Temperature recorded in  bathroom area, in Celsius
*	T6 : Temperature given outside the building area particularly (north side), in Celsius
*	T7 : Temperature provided in ironing room, in Celsius
*	T8 : Temperature in teenager room 2, in Celsius
*	T9 : Temperature in parents’ room, in Celsius
*	T_out : Outside temperature (from Chievres weather station), in °C
*	Tdewpoint : (from Chievres weather station), 
*	RH_1 : Kitchen area Humidity %
*	RH_2 : Living room area Humidity, in %
*	RH_3 : Laundry room area Humidity, in %
*	RH_4 : Office room Humidity, in %
*	RH_5 : Bathroom area Humidity, in %
*	RH_6 :Outside the building Humidity (north side), in %
*	RH_7 : Ironing room Humidity, in %
*	RH_8 : Teenager room 2  Humidity, in %
*	RH_9 : Parents’ room Humidity, in %
*	RH_out :Outside Humidity (from Chievres weather station), in %
*	Pressure : (from Chievres weather station), in mm Hg
*	Wind speed: (from Chievres weather station), in m/s
*	Visibility :(from Chievres weather station), in km
*	Rv1 :Random variable 1, non-dimensional[1]
*	Rv2 :Random variable 2, non-dimensional[1]
*	Appliances : Total energy used by appliances, in Wh[1]


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


# :book:Training Process:

We have used following 5 regression techniques to train the data:

**1] LASSO Regression:**
It is the regression which uses the shrinkage technique. Which means data values will be shrunk towards the central point. The Lasso regression is very useful when data parameters are few. The acronym “LASSO” stands for Least Absolute Shrinkage and Selection Operator.
Lasso solutions are quadratic programming problems, which are best solved with software (like Matlab). 

**2] RIDGE Regression:**
This regression method is mainly used when data having multi-collinearity. The method performs L2 regularization . Whenever multi-collnearity problem occurs, least-square are unbiased and variance are large. Because of it predicted value being far away from the actual values.


**3] Random Forest:**
Random Forest Regression method is a supervised learning algorithm which uses ensemble learning method for regression technique. Ensemble learning method is nothing but a technique which combines predictions from various machine learning algorithms to prepare a more accurate prediction as compare to the single model.

**4] Gradient Boosting Classifier:**
This regression technique calculates the difference between the current predicted value and well known correct target value. This residual is then added to the existing model and this pushes the model towards correct values. To improve the performance of the model we can repeat the process again and again.

**5] ExtraTree-regressor:**
It is a type of ensemble learning technique of regression that adds the results of different de-correlated decision trees which are similar to Random Forest Classifier. Extra Tree can also achieve a good or better prediction than the random forest.


# :book:Steps involved:
The full code for this article can be found here. It is implemented in Python and uses various clustering algorithms. Below is a short description of the general approach I used:

**1] Data Cleansing and Preprocessing:**
It checks whether our data contains any missing value is there or not, then it will replace it with the zero. There are no such columns present in the database and hence no need of this operation.


**2] Exploratory data analysis:**
Here, we wish to gain important statistical insights from our data and analyze the distribution of various attributes, correlations between attributes and target variables, and important quotas and proportions of categorical attributes.

**3] Train and testing procedure pipeline:**
Following methodology has been followed to train and test the model.

* Storing of all the algorithm’s present in a list and then  Iterate over the list

* The regressor’s random_state was initialized.

* The regressor was design to fit on the test as well as training data

* The properties of the regressor , Name, timining and score for training and testing set will be stored in a dictionary variable as key-value pairs.

# :book: Result

![image](https://user-images.githubusercontent.com/114068681/214804970-64871899-f6ee-48d7-b1a5-12e8695a054d.png)


* Best results for test set is being given by extra tree regressor with R2 score 0.5992 and least RMSE is also given by extra tree regressor that is 0.6127

* Using hyperparameter tuning R2 score is improved from 0.5992 to 0.60 and RMSE is reduced from 0.6127 to 0.60


# :book: Conclusion

The top 3 important features are humidity attributes, which leads to the conclusion that humidity affects power consumption more than temperature. Windspeed is least important as the speed of wind doesn’t affect power consumption inside the house. So controlling humidity inside the house may lead to energy savings.
