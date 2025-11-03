## Recap
OLAP  Online Analytical Processing
OLTP Online Transactional Processing

So what's key about these? Main aim of trying to design these is that it is how we have normalised, or not, the data.
OLTP is usually normalised. Reduce repetitive information, separate into other tables, but keep a core table which tends to usually be some sort of transaction. 

Analytical will have a lot more value and a lot more information sitting in there. Might be kept in a larger table with all the additional value. Might have slower querying, but it's all there, so fewer joins are needed and it's more simple. So we fall into that category and that's not a terrible thing!

So can we merge both in one data warehouse?
There are benefits to both. In some cases we might not fully normalise a table. Just a case of trying to strip out as much information as possible. Normalisation is a really broad field. Normal forms is the different stages of normalisation. 

Star and Snowflake Schemas - we know about these! Happy days.
