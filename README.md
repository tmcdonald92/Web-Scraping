# Web Scraping Darty Website

![logo](https://upload.wikimedia.org/wikipedia/commons/b/b0/Darty.svg)

## Objective

This project focuses on Web Scraping and Data Cleaning.
The website chosen for this project was Darty, more specifically the category of washing machines.
The purpose was to use the library **BeautifulSoup** to extract the information required, clean the data and export it to a MySQL table.
Each stage was condensed in a function that was later included in a pipeline to make the code easier to read and to run.

## Tools and Libraries used

* Requests
* BeautifulSoup
* Pandas
* datetime

## Process

The project is divided into **3 main stages**:
  * Extraction/Scraping of the data from the website;
  * Data Cleaning
  * Exporting the data to MySQL
  
### Extraction of the data

To extract the data, two libraries had to be used: **requests and BeautifulSoup**.

The requests library allows to create a connection between Jupyter Notebook and the website. After having a stable connection, BeautifulSoup is used to extract the information we want.

In this case, the data that was extracted was the following:

* Name of the product;
* Price;
* Characteristics;
* Product Category;
* Number of items in stock;
* Rating;
* Discount (if applicable)

### Data Cleaning

Several steps had to be performed to clean the data because we are dealing with text that is usually written in different ways for each product and, in some cases, it might be have been scraped properly for every single product.

Such steps involved **standardizing the text, replacing empty values with a standard value, changing the data types of the columns and splitting columns for each product feature.

### Exporting the data

The final stage involves creating a connection the MySQL database and exporting the dataframe to the designated table. The final result is the one shown below.

![image 2](https://raw.githubusercontent.com/tmcdonald92/Web-Scraping/main/sql%20table.png)

Each one of these three stages is a function and all three are included in a pipeline so that all functions can be run in sequence. For more information, please check the [python file](https://github.com/tmcdonald92/Web-Scraping/blob/main/Web%20Scraping_Darty-Final.ipynb)
