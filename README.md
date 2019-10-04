# MyFitnessPal Diary Parser

Parse a MyFitnessPal diary into CSV file(s).

## Purpose

MyFitnessPal (MFP) is a popular, easy-to-use, on-line food & exercise diary application. MFP even generates nutrition statistics automatically.

People interested in independently analyzing MFP data need to be able to extract diary data in a usable format.

MyFitnessPal  offers an API for extracting data, and there are a number of github repositories to access that API. However, the API is only available to **premium paid account** holders. 

Fortunately, MFP provides **free-account** holders with an option to download their diary to an HTML file.

`myfitnesspal-diary-parser` is available to extract data from a downloaded HTML file, parsing it into a CSV file, which you can then use in any manner you see fit.

## Instructions

Clone or download this GitHub repository.

```sh
$ git clone https://github.com/leaherb/myfitnesspal-diary-parser.git
```
Then ...

#### 1. Download Your MFP diary to an HTML file
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

#### 2. Update runtime options
Edit **~/notebooks/config.ini** to update the name and location of your HTML file, and desired output files.

#### 3. Open Jupyter Notebooks 
Run **~/notebooks/myfitnesspal-diary-parser.ipynb**

#### Output
Depending on which 'boxes of interest' you chose when creating the report, a CSV file will be created for each:
* Food Diary
* Exercise Diary
* Food and/or Exercise Notes

The output file(s) are named using the output_file name you identified in ~/notebooks/config.ini, prefixed with 'food_', 'exercise_', and/or 'notes_'.

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
- [ ] consider separating input and output files into their own subdirectories
- [x] avoid runtime option hardcoding
- [ ] improve error handling
- [ ] better logging
- [ ] offer more output formats (e.g. SQL)
- [ ] extract from the notebook to make command-line friendly

