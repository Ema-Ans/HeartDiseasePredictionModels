# Heart_Disease_Classifier
As part of the Ai for Medicine course, I created two different types of models relying on logistic regression. One uses the sigmoid function with gradient descent and  the other one uses regularized logistic regression from sklearn.


Dataset 

Worked on a dataset that consists of Cleveland, Hungary, Switzerland, and Long Beach V databases, originally with 77 features but was shrinnked to 14 after published experiments. Our dataset is labeled with a target 1 or 0, indicating a certain patient with 13 defined features has or does not have a heart disease respectively.

Features (all numeric): 

age
sex
chest pain type (4 values)
resting blood pressure
serum cholestoral in mg/dl
fasting blood sugar > 120 mg/dl
resting electrocardiographic results (values 0,1,2)
maximum heart rate achieved
exercise induced angina
oldpeak = ST depression induced by exercise relative to rest
the slope of the peak exercise ST segment
number of major vessels (0-3) colored by flourosopy
thal: 0 = normal; 1 = fixed defect; 2 = reversable defect
Target: 0 = no disease ; 1 = disease

After doing some research on the risk factors of heart diseases, I found out that three of these factors are risk factors of heart disease; age, gender, and cholesterol. In total, this dataset has 1026 entries which was good enough to train our model. However, because the dataset wasn't not very big, so I chose to allocate 80% for training and 20% for testing.


Methodology 

For the time constraint, I did research to choose the best classifier to train THE models with. I was able to find a research paper that used a very similar data set to the one we are using to predict heart disease, and they compared different classification algorithms (Kaushalya, 2021). They found out that logistic regression outperformed all the other classifiers for all the features. 

So I developed two models :

Model A: Gradient descent for logistic regression using sigmoid 
Model B: Regularized logistic regression with the help of sklearn 

Model A

Before doing any work, I created two data files. One that contains 80% of the dataset and one that contains 20% of the dataset. 

Some of the data were too big which lead to overflow when I starTed training the model, so I added some thresholds to normalize the dataset (which was not the best way to do it and i reflected on this in Model B)

I first tried to build our model from scratch using only math and numpy libraries. 

To parse the dataset, I created a two dimensional array to represent our data, in such a way that for each vector, I have all the data related to one patient.
This was done to match the parameters vector  = [0,0,0,0,0,0,0,0,0,0,0,0,0], which I first set to zeros and the learning rate α = 0.5. 
After learning, I tested our model and was ready for the conference stage. Using Tx , and sigmoid function predicting a new record to have a heart disease or not was possible as I was able to converge.  

Model B

I noticed that I had low accuracy and I thought I could fix it by regulating the data set correctly. 

To do that, I used the sklearn library to use the StandardScaler function, which standardizes features by removing the mean and scaling to unit variance. 
I also used LogisticRegression from sklearn, which implements regularized logistic regression using the ‘liblinear’ library, ‘newton-cg’, ‘sag’, ‘saga’ and ‘lbfgs’ solvers (skelearn, 2022). 

And for the data representation, I used the pandas library.

To split the dataset for training and testing, I used train_test_split which splits arrays or matrices into random train and test subsets and I was keeping 20 percent of data for testing later and the shuffling applied to data before 
splitting is 100.





 

