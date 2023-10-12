# Predict Gold Price with Long short-term memory(LSTM)
- This model uses a dataset of gold prices from the Comex market, denominated in USD / oz.

>### Input for prediction :
>- Use the imported data by using a set of data that predicts gold prices.
>- Use

```
### Select row in dataset
- Train_data: select all values, 5220 rows, with values from 2000-08-30 to 2021-06-23
- Test_data: select all values, 1885 rows, with values from 2021-06-24 to date now
```
data_size  = int(dataset.shape[0] * 0.90)
Train_data = scalar_price[:data_size - windows_size]
Test_data  = scalar_price[ data_size - windows_size :]

```

#### DataFrame in df

|date|open|high|low|close|
|----|----|----|---|-----|
|2017-10-04|	1273.800049|	1280.800049|	1270.000000	|1273.699951|
|2017-10-05|	1277.800049|	1277.800049|	1267.599976	|1269.900024|
|2017-10-06|	1267.599976|	1272.000000|	1260.500000	|1271.599976|
|2017-10-09|	1280.599976|	1284.000000|	1279.000000	|1281.800049|
|2017-10-10|	1282.599976|	1293.000000|	1281.699951	|1290.599976|
|...|	...|	...|	...|	...|
------------------------------------------------------------------

```

### The graph after the model is trained, only pulling the opening price of the gold market.
> The graph has been enlarged to make the lines more visible, but the data only goes up to October 12, 2023.
> 
#### LSTM Model

![](Graph/Graph_open(LSTM).png)







