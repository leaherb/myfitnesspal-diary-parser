# MyFitnessPal Parser

Parse a MyFitnessPal (MFP) diary from a free MFP account. Output data into one or more data structures (e.g. JSON, CSV, Pickle).

### Status 
Proof-of-concept is complete: notebooks/myfitnesspal-diary-parser.ipynb works as is. 

Improvements actively being made:
* update notebook to optimize functions that build various output options
* create runtime options file (remove hardcoding)

## Purpose

I am building a machine learning model to help identify foods that could be contributing to an individual's physical condition(s). In order to train and use the model, I need data. MyFitnessPal is a popular on-line food & exercise journaling application. It has a free-account option and several methods for adding 'food reaction symptoms' to a journal, making it a great candidate tool for data creation. 

To extract data from an individual's MFP account, I needed a parser. Which is the inspiration behind `myfitnesspal-diary-parser`.

MyFitnessPal does offer an API for extracting data, and there are a number of github repositories to access that API. However, the API is only available to premium paid account holders. 

By-pass the paid-account requirement by downloading your MFP diary (instructions below).

This parser extracts all available MFP "Printable Diary" options available as of October 2019:
* Food Diary
* Exercise Diary
* Food Notes
* Exercise Notes

#### Output format options
* JSON (list of embedded dictionaries)
* Pickle (list of dataframes)
* CSV file(s)


## Instructions

### Download Your MFP diary
To download your MyFitnessPal diary from a free account, follow these instructions (last tested: 2019-10-02).

Caveat: a maximum of 365 days worth of diaries can be extracted at one time. Fortunately, we can extract any 365 day time period.

1. Logon with your MyFitnessPal account
1. FOOD (top menu bar)
2. “View Full Report” (button at bottom of page) 
3. Enter From/To date range
4. Check all boxes
5. “change report” button
6. From browser menu into the ../data directory:
   - File
   - Save Page as ... Webpage, Complete 


### Run this parser

## Input/Output

## How to Contribute

I encourage you to make pull requests and help improve this project.

Use the Udacity Git Commit Message Style Guide (https://udacity.github.io/git-styleguide/), and follow the "fork-and-pull" Git workflow:

1. Fork the repo on GitHub
1. Clone the project to your own computer
1. Commit changes to your own branch
1. Push your work back up to your fork
1. Submit a Pull request so that I can review your changes

Note: Please take care to merge the latest from "upstream" before making a pull request.


## TODO
- [ ] improve README.md
- [ ] avoid runtime option hardcoding
- [ ] improve error handling
- [ ] better logging
- [ ] offer more output formats (e.g. SQL)

