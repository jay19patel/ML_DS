# Linear Regression 
```py
MX +B = Y
```
- Linear regression analysis is used to predict the value of a variable based on the value of another variable.
- Ek line banavi dey je darek data point sathe ocha ma ochi variance rakhi ne mean sodhi ne ek line banave je darek data na center mathi jay jethi next data input nu value e line na through find kari sakiye 

```py
import numpy as np
from sklearn.linear_model import LinearRegression

X = np.array([[1], [2], [3], [4], [5],[100]])
y = np.array([2, 4, 5, 4, 5,100])
lr = LinearRegression()

reg.fit(X, y)
y_pred = lr.predict([[100]])

print("Predicted output:", y_pred)
#  need 2 D array 
```
# Gradiant Descent
- Is is Optimization Algorithem 
- Most Used in Deep Learning
- Type : Bathch , Stochastic, mini batch 
- Gradiant Descent ma apnne minium number joye methemeticly rite jena mate apde darek ponint par x,y sodhi ne slop sodhi ne slop no use kari ne ena pachi no point lesu , m kari kari ne minimum number find kari sakisu 
```py
Bnew = Bold - n * Slop 
# n = learning Rate
# Bnew = New Point
# Bold = Present Point
```
- start ma mota mota step ley jem jem najik ave answer ne ,tem tem nana nana step ley and finly answer mali jay 
- if anser kudi jay to learning rate nano levano ne loop vadhare (eapoch)

## Full Gradient

```py
# ini random variable  for m and b 
m = 1 
b = 0
epoch = 100

for i in epoch:
 b = b-n*slop
 m = m-n*slop

L(m,b)
L minimum thay evu m and b na point 
```
- game em input rey pan into the end right anser apse using Gredian Descent

# Logistic Regression 
```py
Ax + By +C = 0
```
- linearly sepratebale hova joyye 
-  Random ponit ley and random line if ranom line true hoy te pont mate to thik else te new point mujab x,y,c ne adjust kare and next ponit check kare,aam jya sudhi perfect line ni male tya sudhi loop fare and check kari ne line return kare .
- line thi evu sepate thava joyye ke banne group mate line perfectly divided reva joyye.

## Sigmoid 
- sigmodid game e value ne 0 thi 1 ni vache lave 
```py
import numpy as np
from sklearn.datasets import make_classification
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(random_state=42)
model.fit(X_train, y_train)
```
# Classification Metrics

## Accuracy 
- Actual Value ne  Alag alag Algorithem sathe compare  karvanu jethi khbara pade kaya nu accuracy ghani chhe .
```py
from sklearn.metrics import accuracy_score
accuracy_score(x,y)
```

## Confusion Matrix 
```py
from sklearn.metrics import confusion_matrix
accuracy_score(x,y)
```
## Precision
- mano ke email ave chhe clg mathi and model spam ma add kari dey to te fail kevay,atle ke kam na message spam ma ni java joyye ,nakkam na rey to chale pan kam na pan reva j joye 
- false positive < false nagitive   
- jo spam hoy pan spam ni batave to chale pan notspam  spam they jay e false 
## Recall 
-  jetla sacha chhe data te sacha predict kare 
- canser rey pan predict khotu kare to problem,atle sachu revu jarur jo hoy to 



```py
from sklearn.metrics import precision_score, recall_score, accuracy_score

true_labels = [1, 0, 1, 1, 0, 1, 0, 0, 1, 0]
predicted_labels = [1, 1, 1, 0, 0, 1, 1, 0, 1, 1]

# Compute precision, recall, and accuracy
precision = precision_score(true_labels, predicted_labels)
recall = recall_score(true_labels, predicted_labels)
accuracy = accuracy_score(true_labels, predicted_labels)
report = classification_report(true_labels, predicted_labels)
print("Precision:", precision)
print("Recall:", recall)
print("Accuracy:", accuracy)
print(report)
```

# Decision Trees
- mano ke ek dataset chhe jema student and teachers chhe ,student playstor mathi games downlod kare and teacher study metrial ,so next student ave to prediction ma game j suggest thay ,aa type na algo ne Decision Tree kevay

```py
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier(random_state=42)
```


# Random Forest
- all type  ni problem solve kari sake 
- classification / Regression
- Random Forest is base on Decision Trees

# Ensemble Learning
- All Type na Model create kari ne ek group banavani pachi prediction karsu jethi lagbhag lagbhag prediction saru thase.
- koy ek ne puche to avde ni avde nakki ni pan group ma puche to lagbhag lagbhag sacha javab malvani sambhavna vadhare 

# K - Means Clustering
 - first we need  k 
 - k means Clustering (Elbo Mthods) for find k 
 - Darek data ne cluster mani ne WCSS find karvu
 - WCSS atle  dat no ena centrodi vache no tafavat
 - Jetla vadhare cluster etli nano tafavat
 - ene graph ma visulize karsu to curve graph malse jema apde elbo find karisu
 - jya je point pase slop low thato jay te point ne K manisu

 - after k male pachi random k point ne data mani su and pasi ena najik na points ne apde ek cluster manisu
 - cluster baniya pachi apde eno centroid sodhi su and ena najik na data ne cluster ma add karisu 
 - fari di centrodi banavisu ne fari di cluster banavi ne new center find kari su
 - jya sudhi center same na rey ena past center na jetlu tya sudhi cluster ne optimize karsu 
 - in the end cluster pure pura optimize jova malse 


# KNN 
- K Nearest Neighbors
- Input point ne badha  point sathe distnace find karva nu 
- Najik na K count karva na and ena parthi Point nu prediction Thay 
- K  ne find karva Cross Validation use karvu ,and je best k fit thay te apde select karvu 
- Low speed for prediction for big dataset 
- low performance for high dimantions 

# SVM
- Support Vector Machine
- SVM means find better highper plan
- mano ke be group chhe and vache thi ek line emna seprate kare pan seprate karva 1 j line ni hoy 2-3 line pan hoy sake je  banne ne seprate kari sake
- svm best line find kare ke je ek dam perfect data ne seprate karse 
- mano ke be grpup of data present chhe round shape ma inner round group 1 and outer group 2 , how can i classify them -> use multidimantion svm 
- g1 and g2 ne alag dimantion ma muki ne classifiy karvu 

# Naive Bayes Classifier
```py
P(A|B)= P(A∩B)|P(B) # Mutually Exlusive (Sathe Exist ni kare )
P(A∩B)= P(A) * P(B) # Independent Events 
```

## Bayes Thorem
```py
P(A|B)= P(B|A)P(A)|P(B) 
P(B)  != 0
```

































