# NoSQL Challenge - Eat Safe, Love

## Before You Begin

- Create a new repository named "nosql-challenge" for this project.
- Clone the repository to your local machine.
- Add the Jupyter notebook starter files and the establishments.json file to the repository.
- Push the changes to GitHub.

## Files

Download the following files:

- [Module 12 Challenge files](#) 

## Part 1: Database and Jupyter Notebook Set Up

1. Import the establishments.json data to MongoDB using the following command: `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`
2. Import the required libraries in your Jupyter notebook: `PyMongo` and `pprint`.
3. Create a Mongo Client instance.
4. Confirm the database and collection are created properly:
- Use `db.getMongo().getDBNames()` to list the databases and ensure `uk_food` is listed.
- Use `db.getCollectionNames()` to list the collections and ensure `establishments` is present.
- Use `db.establishments.findOne()` to find and display one document from the `establishments` collection.
5. Assign the `establishments` collection to a variable for further use.

## Part 2: Update the Database

1. Add information about the new restaurant, "Penang Flavours," to the database.
2. Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.
3. Update the new restaurant with the obtained `BusinessTypeID`.
4. Remove all establishments within the Dover Local Authority and verify the deletion.
5. Use `update_many` to convert latitude and longitude to decimal numbers.
6. Use `update_many` to convert `RatingValue` to integer numbers.
## Part 3: Exploratory Analysis
Use the following questions to explore the database:

1. Which establishments have a hygiene score of 20?
2. Which London establishments have a `RatingValue` greater than or equal to 4?
3. What are the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score, nearest to "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Display the top ten Local Authority areas.

That's it! You have completed the NoSQL challenge for the UK Food Standards Agency's establishments ratings data.
