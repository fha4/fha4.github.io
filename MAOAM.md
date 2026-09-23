# MAOAM: MAOAM Automates Ordering of Amazing Meals
MAOAM is a python script that partially automates ordering a meal at a UofM dining hall.

This project is named after the candy brand MAOAM and their yummy "[Kracher](https://www.haribo.com/de-de/produkte/maoam/kracher)" candy.

## Program Architecture
MAOAM is built using the [Selenium Python Package](https://www.selenium.dev/). Selenium effectively lets a program click around on a website in the same manner that a human user can. This means that MAOAM can interact with M-Dining's websites, despite their lack of APIs.

Selenium requires that your computer has a web-browser and the corresponding web-driver. By default, MAOAM uses chrome, and expects that the binaries are in `/usr/bin/google-chrome` and `/home/[your_username]/bin/chromedriver`, respectively.

MAOAM primarily relies on hard-coded XPaths to know where to click / type. This means the reliability of the program is very susceptible to minor changes in HTML content.
  
## Setup
Retrieve MAOAM via `git clone git@github.com:fha4/MAOAM.git`.

Rename `starter_my_configs.py` to `my_configs.py`. Fill in the relevant information.

Download the [chromedriver binary](https://googlechromelabs.github.io/chrome-for-testing/). Place it in `/home/[your_username]/bin/chromedriver`. 

Modify MAOAM.py: Replace `service = Service(executable_path='/home/fha/bin/chromedriver')` with `service = Service(executable_path='/home/[your_username]/bin/chromedriver')`.

## Usage

In a terminal, run `python3 MAOAM.py`.

Via the terminal, enter the date on which you would like to pick up your food.

Respond yes or no to each food the program presents you with via the terminal.

Complete Okta Verify. When complete, inform the program that you have done so.

When the program has filled out the meal-ordering form, use the chrome window to enter the time for your meal.

Let the program know you are ready to submit via the terminal.

TODO: add photos

## Notes
MAOAM is only able to order breakfast at Bursley, and filters out many food options due to allergens.

For dining hall recommendations, please visit [this site](https://isitagooddaytoeatatbursley.com/).

## Other Links
- [MAOAM Repository](https://github.com/fha4/MAOAM)
- [https://www.selenium.dev/](https://www.selenium.dev/)
- [https://developer.chrome.com/docs/chromedriver](https://developer.chrome.com/docs/chromedriver)
