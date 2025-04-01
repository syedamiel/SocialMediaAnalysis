# SocialMediaAnalysis
Python notebook to analyze TikTok comments from Malaysia Airlines. The notebook is created on Google Colab

Files required:
- dataset_tiktok-profile-scraper_2025-03-27_08-56-41-895.json (Posts dataset)
- dataset_tiktok-comments-scraper_2025-03-28_01-13-55-183.json (Comments dataset)

NOTES:
The JSON datasets are obtained using Apify TikTok Actors named TikTok Profile Scraper and TikTok Comments Scraper

1. Data Cleaning and Preparation (Comments)
The code begins by importing necessary libraries: json for handling JSON data, datetime for working with timestamps, and pandas for data manipulation.

It then loads TikTok comment data from a JSON file specified by the file_path variable. The code extracts relevant information like video URL, timestamp, username, comment text, likes, and replies from each comment in the JSON data, storing them in a list called extracted_data. During this process, it also converts timestamps to a more readable format. 

To prepare for export, the extracted data is structured into a list of lists and cleaned by converting None values to empty strings. Finally, it utilizes pandas to create a DataFrame, which is essentially a table, from this cleaned data, assigns column names, and exports it to an Excel file. The file path for the output Excel file is specified, and a message confirms the successful export. In essence, the code transforms raw TikTok comment data from a JSON file into a structured and organized Excel file for further analysis.

2. Data Cleaning and Preparation (Posts/TikToks)
Th next step starts by importing the necessary libraries. Then, it defines the input and output file paths and loads the JSON data into a Python data structure. The code proceeds to clean and prepare the data by selecting specific fields (defined in required_keys) from each TikTok post, handling potentially missing data, and organizing it into a list of dictionaries.

This list is then used to create a pandas DataFrame with the desired column order. Finally, the DataFrame is saved to an Excel file, and a confirmation message is printed to the console, indicating the completion of the data cleaning and saving process. This organized data is now ready for further analysis or use in other applications.
