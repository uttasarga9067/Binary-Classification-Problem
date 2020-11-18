# Binary-Classification-Problem

## The Idea behind this Machine Learning Model was to build a Binary Classification Application using PySpark (Distributed Computing Python API) and MLLib Pipelines. The four Models that were built on the Bank Dataset were Logistic Regression Model, Decision Trees, Randmom Forest and Gradient Boosted Tree Algorithms.
## Gradient Boosted Tree algorithm performed best on the Data Set with around 89% Accuracy.

About the Dataset:

#### 1. Data Schema:
root
 |-- age: integer (nullable = true)
 |-- job: string (nullable = true)
 |-- marital: string (nullable = true)
 |-- education: string (nullable = true)
 |-- default: string (nullable = true)
 |-- balance: integer (nullable = true)
 |-- housing: string (nullable = true)
 |-- loan: string (nullable = true)
 |-- contact: string (nullable = true)
 |-- day: integer (nullable = true)
 |-- month: string (nullable = true)
 |-- duration: integer (nullable = true)
 |-- campaign: integer (nullable = true)
 |-- pdays: integer (nullable = true)
 |-- previous: integer (nullable = true)
 |-- poutcome: string (nullable = true)
 |-- deposit: string (nullable = true)
 
#### 2. Selecting the Numeric Columns of the Data Set:
 
![ScreenShot](https://github.com/uttasarga9067/Binary-Classification-Problem/blob/main/1.PNG)

#### 3. Correlation Matrix between the Numeric Columns: 

![ScreenShot](https://github.com/uttasarga9067/Binary-Classification-Problem/blob/main/3.png)

#### 4. Diagramatic Representation of Correlation between Independent variables:

![ScreenShot](https://github.com/uttasarga9067/Binary-Classification-Problem/blob/main/2.png)

#### 5. Preparing the Data Set for fitting in the Model.

I used process of Category Indexing, One-Hot Encoding and Vector Assembler[This helps to merge multiple Columns into Vector Column]

The follwing lines of code indexes each categorical column using the StringIndexer, then converts the indexed categories into one-hot encoded variables. 
The resulting output has the binary vectors appended to the end of each row. We use the StringIndexer again to encode our labels to label indices. 
Then, we use the VectorAssembler to combine all the feature columns into a single vector column.

![ScreenShot](https://github.com/uttasarga9067/Binary-Classification-Problem/blob/main/4.PNG)



