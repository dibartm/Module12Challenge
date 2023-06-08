# Module12Challenge
# MongoDB Data Analysis

This repository contains the Jupyter notebook and associated files for performing data analysis on MongoDB using PyMongo and Pretty Print.

## Setup

1. Importing the Data:
    - Use the following `mongoimport` command to import the `establishments.json` file into MongoDB, ensuring that any existing `establishments` collection is dropped:

        ```
        mongoimport --db uk_food --collection establishments --drop --file establishments.json
        ```

2. Jupyter Notebook Requirements:
    - Make sure you have the `PyMongo` and `pprint` libraries installed to work with MongoDB in the Jupyter notebook environment.

3. Connection to MongoDB:
    - Ensure that you have the MongoDB server running.
    - Create an instance of the `MongoClient` in your Jupyter notebook to establish a connection with MongoDB.

## Data Analysis

### Listing Databases and Collections

- Use the following code snippet to list the available databases and collections in MongoDB:

    ```python
    # List Databases
    client = pymongo.MongoClient()
    print(client.list_database_names())

    # List Collections in uk_food Database
    db = client['uk_food']
    print(db.list_collection_names())
    ```

### Querying and Updating Data

- Use the provided code snippets in the Jupyter notebook to query and update the data in the `establishments` collection.

### Exploratory Analysis

- The Jupyter notebook includes code snippets to perform exploratory analysis on the data, answering questions such as hygiene scores, establishment ratings, and more.


