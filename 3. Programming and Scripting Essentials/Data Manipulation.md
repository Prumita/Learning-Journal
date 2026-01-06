Okay, feeling very tired here and sad and just generlaly like I could curl up in a ball! So let's see how we do.

I have stored todays downloads to here: C:\Users\fishm\OneDrive\Documents\Apprenticeship\Downloads\Module 3 topic 5 Python Pandas

So what is Pandas? it's a Python Library and it's great at data manipulation. Panda has a lot of functions that lets you do all sorts. Import, export, group, aggregate, transform, make new columns, fill in missing values etc, amazing!

Real world scenario. banking analyst wants to look at historic stock to make investment decisions.
Make sense of data they have so they can make decisions going forward. So they can try or forecast.

Pandas is an open source python library and comes with data analysis tools, pre-defined functions.

Pandas uses a DataFrame, which you can visualise like a SQL table or a spreadsheet. Data is organised in rows and columns.

```
data = {
  'Name':['Alice','John'],
'Age': [25, 30, 22, 28],
'City': ['New York','London','Paris']
}
#bit wrong above as they should have the same number ofg values but trying to keep up

df = pd.DataFrame(data)
print(Df)
 #Lovely picture here of basically a table
```

Okay so above is a DataFrame. What is a series?

it's a one-dimensional labelled array.

```
import pandas as pd

#Create a series with labelled data
fruit_series = pd.Series([10,15,8,12],index=['Apple', Banana', 'Orange', 'Grapes')

#Display the series
print(fruit_series)
```

Looks like

|Apple|10|
|Banana|15|
|Orange|8|
|Grapes|12|
|dtype:|int64|

Series dictates the order, index needs to match it. I mean, they just need to match eachother don't they really.

