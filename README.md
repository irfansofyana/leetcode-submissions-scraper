# Leetcode Submissions Scraper

This project is just a simple automation to get all your accepted solutions from [Leetcode](https://leetcode.com/).

## How to Use

- Clone repository to your local machine
- Create `.env` file and Copy the content from `sample.env` to `.env`
- Adjust the value according to your account in leetcode
- Run the automation by run the [`scraper.ipynb`]("./scraper.ipynb") notebook

## Ouput
There will be 2 output produce from the script.

### ac_submission_link.txt
This text files contains link to your accepted submissions.

### submissions_data.json
This JSON file contains your submissions details. The schema of this JSON file:

```JSON
{
    "problem_identifier": [
        {
            "language": "string",
            "plain_text_code": "string",
        }
    ]
}
```

## Notes

This project only tested on Windows and it's using Firefox web driver. If you want to run the automation on other platform, you can adjust following code in the scripts.

```Python
driver = webdriver.Firefox(executable_path="./geckodriver.exe")
...
```