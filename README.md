# Fruits Doodle Recognition
This is done by @kentai1114 , @marylfo , @meiling1020 and  @raylyh for COMP 4651(Cloud Computing and Big Data Systems) Project.

## Project description
This project builds three recognition models to classify fruits with fruit doodle images obtain from QuickDraw Dataset using Spark.

## Data
[The Quick, Draw! Dataset](https://github.com/googlecreativelab/quickdraw-dataset)  is used in this project. This dataset which is owned by Google, Inc. under the Creative Commons Attribution 4.0 International Licence. Nine fruit datasets are downloaded from [here](https://console.cloud.google.com/storage/browser/quickdraw_dataset/full/numpy_bitmap/) and stored in .npy format in folder `dataset`.

**Since the file size of fruit datasets is too big and exceed the limitation of GitHub, so they are not attached in this repository** 

`9fruitsTrainDF.csv` and `9fruitsTestDF.csv` are two processed .csv files for model training and model testing.

## Python Program
- `npy2csv.ipynb` is a program converting raw dataset from .npy files into 9fruitsTrainDF.csv and 9fruitsTestDF.csv by extracting and labelling the fruit data.

| fruit             | label |
|-------------------|-------|
| apple             | 0     |
| banana            | 1     |
| blackberry        | 2     |
| blueberry         | 3     |
| grape             | 4     |
| pear              | 5     |
| pineapple         | 6     |
| strawberry        | 7     |
| watermelon        | 8     |

- `project.ipynb` is program run on Databricks using PySpark. It implements three recognition models.
1. Multi-layer perceptron classifier
2. Random forest classifier
3. Multinomial logistic regression
