---
layout: post 
title: Nashville Data Cleaning
date: 13-11-2024
categories: [documentation]
tag: [data, cleaning, sql]
---

# Nashville Housing Data: Cleaning Data

## Introduction

This case study focuses on cleaning Nashville’s Housing data through using SQL. A quick preview of what I do during this cleaning process consisted of: 

 - Fix the date format
    
 - Populating missing addresses

 - Breaking up the property address and owner address into individual columns (ex: address, city, state)

 - Change Y and N to Yes and No 

 - Remove duplicates 

 - Delete unused columns 

By using SQL queries, I clean the data to ensure the accuracy and consistency the data set. The following are the steps I took: 

### Standardizing the Date Format
Initially the data showed a date/time format in the SaleDate column. The query converts the date/time format to update only to show a date. 

![Standardizing the Date Format](/assets/images/Nashville1.png)

### Populate Property Address Data
In the PropertyAddress column there was null data. I first joined the table to itself to allow find relationships or patterns between different rows within the same table. I then updated the table to populate data into the PropertyAddress column where there was no address. 

![Populate Property Address Data](/assets/images/Nashville2.png)


### Break out PropertyAddress into individual columns
I used the query to break apart the PropertyAdress column into individual columns for the address and the city.

![Break out PropertyAddress into individual columns](/assets/images/Nashville3.png)

### Break out OwnerAddress into individual columns
I used the query to break apart the OwnerAddress column into individual columns for the address, city and state. 

![Break out OwnerAddress into individual columns](/assets/images/Nashville4.png)

### Change Y and N to Yes and No 
This query helped to change the “Y” and “N” values into “Yes” and “No” values instead. 

![Change Y and N to Yes and No](/assets/images/Nashville5.png)

### Remove duplicates 
This query removed duplicate rows. 

![Remove duplicates](/assets/images/Nashville6.png)

### Delete unused columns 
This query deletes unused columns.

![Delete unused columns](/assets/images/Nashville7.png)
