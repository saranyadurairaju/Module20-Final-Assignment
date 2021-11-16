# Agriculture and ForestLand Emission Analysis with Machine Learning

Earth's greenhouse gases trap heat in the atmosphere and warm the planet. The main gases responsible for the greenhouse effect include carbon dioxide(CO2), methane(CH4), and nitrous oxide(N20). At every stage, food provisioning releases greenhouse gases into the atmosphere. Farming in particular releases significant amounts of methane and nitrous oxide, two powerful greenhouse gases. 

![image](https://user-images.githubusercontent.com/85472349/141949794-cdd0c9bb-6307-4755-847a-ccf10a1d792a.png)

![image](https://user-images.githubusercontent.com/85472349/141952107-d5ba2298-353d-4891-b450-1bb24418778a.png)

## Analysis

In our Machine Learning model we are going to analyze Methane (CH4) and Nitrous Oxide (N2O) emissions as it contributes more on Agriculture and Forest land emissions. Below are the list items contribute in each gas. 

![image](https://user-images.githubusercontent.com/85472349/141954151-80dd5f92-6b6c-4240-a29c-9208c55a253b.png)

As per fao.org below items are aggregated values which can be avoided in the algorithm:

**IPCC Agriculture** - Agriculture total 

**LULUCF** - Land Use total 

**AFOLU** - Sum of IPCC Agriculture and LULUCF

**Farm-gate** - Sum Drained Organic Soils and on-farm energy use

**Emissions on Agricultural land** - Sum of Farm-gate and Land Use Change 


As the Machine learning methods that predict the future Emission depends on many factors like soil temperature, air moisture, Volumetric Water Content(VWC), we are classifying the Emission values into different Zones for N2O & CH4 Elements.


### Data Preprocessing

* Categorizing Element, Item, Year, Population, Emission features

* Classifying the Target variable “Zones” into Binary Values is not possible as the data is Imbalanced. 

* Multiclass classification is the problem of classifying instances into one of three or more classes.


## Analysis using Linear Regression

In this section we are trying to analyze few most contributing items of top 3 countries and the Whole world data. This analysis will help us to figure out the action needed items for those countries. 

### **Nitrous Oxide (N2O) Emission Analysis**

![image](https://user-images.githubusercontent.com/85472349/141958779-f5e3ac87-8a74-423d-b31e-abb38ffa80e4.png)

### **Methane (CH4) Emission Analysis**

![image](https://user-images.githubusercontent.com/85472349/141960605-bc28e192-928d-474d-86c2-2bd5e5c41352.png)

### **Global Green House Gas Emission Analysis**

![image](https://user-images.githubusercontent.com/85472349/141962584-68e4989b-5cc5-4c49-9c5c-1b83b70c42d1.png)


## Logistic Regression Classifier

Logistic regression is a simple yet very effective classification algorithm. Multinomial logistic regression is an extension of logistic regression that adds native support for multi-class classification problems.

### **N2O Emission**

![image](https://user-images.githubusercontent.com/85472349/141972590-7910f206-4ec8-4efd-a30d-dcc0aba060af.png)


![image](https://user-images.githubusercontent.com/85472349/141972683-582ee37a-4eed-479d-a799-94a73f95b2c4.png)

### **CH4 EMission**

![image](https://user-images.githubusercontent.com/85472349/141972799-5806d4e4-f26e-4ab0-9850-0290d38474d3.png)


![image](https://user-images.githubusercontent.com/85472349/141972857-9476b13d-fe98-4120-af7a-61c1f75dbfb0.png)


## Random Forest Classifier

A random forest classifier works with data having discrete labels or better known as class. It reduces overfitting in decision trees and helps to improve the accuracy. It is also flexible to both classification and regression problems and works well with both categorical and continuous values.

### **N2O Emission**

![image](https://user-images.githubusercontent.com/85472349/141973186-648c63c3-ea7f-4806-a708-39f90e753b5f.png)


![image](https://user-images.githubusercontent.com/85472349/141973225-a32995b5-2b80-45b1-a449-20249458fd96.png)


### **CH4 Emission**

![image](https://user-images.githubusercontent.com/85472349/141972941-924be08a-5d5b-4954-b0da-7ebb9662763b.png)


![image](https://user-images.githubusercontent.com/85472349/141973060-4a996f30-d9c0-4931-905b-866f40a4ee06.png)


## Results

![image](https://user-images.githubusercontent.com/85472349/141973384-fcd1b24f-42be-4f14-a5db-994ff5471916.png)


## Summary

The above results show that the Logistic Regression Algorithm classifies the Emission more accurately than Random Forest Classifier. Since our data is Skewed (Stratify was used) and Imbalanced which results in more number of items in specific categories. This might be the reason that our Logistic performed better than the Random Forest. Also, Logistic regression performs better when the number of noise variables is less than or equal to the number of explanatory variables. (Noise variables - Difficult or impossible to control; Explanatory Variable - manipulated in an experiment by a researcher). So. which model performs better completely depends on our Data set. 

**Suggestions**

* Naive Bayes or Gradient Boosting can be performed to check the precision/recall
* More dependant variables can be merged to this dataset to predict the future values
* Countries with Top values in our Linear Regression should try to reduce their Zones.

**Lets dream for a world with Zone 0 (Green)!!!**