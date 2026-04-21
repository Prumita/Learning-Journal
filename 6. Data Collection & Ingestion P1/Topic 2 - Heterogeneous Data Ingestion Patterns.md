Going to really try and reenage my focus today!!
Module 6 of 12, topic 2 of 4.
Like...literally half way through? Nice!
Learned what the difference is between collection and ingestion

so, let's dive into some complexity.
Lloyds, we have dozens of different files, different times, different formats, different qualities. That's what heterogeneous means, it means the reality of the messy, coming from all over.


We had an icebreaker, chatting about what ETL would we do in our personal life.

Chatting through an example, a cataologing problem. Got a report called V3 final, that's not good naming is it.

AirBnB case study
They are huge, lots of processes, including
user interactions
booking details
property listings
employs metadata management to ensure data quality and compliance

impact
Provides personalised user experiences
optimises seach results
maintsin high data quality standards
crucial for business operations

What would be batch, what would be real time?
Gave an example of bookings with AirBnB would need to be real time so there aren't clashes.

Then chatted about what would data be of just somebody looking at a page, not clicking on it. I wasn't sure and said metadata, but realised after that wasn't really right, as it is genuinely data, not data about data.
So instead someone said customer behaviour, and yeah that's spot on.

Benefit of an ETL, what's the primary benfit? Answer:
It ensures data is cleaned and transformed before loading into the data warehouse.

### Session aim and objectives
Completion of this topic supports the following outcomes:

Oh darn, missed it. But we're going to do an AWS lab that includes Glue and what not.

She's maybe about to recap from e-learning, which I raced through a bit.

Summary of elearning:

2 main ways, batch and stream processing.
Batch processing is in bulk at scheduled intervals, while rea`l-time processing handles data as it arrives.

Designing ingestion solutions
Key parameters for designing a data ingestion solution include data formats, volumes, velocity, frequency of ingestion and security.

## Intricacies of heterogeneous data ingestion
So far, we have discussed the following aspects of data ingestion:

- Data wrangling and cleaning
- Data structuring
- Data validation

  However, there is more to heterogeneous data ingestion, and we will now discuss:
  - ETL, ELT and Reverse ETL (that's a new one on me!)
  - Data discovery and cataloguing
  - Matching data sources to the right ingestion service.
 
  So let's start with what an ETL is.
  Happy little lego picture.
  knowing the right tool for the job is really confusing.

## The magic of an ETL

Data sources, we extract from them.
Then we tranform, we can automate routine transformations and also filter out sensitive data and never store it.
Then we load it up, stored data is ready for analysis and complex queries can run more quickly.

## Now the ELT, whoop whoop.
Reflects a more modern, cloud optimised approach for data ingestion apparently.
So basucally a buzz acronym.

So we go Extract still, we always need to extract!
Then we load it up, the ingestion process can run more quickly, and we don't invest effort in guessing what people will use. So nice big dumping ground.
Then we transform.
