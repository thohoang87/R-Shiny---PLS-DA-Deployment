# R-Shiny - PLS-DA package Deployment
Create R-shiny application to deploy PLS-DA package 

After creating the PLS-DA package in R (see [here](https://github.com/thohoang87/Regression-PLS-) ), we built an R-shiny application to deploy this package.

## Dataset Description

In order to test our application, we work with the dataset breast_train_test.xlsx. It consists of 400 observations and 10 variables.

The Breast Cancer (Diagnostic) DataSet, contains features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass and describe characteristics of the cell nuclei present in the image.

Attribute information:
  - 9 features : clump, ucellsize, ucellshape, mgadhesion, sepics, bnuclei, bchromatin, nomnucl and mitoses.
  - Diagnosis (classe) : malignant or benign.
  
The dataset contains 2 sheets : apprentissage (for training model) and test (for prediction).

## Application Interface:

<img width="1425" alt="Capture d’écran 2022-12-02 à 15 23 52" src="https://user-images.githubusercontent.com/114235978/205315518-4e79b4ba-9da2-47a9-a622-717cfe4bce13.png">

After opening the app, you will see the header which contains name of the app (PLS-DA Application) and the menu.

The menu includes :
  - Data view : allows to upload, view and analyse your data.
  - Define status : allows to select features (independent variables), the target and modify parameters of algorithms if necessary.
  - Fit : allows to view the training results.
  - Prediction : allows to view the prediction results of the training model or the prediction results of the file that you want to get the prediction of.
  - Graphics : allows to view some graphics of the training model.

## App functionality :

### Data view section:

If you want to upload an excel file, please choose the sheet name before uploading, then upload the file from your local machine.

<img width="1354" alt="Capture d’écran 2022-12-02 à 16 26 58" src="https://user-images.githubusercontent.com/114235978/205327599-ea8bdef0-bfbb-470c-b62c-bf7434cbf17c.png">

If you want to upload a csv file, upload the file from your local machine, then select the separator (comma, semicolon or tab) and quote (none, double quote or single quote).

<img width="1297" alt="Capture d’écran 2022-12-02 à 16 34 04" src="https://user-images.githubusercontent.com/114235978/205329352-0f52734c-d216-48c8-a818-15096d05f0ac.png">
<img width="1350" alt="Capture d’écran 2022-12-02 à 16 35 24" src="https://user-images.githubusercontent.com/114235978/205329372-47d56fa3-8e93-4039-8e86-038105ba37eb.png">

Selection of the header is automatic, if you don't want to have the header, just don't select it.

If you just want to do some analysis and you don't have the file for prediction, just forget the section of prediction's upload.

After uploading your file, click on "head" if you want to view your data, or click on "summary" to get some analysis of your data.

### Define status section:

In the "Select x variable" section, please choose features. 
And in the "Select y variable", please choose the target.
Don't forget to click on the two submit's button.

<img width="1352" alt="Capture d’écran 2022-12-02 à 16 39 56" src="https://user-images.githubusercontent.com/114235978/205331587-1a743cdd-4061-4bd5-b533-f826d9e1602d.png">

If you want to change parameters or the algorithm, just change it. If not, let it by default.
You can :
  - Choose the algorithm that you prefer (nipals or simpls);
  - If you choose the nipals algorithm, you can change the threshold and the number of iteration maximum of this algorithm;
  - Choose the threshold of VIP function;
  - Choose the number of components (if you don't choose it (it is 0 by default), the number of components will be decided by cross-validation process).

### Fit section:

In this section, you can choose if you want to see the results of training model results or the whole data model results. If you choose "train" in the "Select train of full data", your data will be splitted in train and test parts.

In the "Results of fit", you can choose:
  - Classification : allows to see the coefficients and intercept of linear model.
  - Xweights, Yweights: weights of X and Y.
  - Xscores, Yscores
  - and Xloadings, Yloadings.
 
 <img width="1346" alt="Capture d’écran 2022-12-02 à 16 48 43" src="https://user-images.githubusercontent.com/114235978/205333579-f4cc606c-2138-4ebe-ab57-06411565b9f3.png">

### Prediction Results :

There are two sub-sections in this section: 
  - Training data prediction : allows to see the prediction results of training model. In this sub-section, you can choose:
    * Class : allows to see the group of each individual.
    * Probability : allows to see the probability's result of softmax function.
    * Confusion matrix
    * Accuracy
    * Precision
    * Recall
    * and F1 score
  
  <img width="1188" alt="Capture d’écran 2022-12-02 à 17 03 27" src="https://user-images.githubusercontent.com/114235978/205334656-fdfee13f-24b6-4d67-9537-368ef5e076d0.png">
  
  - Prediction Result : allows to see the prediction results of the file that you want to get the prediction of, and you can download this result on csv or excel format.

<img width="1205" alt="Capture d’écran 2022-12-02 à 17 04 10" src="https://user-images.githubusercontent.com/114235978/205334740-7e2927e6-9a31-4293-8142-77c7452e2049.png">

### Graphics :

There are two sub-sections in this section: 
  - First selection graph : allows to see the circle correlation of features, the individual plot and the correlation matrix plot.
  
  <img width="1191" alt="Capture d’écran 2022-12-02 à 17 05 43" src="https://user-images.githubusercontent.com/114235978/205335639-aacb8e98-5926-4dc7-9f34-124eca7dbe3f.png">

  - Second selection graph : allows to see cos2 plot, contribution of features plot, screeplot and VIP plot.

<img width="1202" alt="Capture d’écran 2022-12-02 à 17 06 01" src="https://user-images.githubusercontent.com/114235978/205335679-5cb2a05f-c187-4379-9802-4d0ba1841f0c.png">
