# Supervised Learning
1. Regression
2. Classification 

- Student na Data chhe (iq/CGPA/Placement)
- input iq/CGPA 
- output Placement 
- next student ave to e iq and cgpa api ne joy sake ke placement thase ke ni te 
- Need To labeld data 
- if output numeric hoy to Regression (4.5,89)
- if output categorical hoy to Classification (Yes/No)

# Unsupervised Learning
1. clustering
2. Dimensinality Reduction
3. Anomoly detection
4. Assosiation Learning

- Student na data chhe (IQ/CGPA)
- input IQ/CGPA
- (Clustering): Jate j Group banave ke kona IQ vadhare chhe kona CGPA vadhare se kona CGPA osa IQ high and CGPA osa and IQ low etc 
- (Dimensionality): Remove extra columsn and kam ni j columsn use kare je dipendend rey 
- Length and width be columsn hoy to area ni navi column banavu ne l and W ne area ma convert kari ne delete kari ne area ni column use karvani .
- (Anomoly detection): alredy train data chhe pan train data ma 100 data ma ek alag ave to tene avganva ma ave 
- (Assosiation Learning) : mall ni andar baju ma kayi vastu mukvi ke jethi loko ley jemk ke , bred ni baju ma jem muksu to banne ley lese jethi sale vadhe .jo bred and jem alag alag rey to sayad  koy ne yad ni rey ne ni ley, so relationship sodhvanu 

# Semi Supervised
- Google photos 
- Supervieds ma lable karva mate bo time jay pan amma ek var lable kari diye pachi unsupervise ni madad thi train kari diye
- Google photo ek var puchse ke aa kon chhe apde name apsu to ena jeva badha phota ek sathe ley ne group banavi dey 

# Reinforcement Learning
- no lable data no any data for train
- mano ke ek robot chhe and ena pase bo choice chhe  hot ya cold 
- if robot hot baju jay to point cute thay and cold baju jay to point male so next time khabar padi jay ke hot baju java to nuksan so apde cold baju j jasu . jate j try kari ne sikhe 


# Ml Model Training Data  
1. Batch Training
- Badha ek sathe train thay annd thoda thoda time a update karva pade
2. Online Training
- autometicly new data ave tem tem jate train they jay ne updated  value return kare 


# Ml model Learning Data
1. Instance Base Learning
- No need any Pre Model Taringing
- Direct javab api dey  Training kara vagar atle ke ene machine learning karva training ni jarur ni pade koyk methemetic calculation kari ne anser appe jem ke (KNN)
- darek data depend rey output par

2. Model Base Learning
- ek var tarining kari ne border banavi dey pachi border no use kari ne j classification ke regression kari ne anser ape ,ni ke darek data ne farithi calculate kare
- ek var model create kari ne model no use kari ne anser ape  
- Ek var model banavi dey atle ke koy equeation ke kay pan pachi train data ni jarur ni pade 

# Challenes in ML
- Insufficient Data / Label data 
- Non Preresentative Data 
- poor Quality Data 
- Inrelevent Features (feture engineering atle be column ne ek ma karvu )
- Overfitting(train = 100 , test=10)
- Underfitting(train = 50, test=30)

# ML Learning Development Life Cycle 
- Frame the Problem 
- gethering Data
- Data Preprocessing
- Exploratory Data Analysis (Analysis karvu ne graph banava ne all type nu posible analysis karvu)
- Feature engineering And Selection(IMP) 
- Model Training ,Evalution and Selection (badhu model ne try karvu ne kayu best chhe te select kari ne agadi vadhvu)
- Model Deployment(Create webiste ke app ke game e jenathi user ineract kari sake ne user use kari sake apdu model)
- Testing
- Optimize 



# What is Tensors
- Tensors is a Data Structure in ml
- Tensors = n Dimantion Array 

### 1 D Tensors
```py
a = [1,2,3,4,5]
# 1 D Tensor and 5 D Vector (5 Sankhiya atle  5 D vector )
```
### 2 D Tensors

```py
a = [[1,2,3],[4,5,6]]
# 2 D Tensor and 2 D vector 
```

### 3 D Tensors
- mainly use in NLP
```py
text = "Jay Patel"
# text ne  number ma convert karva padse 
# text ne koy vector ma convert kari devano 
ex =[[[1,2,3],[1,2,3]],
     [[1,2,3],[1,2,3]],
     [[1,2,3],[1,2,3]]]
```
- time series data  are 3 d tensors 

