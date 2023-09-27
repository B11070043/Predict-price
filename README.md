# Predict Gold Price with Linear Regression and Long short-term memory(LSTM)
- This model uses a dataset of gold prices from the Comex market, denominated in USD / oz.

>### Input for prediction :
>- Use the imported data by using a set of data that predicts gold prices.
>- Use

### Import the model file in the folder called "Model".
```
load_model = tf.keras.models.load_model("./Model/model.h5")
```
### Select row in dataset
- df1: select all values, 1885 rows, with values from 2010-08-30 to 2018-02-28
- df2: select all values, 1885 rows, with values from 2017-10-04 to 2023-09-21
```
df1 = df[2500:-1400]
df2 = df[-1500:]
```

#### DataFrame in df2

|date|open|high|low|close|
|----|----|----|---|-----|
|2017-10-04|	1273.800049|	1280.800049|	1270.000000	|1273.699951|
|2017-10-05|	1277.800049|	1277.800049|	1267.599976	|1269.900024|
|2017-10-06|	1267.599976|	1272.000000|	1260.500000	|1271.599976|
|2017-10-09|	1280.599976|	1284.000000|	1279.000000	|1281.800049|
|2017-10-10|	1282.599976|	1293.000000|	1281.699951	|1290.599976|
|...|	...|	...|	...|	...|
------------------------------------------------------------------


### Predict data
> Use df2 to make predictions to find the trend of gold prices.
```
predictions = load_model.predict(df2)
```
### The graph after the model is trained, only pulling the opening price of the gold market.
> The graph has been enlarged to make the lines more visible, but the data only goes up to September 21, 2023.

![](/Graph/Graph_open_zoom.png)







