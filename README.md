# Práctica: Módulo Deep Learning - Bootcamp KeepCoding - BIG DATA & MACHINE LEARNING

# Deep Learning

In this practice, different ** neural networks ** are used and compared on numerical data to be able to predict the price of
Airbnb homes. Likewise, we work with ** convolutional ** neural networks for the treatment of images and finally
Numerical data and images are combined to predict the price of Airbnb homes. The code is developed in Python.

These techniques are used to solve both a regression and a classification problem.

Concepts covered in this practice:

- Python **numpy**, **pandas**, **Sklearn** and **Keras** libraries
- Division of data in train and test
- Cleaning and data processing
- Generation of new features
- Exploratory analysis of numerical variables. Statistical data, distributions
- Treatment of outliers
- Exploratory analysis of categorical variables
- Exploratory analysis of Boolean variables
- Coding of categorical variables
- Correlation analysis
- Standardization and normalization
- Modeling with neural networks using only numerical data
     - Neural networks with several dense layers
     - Neural networks with regularization of type L1 and Dropout
- Modeling with convolutional networks using only images
     - Download images from URLs
     - Construction of image dataset
     - Neural networks with several convolutional layers
     - MaxPooling2D regularization, BatchNormalization and Dropout
     - Modeling using VGG16, RestNet50 and InceptionV3 with finetunning
- Modeling with neural networks combining numerical data and images for both a regression and classification problem


## Statement

The objective of the practice is to tackle a realistic Deep Learning problem following the methodology and good practices explained during the theoretical classes.

**Task: Implement a predictive algorithm that is capable of estimating the price of Airbnb homes using data of different types and Deep Learning techniques (deep neural networks).**

First, a modeling with only numerical data will be carried out, later a modeling with convolutional networks using only images, and finally both types of data will be combined in a single predictive model. It will be solved as a regression problem and as a classification problem


## Data set

The chosen data set is [éste](https://public.opendatasoft.com/explore/dataset/airbnb-listings/export/?disjunctive.host_verifications&disjunctive.amenities&disjunctive.features&q=Madrid&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJ5QXhpcyI6Imhvc3RfbGlzdGluZ3NfY291bnQiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiJyYW5nZS1jdXN0b20ifV0sInhBeGlzIjoiY2l0eSIsIm1heHBvaW50cyI6IiIsInRpbWVzY2FsZSI6IiIsInNvcnQiOiIiLCJzZXJpZXNCcmVha2Rvd24iOiJyb29tX3R5cGUiLCJjb25maWciOnsiZGF0YXNldCI6ImFpcmJuYi1saXN0aW5ncyIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUuaG9zdF92ZXJpZmljYXRpb25zIjp0cnVlLCJkaXNqdW5jdGl2ZS5hbWVuaXRpZXMiOnRydWUsImRpc2p1bmN0aXZlLmZlYXR1cmVzIjp0cnVlfX19XSwidGltZXNjYWxlIjoiIiwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZX0%3D&location=16,41.38377,2.15774&basemap=jawg.streets), extracted from Airbnb using scraping techniques. Among the options, I recommend using extract (“Only the 14780 selected records”), since it minimizes execution time and avoids memory problems on computers with fewer features.

## Structure of the project.

**data**

*airbnb_listings.csv*: It is the original airbnb dataset, the reduced version. It is compressed as .zip as it exceeds the size allowed by Github

*airbnb_cleaned*: It is the dataset already cleaned and prepared. The result of the first 5 points of the practice and was also obtained in the Machine Learning module

*airbnb_segun_img*: This is the clean and orderly dataset according to the images we have and how they were loaded. It will be used when combining numerical data and images for the model. This file is obtained in point 8.2 of the practice

**imagenes**

They are all the images downloaded starting from the "Picture URL" field that is in the airbnb dataset. The name of each file matches the ID of the airbnb listing. The download of these images is done in point 8.1 of the practice

**datasetImagenes**

*X.pickle*: is the already prepared dataset extracted from the images, it contains a structure (1271x50x50x3)

*Y.pickle*: It is the dataset with the prices extracted from the ID of the images and looking at the airbnb dataset

These two files are obtained in point 8.2


## Developing

This practice has been developed using Google Colaboratory and the files are saved in Drive.

At the beginning of the practice a Path variable is established that contains my current path within Drive where the structure of the previous project is. You will have to change that path variable if you want to copy this structure to another Drive and run the project.
     
    
     