### 4 D Tensors
- Images are 4 D tensors 
(50image,3grb,height,width)

### 5 D Tensors 
- Video is a example of a 5 D

# 1. Data Gethering 
- API
- Data Scraping
- CSV/ Excel file
- DataBase

# 2. Data Preprocessing
- profiling
- cleaning
- reduction
- transformation

# 3. Exploratory Data Analysis
## 1. Understanding Yor Data :
How Big Data = df.shape
Look our data =df.sample(5)
type of columns an info = df.info()
missing Values = df.isnull().sum()
data Staticstic = df.describe()
find Dupicate values= df.duplicated().sum()
coreelation = df.corr()['columnname'] - find relation with other columsn if relation then drop columns 

## 2. EDA (Exploratory data analysis)
	1) Univariate
	2) Bivariate
	3) Multivariate

### 1. Univariate
- the study of one variable at a time without considering its relationships with other variables
- Data have two type 1) Numeric ,2) Categorical

	1) Categorical
	- Count Plot = sns.countplot(df['survived'])
		     = df['survived'].value_count().plot(kind='bar')
	- Count nessesory columsn and visiultize those data 
	- also we use pie chart 
	
	2) Numerical Data
	- Histogram (most use) (age no hist lesu to khabar padse k ketla age vala vadhare and osa )
	- Distplot (probability find)
	- boxplot (if we have noice in our data )


### 2. Bivariate 
- the examination of the relationship between two variables.

### 3. Multivariate
he examination of relationships and interactions among multiple variables simultaneously.

	1) Categorical
	- crosstab(pclass vala jive ketla and mare ketla )
	- HeatMap
	- Use Pandas Groupby for more accuracy(most imp)

	2) Numerical Data
	- scatterplot (sns)(multiple columns use to visiulize more data in one frame )

	3) Numerical  - Categorical
	- barplot (sns)
	- Box Plot (sns)
	- Displot(sns)(jivta and marta banne na age no displot ley ne analysis kari sakay)

## 3. Pandas profiling
- Autometicly Creating Analysis by own and give a html page 
- all kind of data are present in the html page so very very helpfull this model with easy understanding


# 4. Feature engineering And Selection (IMP)
- convert row data into ml cunsume data called Feature Engineering
- ex . columsn ma unnessesory column ne delete kari ne use thay evi kam ni column ma convert karvu 

1. Feature Transformation
- Missing Values (Remove or fill missing value)
- Handlling Categorical Values (One Hot Encoding)
- Outlier Detection (100 mathi 10 data alag ave to line alag thay jethi pure puri calculation ma problem ave atle outlier ne delete karvu)
- Feature Scaling (arek na ekam ,formate same rakhvi kya to nana ma nani sankhiya ma rupantar karvu (-1 to 1 or etc ))
- use sklearn  columns transformar

2. Feature Construction 
- create new column and murge kari ne ek column banavani 
3. Feature Selection
- ghani badhi column chhe pan emathi kam ni j column use karvi 
4. Feature Extraction 
- be column ne use kari ne navi column create karvani

### Selection (IMP)
1. Standaraization 
- mano ke ek column chhe age but apane age ne standeraization karva pade 
- mean ne center ma lavi devanu atleke 0 
- Standaraization atle ene dabavu atle ke compress karvu 
- Standaraization ni kare to koy nani moti range na karane apde vesiulize ke ganatri ni kari sakiye
- Standaraization faydo e ke banne na ekam/ range nani they jay  jethi badhi column na sarkhamni ma avi jay 
- Standaraization thi outlier ma koy fer ni pade atle apde ene menualy alag rite remove karva padse 
```py
 Z-Score = (Current_value – Mean) / Standard Deviation.
```
2. Normalization
- min max scaling kari ne ekeam nana kari deva (0,1)
- mean normalization formula used

```py
Min-Max Normalization: (X – min(X)) / (max(X) – min(X))
```
# 5. Model Training ,Evalution and Selection
# 6. Model Deployment

# Pipeline 
- performing multiple operations in a sequence, for each element of an iterable, in such a way that the output of each element is the input of the next
- ek type ni chain bani jay jethi ek pasi ek badhu thaya j kare je step apde add karela hase jethi badhu easy thay and code ripit ni thay



 

