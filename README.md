# Data Preparation Processes for Social Buzz: Social Media Content Analytics

To ensure the raw data was clean, organized, and ready for analysis, I used Microsoft Excel and followed a systematic data preparation process with three main steps:

1. [Data Exploration](#data-exploration)
2. [Data Cleaning](#data-cleaning)
3. [Data Modelling](#data-modelling)


## Data Exploration

For this project, I received 7 datasets from Social Buzz: User, Profile, Location, Session, Content, Reaction, and Reaction Types. However, only 3 datasets were relevant to the business questions and were used for analysis: *Reaction*, *Content*, and *Reaction Types*.

### Dataset Details:
#### 1. Content:
- Content ID: Unique identifier for uploaded content.
- User ID: Unique identifier for users (exists in the User table).
- Content Type: Type of uploaded content. 
- Category: Category associated with the content.
- URL: Link to the content's storage location.

#### 2. Reaction: 
- Content ID: Unique identifier for uploaded content.
- User ID: Unique identifier for users (exists in the User table).
- Reaction Type: Type of user reaction.
- Datetime: Date and time of the reaction.

#### 3. Reaction Types: 
- Reaction Type: Type of user reaction.
- Sentiment: Classification of reaction as positive, negative, or neutral.
- Score: Popularity score calculated by Social Buzz.


## Data Cleaning:

To ensure the data was accurate, consistent, and reliable, I performed the following steps:

1. **Convert CSV to XLSX:** Converted raw CSV files into Excel format for easier handling.
   
2. **Text-to-Columns Conversion:** Used Excel’s "Text-to-Columns" feature to separate data fields as needed.
   
3. **Identify Missing Values:** Detected missing data using "Find & Select" → "Go To Special" → "Blanks."
   
4. **Delete Blank Rows:** Removed 980 rows with blanks in the *Reaction* dataset; no blank cells were found in the other datasets.
   
5. **Remove Unnecessary Columns:** Deleted irrelevant columns, including UserID from *Reaction* and *Content* datasets, and URL from the *Content* dataset.
    
6. **Data Type Adjustments:** Ensured all columns had appropriate data types for analysis.
    
7. **Text Formatting:** After merging the tables in the Data Modelling process, pplied the Excel formula ```=PROPER(text)``` to standardize text formatting for consistency and readability.


## Data Modelling

To structure and align the data for analysis, I prepared and merged the datasets through the following steps:

#### 1. Merging Datasets:

- Used Power Query to combine the three datasets: *Content*, *Reaction*, and *Reaction Types*.

#### 2. Key Relationships:

- The *Content* table links to the *Reaction* table via the Content ID field.
- The *Reaction Types* table links to the *Reaction* table via the Reaction Type field.

This setup creates a central *Reaction* table, with the *Content* and *Reaction Types* tables connected through their respective fields. This relational structure ensures seamless data alignment for analysis and reporting.
