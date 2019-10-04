# MyFitnessPal Diary Parser

Parse a MyFitnessPal (MFP) diary into CSV file(s).

## Purpose

The inspiration behind this parser is a machine learning model I'm working that will help identify foods that could be contributing to an individual's condition (e.g. allergy, IBS, keto level, etc.) 

In order to analyze food logs, we need to create and access data in a format we can use. 

MyFitnessPal is a popular on-line food & exercise journaling application. It has a free-account option and is a great candidate tool for data creation. 

MyFitnessPal does offer an API for extracting data, and there are a number of github repositories to access that API. However, the API is only available to premium paid account holders. 

What MFP does provide to free-account holders is a report we can download into an HTML file.

To extract data from the downloaded HTML file into a format you can use, run this `myfitnesspal-diary-parser`.

## Instructions

### 1. Download Your MFP diary to an HTML file
(last tested: 2019-10-02)

Caveat: a maximum of 365 days worth of diaries can be extracted at one time. Fortunately, we can extract any 365 day time period.

1. Log onto with your MyFitnessPal account [https://www.myfitnesspal.com/]
1. Click `FOOD` (in the top menu bar)
2. Click `View Full Report` (at bottom of page) 
3. Enter From/To date range
4. Check all boxes of interest (Food Diary, Exercise Diary, Food Notes, Exercise Notes)
5. Click `change report` button on top right
6. From your browser menu, click `File`
6. `Save Page as` .... `Webpage, Complete` (exact menu options may differ depending on your browser)

### 2. Update notebooks/config.ini

### 3. Open and Run Jupyter Notebooks `myfitnesspal-diary-parser.ipynb`
Depending on which 'boxes of interest' you chose when creating the report, a CSV file will be created for each:
* Food Diary
* Exercise Diary
* Food and/or Exercise Notes

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
- [ ] consider reading/writing to/from data/input and data/output
- [x] avoid runtime option hardcoding
- [ ] improve error handling
- [ ] better logging
- [ ] offer more output formats (e.g. SQL)

