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

|Fruit|Amount|
|-|-|
|Apple|10|
|Banana|15|
|Orange|8|
|Grapes|12|
|dtype:|int64|

Series dictates the order, index needs to match it. I mean, they just need to match eachother don't they really.

Pandas is cool, it can read things in different formats.

csv

```
df_csv = pd.read_csv('data.csv')

print(df_csv.head())
```

And basically you can swap the above for excel or json too.

```
import pandas as pd
import sqlite3

# Connect to the SQL database
conn = sqlite3.connect('database.db')

# Reading data from a SQL table
query = 'Select * from table name'
df_sql = pd.read_Sql(query, conn)

#Display the dataFrame
print(df_sql.head())

```

head() and tail() let us define how many of the first or rows to display. I think you can put a number in the brackets to dictate how many reuslts to return. Can be used without though, so it'll just return...not sure what without a number, so it's just the first few.

### Understanding the Structure of Data

The describe() method generates statistical summaries of the DataFrame.

This method provides measures like mean, median, standard deviation, and quartiles for numerical columns.

#Generate statistical summary using describe()
print(df.describe())

You get back:
- count
- mean
- standard deviation
- minimum
- 25 %
- 50 %
- 75 %
- max

  I can't remember the statistics anymore but it's like from the mean is it?

  Data filtering

  import pandas as pd

  #Sample dataframe
  data = {
    'Name': [john alice bob emily david],
    'Age': [25, 28, 22, 24, 27],
    'City': ['New York', 'San Fransisco', 'Chicago', 'Los Angeles', 'Seattle']
}
  df = pd.DataFrame(data)

  filtered_Date = df[df['Age'] > 24]
  print(filtered_data)

  Result

  John
  Alice
  David

  ## Sorting
  sort_values()

  sorted_Date = df.sort_values(by='Age', ascending=False)
  print(sorted_data)

  So with the above you get descending, by default it is ascending.

  df.query('age > 30 and city == "London"')

  Let's us query and filter the rows. Can also slice with .loc and .iloc . loc references column name, iloc references position.
df.loc[df['age'] > 30, ['name', 'city']] # filtering rows based on where age greater than 30, then only returning name and city.
df.iloc[0:10] # Returns first 10 rows, could put a comma and specify column by number position (o indexed)

Some RegEx things, string expressions!

.str.contains()
.str.startswith()/ .str.endswith()

### Basic Data Transformations

pandas supports various data transformation operations, such as adding or removing columns, renaming columns and converting data types.

### Data wrangling

Crucial aspect of data anlysis that involves cleaning, transforming and preparing data to make it suitable for analysis.

data = {'Name': ['John','Mary', np.nan, 'Lee'],
  'Age': [25, 30, np.nan, 28]}

and it's gone. Sorry lost that bit.

Can use duplicated() to get rid of duplicates.

RegEx

1. Characters: Literal characters (e.g., ‘a’, ‘1’, ‘$’).
2. Metacharacters: Special symbols with specific meanings (e.g., ‘.’, ‘*’, ‘?’).
3. Quantifiers: Specify repetition (e.g., ‘+’, ‘{3}’, ‘*’).
4. Character Classes: Sets of characters (e.g., [a-zA-Z], \d).
5. Anchors: Indicate position (e.g., ^, $).

. (dot): Matches any single character.
* (asterisk): Matches zero or more of the preceding element.
+ (plus sign): Matches one or more of the preceding element.
? (question mark): Makes the preceding symbol optional.
^ (caret): Indicates the start of a line.
$ (dollar sign): Indicates the end of a line.
Character classes (e.g., [a-zA-Z], \d): Define sets of characters.
Metacharacters (e.g., \, |, (), {}): Have special meanings in regex.

| Symbol |Meaning|
|-------|------|
|^|Start of input|
|$| End of Input|
|[A-za-z0-9]| range of characters|
|\s| whitespace|
|\w| word characters|
|\. |. (dot) character|
|. |any single character|
|\D |a single NON-digit|
|\S |NON-whitespace|
|\W |NON-word characters|

| Symbol |Meaning|
|-------|------|
|+ |One or more|
|{5} |Exactly five|
|{5,} |at least five|
|? |One or none|
|{2,5} |two to five|
|{,5} |up to five|

[A-Za-z]{2}\d{3}

So eg CS229 would be valid here.
