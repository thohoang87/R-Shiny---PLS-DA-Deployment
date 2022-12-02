# R-Shiny - PLS-DA package Deployment
Create R-shiny application to deploy PLS-DA package 

After creating the PLS-DA package in R (see [here](https://github.com/thohoang87/Regression-PLS-) ), we built an R-shiny application to deploy this package.

## Dataset Description

In order to test our application, we work with the dataset breast_train_test.xlsx. It consists of 400 obervations and 10 variables.

The Breast Cancer (Diagnostic) DataSet, contains features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass and describe characteristics of the cell nuclei present in the image.

Attribute information:
  - 9 variables : clump, ucellsize, ucellshape, mgadhesion, sepics, bnuclei, bchromatin, nomnucl and mitoses.
  - Diagnosis (classe) : malignant or benign.
  
The dataset contains 2 sheets : apprentissage (for training model) and test (for prediction).

## Application Interface:
<img width="1425" alt="Capture d’écran 2022-12-02 à 15 23 52" src="https://user-images.githubusercontent.com/114235978/205315518-4e79b4ba-9da2-47a9-a622-717cfe4bce13.png">
<img width="1399" alt="Capture d’écran 2022-12-02 à 15 24 44" src="https://user-images.githubusercontent.com/114235978/205315564-d20c75fc-8c73-495b-a3df-367c742a1942.png">
