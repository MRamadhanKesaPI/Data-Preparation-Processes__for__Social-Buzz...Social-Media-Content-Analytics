# Data Preparation Process for Social Buzz: Social Media Content Analytics

The data preparation process ensures raw data clean, organized, and ready for analysis. In this project, it involves three main steps:

1. [Data Exploration](#data-exploration)
2. [Data Cleaning](#data-cleaning)
3. [Data Modelling](#data-modelling)


### Data Exploration

For this project, I received 7 datasets from Social Buzz, including User, **Profile**, **Location**, **Session**, **Content**, **Reaction**, **Reaction Types**. However, only 3 datasets were used as they were relevant to the business questions: **Reaction**, **Content**, and **Reaction Types**.

#### Data Detail:
#### 1. Content:
- Content ID: Unique ID of the content that was uploaded. 
- User ID: Unique ID of a user that exists in the User table. 
- Content Type: A string detailing the type of content that was uploaded. 
- Category: A string detailing the category that this content is relevant to.
- URL: Link to the location where this content is stored. 

#### 2. Reaction: 
- Content ID: Unique ID of the content that was uploaded. 
- User ID: Unique ID of a user that exists in the User table.
- Reaction Type: A string detailing the type of reaction this user gave.
- Datetime: The date and time of this reaction. 

#### 3. Reaction Types: 
- Reaction Type: A string detailing the type of reaction this user gave. 
- Sentiment: A string detailing whether this type of reaction is considered as positive, negative or neutral.
- Score: This is a number calculated by Social Buzz that quantifies how “popular” each reaction is. 


### Data Cleaning:

In this phase, i clean the data to make sure it's accurate, consistent, and reliable. The process includes:

1. **Convert CSV to XLSX:** Begin by converting CSV files to Excel format.
   
2. **Text-to-Column Conversion:** Use Excel's text-to-column feature to separate data as needed.
   
3. **Identify Missing Values:** Use "Find & Select" → "Go To Special" → "Blanks" to identify missing data.
   
4. **Delete Blank Rows:** Remove rows with blanks in the Reactions dataset (980 rows identified and deleted). No blank cells were found in the other datasets
   
5. **Remove Unnecessary Columns:** Delete columns including UserID from the **Reactions** and **Content** datasets and URL from the **Content** dataset. No columns were deleted from the **Reaction Types** dataset.
    
6. **Data Type Changes:** Adjust columns to appropriate data types.
    
7. **Text Formatting:** After merging the tables in the Data Modelling process, apply the formula ```=PROPER(text)``` to standardize text formatting for consistency and readability.


### Data Modelling

In this phase, I prepare the data for analysis by structuring and merging the relevant datasets to ensure they are properly aligned and ready for insightful reporting. The process includes:

#### 1. Merging Datasets:

- I Utilized Power Query to merge the three datasets: **Content**, **Reactions**, and **Reaction Types**.

#### 2. Key Relationships:

- The **Content** table is linked to the **Reactions** table through the Content ID field.
- The **Reaction Types** table is linked to the **Reaction** table through the Reaction Type field.
This results in the **Reaction table** (main table) acting as the central point, with **Content** and **Reaction Types** connected via their respective fields (Content ID and Reaction Type).
