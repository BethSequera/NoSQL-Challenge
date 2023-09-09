# Eat Safe, Love - UK Food Ratings Analysis

The UK Food Standards Agency evaluates various establishments across the United Kingdom and assigns them food hygiene ratings. We've been contracted by the editors of the food magazine, Eat Safe, Love, to analyze this ratings data. The goal is to assist their journalists and food critics in deciding where to focus their future articles.

This project is divided into three main parts:

### Part 1: Database and Jupyter Notebook Setup
### Data Import
To get started, we import the provided data from the `establishments.json `file into a MongoDB database named `uk_food` with a collection named `establishments`. Below is the command used for importing the data:

`mongoimport --db uk_food --collection establishments --file establishments.json`

### Python Libraries and MongoDB Connection
In the Jupyter Notebook (`NoSQL_setup_starter.ipynb`), we import the following Python libraries:

- PyMongo
- Pretty Print (pprint)
We also create an instance of the MongoDB Client to connect to the database.

### Database Confirmation
To ensure that the database and data were set up properly, we perform the following steps:

- List the databases in MongoDB to confirm the presence of `uk_food`.
- List the collections in the `uk_food` database to ensure that `establishments` is present.
- Find and display one document from the `establishments` collection using `find_one` and display it using `pprint`.
- Assign the `establishments` collection to a variable for further use.

###  Part 2: Update the Database
In this section, we make modifications to the `establishments `collection as requested by the magazine editors. The following changes are made:

### Database Modifications
- Add information for a new halal restaurant, "Penang Flavours," to the database.
- Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and update the new restaurant's entry with this ID.
- Remove all establishments within the Dover Local Authority from the database.

### Data Type Conversion
We also address data type issues in the database:

- Use `update_many` to convert latitude and longitude to decimal numbers.
- Use `update_many `to convert RatingValue to integer numbers.

### Part 3: Exploratory Analysis
In this section, we perform an exploratory analysis of the database to answer specific questions posed by Eat Safe, Love. We use the `NoSQL_analysis_starter.ipynb` notebook for this part.

### Installation
To set up and run this project locally, follow these steps:

1.Clone the repository to your local machine.
2.Install the required Python libraries by running: `pip install -r requirements.txt`
3.Ensure you have MongoDB installed and running.
4.Follow the instructions in the Jupyter notebooks (`NoSQL_setup_starter.ipynb` and `NoSQL_analysis_starter.ipynb`) to execute the code and perform the analysis.

### Usage
Detailed usage instructions are provided in the Jupyter notebooks.

### Dependencies
PyMongo
Pretty Print (pprint)
Jupyter Notebook
Pandas

### Contributing
Feel free to contribute to this project by opening issues or submitting pull requests.

### License
This project is licensed under the MIT License - see the LICENSE file for details.
 
