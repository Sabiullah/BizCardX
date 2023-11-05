# BizCardX
Extracting Business Card Data with OCR
# Project Overview
BizCardX is a user-friendly tool for extracting information from business cards. The tool uses OCR technology to recognize text on business cards and extracts the data into a SQL database after classification using regular expressions. Users can access the extracted information using a GUI built using streamlit. The BizCardX application is a simple and intuitive user interface that guides users through the process of uploading the business card image and extracting its information. The extracted information would be displayed in a clean and organized manner, and users would be able to easily add it to the database with the click of a button. Further the data stored in database can be easily Read, updated and deleted by user as per the requirement.

# Libraries/Modules used for the project!

* Pandas - (To Create a DataFrame with the scraped data)
* mysql.connector - (To store and retrieve the data)
* Streamlit - (To Create Graphical user Interface)
* EasyOCR - (To extract text from images)

# Features
+ Extracts text information from business card images using EasyOCR.
+ Utilizes OpenCV for image preprocessing, such as resizing, cropping, and enhancing.
+ Uses regular expressions (RegEx) to parse and extract specific fields like name, designation, company, contact details, etc.
+ Stores the extracted information in a MySQL database for easy retrieval and analysis.
+ Provides a user-friendly interface built with Streamlit to upload images, extract information, and view/update the database.

# Workflow
 To get started with BizCardX Data Extraction, follow the steps below:

+ Install the required libraries using the pip install command. Streamlit, mysql.connector, pandas, easyocr.
+ By using streamlit, I have created the app with three menu options namely HOME, UPLOAD & EXTRACT, MODIFY where user has the option to upload the respective Business Card whose information has to be extracted, stored, modified or deleted if needed.
+ Once user uploads a business card, the text present in the card is extracted by easyocr library.

+ The extracted text is sent to get_data() function(user defined- I have coded this function) for respective text classification as company name, card holder name, designation, mobile number, email address, website URL, area, city, state, and pin code using loops and some regular expression.

+ The classified data is displayed on screen which can be further edited by user based on requirement.

+ On Clicking Upload to Database Button the data gets stored in the MySQL Database. (Note: Provide respective host, user, password, database name in create_database, sql_table_creation and connect_database for establishing connection.)

+ Further with the help of MODIFY menu the uploaded data’s in SQL Database can be accessed for Read, Update and Delete Operations.

 
My LinkedIn video - https://www.linkedin.com/posts/sabiullah-noor-mohamed-83507386_softwaredevelopment-python-streamlit-activity-7126959359389011968-CqbX?utm_source=share&utm_medium=member_desktop
