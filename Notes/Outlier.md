# What is outlier:
- 100 mathi 5 evi sankhiya je 95 thi ek dam j alag rey jena lidhe mean par asar pade ,ane agad ni calculation ma asar pade 
- outlier ne remove karva pade jethi calculation thik thay

## How Treat outlier:
- Trimming (complatly remove)
- Capping (limit lagavi devani atle ena thi motu rey to remove )

## How to detect Outlier:
- Normal Distribution
- skewed Distribution (Boxplot)


# Example  Trimming
- get data frame
- plot boxplot and show outlier
- find IQR
```py
per25 = df['marks'].quantile(0.25)
per75 = df['marks'].quantile(0.75)
IQR = per75 - per25
```
- find upper and lower limit
```py
upper_limit = per75 + 1.5 * IQR
lower_limit = per25 - 1.5 * IQR
```
- filter the dataframe using limites 
```py
df[df['marks']>upper_limit]
```


# Example  Capping
- Dataframe
- find uper and lower limit using abov technique
- use np.where
```py
df['new']= np.where(condition,true,false)
```



