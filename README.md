# MyFitnessPal Parser

Parse a personal MyFitnessPal (MFP) diary into one or more data structure formats.

## Purpose

I was inspired to write a MFP parser because I am building a machine learning model to help identify foods that may contribute to an individual's adverse symptom(s). MyFitnessPal is a popular on-line food & exercise journaling application. It also has a couple options for entering 'symptoms' being experienced.

MyFitnessPal offers an API for extracting data. However, it is only available to premium paid account holders. 

By-pass the paid-account requirement by downloading your MFP diary (instructions below). Then run this parsing script.

This parser extracts all available MFP "Printable Diary" options available as of October 2019:
* Food Diary
* Exercise Diary
* Food Notes
* Exercise Notes

### Runtime options
* Manually downloaded diary filename (html format)
* Data structure output format(s)


#### Output format options
* JSON (list of embedded dictionaries)
* Pickle (list of dataframes)
* CSV file(s)


## Instructions


### Download Your MFP diary
To obtain a MyFitnessPal report in HTML format from a free account, follow these instructions (last tested: 2019-10-02).

Caveat: a maximum of 365 days worth of diaries can be extracted at one time. Fortunately, we can extract any 365 day time period.

1.  Logon with your MyFitnessPal account
1.	FOOD (top menu bar)
2.	“View Full Report” (button at bottom of page) 
3.	Enter From/To date range
4.	Check all boxes
5.	“change report” button
6.	From browser menu into the ../data directory:
  1. File
  2. Save Page as ... Webpage, Complete 


### Run this parser

## Input/Output


## TODO
* avoid filename hardcoding
* error handling
* better logging
* offer more output formats (e.g. SQL)
* ship-shape

## Status
* Proof of concept completed.
