# Consolidation Exercise

## Reflect on how different storage solutions - HDFS, key-value stores and Parquet can meet the diverse data storage and analysis needs within your organisation

Well, honestly, you've given me barely any information to work on to do any such reflection. But I did look up a bit of parquet myself. 
Parquet sounds interesting, though complicated, in that it can be thought of as being a columnar store rather than a row store. So a file might have 50 columns and millions of rows, but you only actually want 12 of those columns. Well to do that, right now I'd have to read the whole lot from csv into SQL and then drop what I wanted to get rid of. With Parquet, I could just read in the 12 and leave the others behind. Clearly it's complicated, our SQL right now isn't set up for that. Parquet has been mentioned with apache spark, so potentially that's the only way to actually interact with a parquet file, wehreas obviousy a csv is just universally accessible. You're not going to be able to open a parquet file in Excel for example. It's all chunked up, so needs lots of metadata.

## Consider the impact of these technologies on adata accessibility, analytics capabilities and overall strategic objectives.

Well there's definitely trouble caused when data gets too big and bloated to easily share, get to where it's going, when it takes so long that your daily reporting can't complete in a day you've got a problem! So anything that allows that to be slicker is obviously a good thing. I also know from that other training I did that what Hadoop is really good at, because it takes copies of itself I guess, is the constant streaming thing, it replicates and works on eaxctly what it has, so there's no issues about overlap or confusing stuff. So rather than daily batch you can have live data, which would obviously be good.

## Identify a specific data challenge in your organisation and propose a storage solution that addresses this challenege, outlining the benefits and any potential limitations.

Well we have our data in silos all over the place and we want to centralise it with GCP, so that's the challenge and the benefits.
