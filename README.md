# Data Preparation Process

The data preparation ensures

Here are the steps:
1. Data Exploration
2. Data Cleaning
3. Data Modelling

## 1. Data Exploration

For this project, I received 7 datasets from Social Buzz, including User, *Profile*, *Location*, *Session*, *Content*, *Reaction*, *Reaction Types*. However, only 3 datasets were used as they were relevant to the business questions: *Reaction*, *Content*, and *Reaction Types*.

#### Data Detail:
**1. Content**
- Content ID: Unique ID of the content that was uploaded. 
- User ID: Unique ID of a user that exists in the User table. 
- Content Type: A string detailing the type of content that was uploaded. 
- Category: A string detailing the category that this content is relevant to.
- URL: Link to the location where this content is stored. 

**2. Reaction** 
- Content ID: Unique ID of the content that was uploaded. 
- User ID: Unique ID of a user that exists in the User table.
- Reaction Type: A string detailing the type of reaction this user gave.
- Datetime: The date and time of this reaction. 

**3. ReactionTypes** 
- Reaction Type: A string detailing the type of reaction this user gave. 
- Sentiment: A string detailing whether this type of reaction is considered as positive, negative or neutral.
- Score: This is a number calculated by Social Buzz that quantifies how “popular” each reaction is. 

## 2. Data Cleaning:
1.	Csv to XLSX
2.	Convert text to column
3.	Find the missing values using (Find & Select – Go To Special – Blanks )
4.	Delete blanks detected rows (Delete – Table Rows) (found 980 blank rows) for reactions dataset, and others don’t have blank cells
5.	Delete useless column (Reaction UserID, Content UserID and URL, and Reaction Type no column needed for delete)
6.	Changing the data type.
7.	After Merging the 3 tables (in Data Modelling process), i use “=Proper(text) for better looking text.
Data Modelling:
Merging These 3 tables
Im using power query for merging it, content (Content Type and Category) and reaction type (Sentiment and Score) connected to reaction utilize the connection of Content ID for Content files and Reaction Type for Reaction Types files.
