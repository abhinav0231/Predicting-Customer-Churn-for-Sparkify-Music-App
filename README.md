# Predicting-Customer-Churn-for-Sparkify-Music-App

### >  Summary

This prject is part of the Data Science Capstone Project. Any project can be chosen by the student, but here we are going to work on the project that is provided by Udacity itself. This is to Predict based on a Imaginative Company dataset(Sparkify) which is a Digital Music Streeming company, We are using the medium sized dataset that is around 231 mb in size. We are going to use Spark to Do our analysis and the main objective is to Analysis and create a Model to indentify Customers likely to Churn and leave the platform. IBM Watson Sudio will be used and within it wll use the Python3.6 with Spark environment notebook to carry out the analysis. We learn how to use Spark MLlib to build machine learning models with large datasets, far beyond what could be done with non-distributed technologies like scikit-learn. The blog post for the work done here can be found in the following medium link to the blog.
https://medium.com/@abhinav.sharma023/predicting-customer-churn-9c6a54071a99



### > Installation and Library\Tools Used

           > Pyspark
           > Spark
           > Pandas
           > Skitlearn
           > Matplotlib
           > Numpy
           
  ####    Tools-
           > Spark
           > Python
           > IBM Watson Studio

Note - If running on Python 3 Jupyter notebook, please do ! pip install spark


### > Project Workflow

           > Loading the data as Spark datafram
           > Getting the Spark session up and running 
           > Loading the dataset
           > Performing desctiptive analysis
           > Cleaning the data
           > Performing EDA
           > Performing Feature Engineering to create and extract out most informative data
           > Modeling
           > Evaluation



### > Evaluation

Accuracy and AUC Score is used as the Evaluation matrix. AUC tells you your model performance, while addressing the issue of class imbalance. Since we have high class imbalace in out data as having vatio of around 78:22, hence AUC is the best evaluation matrx as it is insensitive to this imbalance and will capture the minority ckass very well. What the AUC does, is that it notifies you that you have several wrongly classified positives FP despite the fact that you have a high accuracy because of the dominant class, and therefore it would return a low score in this case.

We created a lot of variables like that impact churn like downgrade, upgrade, addfriend, add to playlist, avg lenght etc. These all turn out to be very impactfull on the final result to predict to churn users. Most impactfull being Thumbs down given, avg of the time on the paltform, total songs. 

Tree based models captures the variace in the data best and are very good at dealing with class imbalance hence not surprisingly Gradient Boosted Tree Classifier gives us the best result with 96% of Accuracy and AUC score of  .989 before Hyperparamter Tuning.

With Cross validation for Gradiant Boosted Tree we get maxDepth=5,maxbin=20 and MaxIter=10 as best hyperparameters and we get a improvement in accuracy to 98% and AUC score as before .99.

Evaluation matrix before Hyperparamter tuning-








 


### > Acknowledgements

Credit to Udacity for a very well structured course and Student guidence. Greatly Stuctured Notebooks to assist and guide students.
