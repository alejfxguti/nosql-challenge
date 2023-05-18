# NoSQL Challenge - Eat Safe, Love

## Steps Taken to Complete the Challenge

### Preparation

1. Created a new repository named "nosql-challenge" for the project.
2. Cloned the repository to my local machine.
3. Added the Jupyter notebook starter files and the establishments.json file to the repository.
4. Pushed the changes to GitHub.

### Part 1: Database and Jupyter Notebook Set Up

1. Imported the establishments.json data to MongoDB using the following command: `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`
2. Imported the required libraries in the Jupyter notebook: `PyMongo` and `pprint`.
3. Created a Mongo Client instance.
4. Confirmed the creation of the database and collection:
- Used `db.getMongo().getDBNames()` to list the databases and ensured `uk_food` is listed.
- Used `db.getCollectionNames()` to list the collections and ensured `establishments` is present.
- Used `db.establishments.findOne()` to find and display one document from the `establishments` collection.
5. Assigned the `establishments` collection to a variable for further use.

### Part 2: Update the Database

1. Added information about the new restaurant, "Penang Flavours," to the database.
2. Found the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and returned only the `BusinessTypeID` and `BusinessType` fields.
3. Updated the new restaurant with the obtained `BusinessTypeID`.
4. Removed all establishments within the Dover Local Authority and verified the deletion.
5. Used `update_many` to convert latitude and longitude to decimal numbers.
6. Used `update_many` to convert `RatingValue` to integer numbers.

### Part 3: Exploratory Analysis

Explored the database by answering the following questions:

1. Identified establishments with a hygiene score of 20.
2. Identified London establishments with a `RatingValue` greater than or equal to 4.
3. Determined the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score and nearest to "Penang Flavours."
4. Calculated the number of establishments in each Local Authority area with a hygiene score of 0 and displayed the top ten Local Authority areas.
