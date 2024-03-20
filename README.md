# NoSQL Challenge
This repository will be used for the Module 9 SQL challenge.

## Description

The setup to complete this project includes using MongoDB, Terminal, and Pandas. I imported the dataset in the terminal using the following code (`mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`). Then I added a new entry into the database for the restaurant Penang Flavours. I queried the database for similar restaurants and returned the BusinessTypeID. I then used the BusinessTypeID and added it to the Penang Flavours. Next, I was not interested in any establishments in Dover so I removed all entries (documents) with Dover as the LocalAuthoityName. The longitude and latitude values were stored as strings so I converted the data types to Decimal. the RatingValue field was in string formatting so I converted that to integer. That is all for the challenge setup.

For the data analysis using MongoDB, I answered the 4 questions below: 

    1. Which establishments have a hygiene score equal to 20?

    2. Which establishments in London have a RatingValue greater than or equal to 4?

    3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

    4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top           ten local authority areas.

You can review the Jupyter notebooks to find the answers to the four questions.

## Installation

Feel free to download the Python Jupyter files I provided to look over and run the Python script.

To run this project on your own, you will need to download Mongo DB.

For the setup file, you will need the following dependencies:

```python
from pymongo import MongoClient
from pprint import pprint
```

For the analysis file, you will need the following dependencies:

```python
from pymongo import MongoClient
import pandas as pd
from pprint import pprint
```

## Contributing

Pull requests are welcome. For major changes or additions to the project, please open an issue first
to discuss what you would like to change/recommend.
