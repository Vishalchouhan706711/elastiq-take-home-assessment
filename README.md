Selenium Test with Pytest

This project demonstrates the use of Selenium with Pytest to test the search functionality of a table on the Selenium Playground website.

Overview

The script performs automated testing of a web application's table search functionality. It uses Selenium WebDriver to interact with the webpage and Pytest as the testing framework to ensure that the functionality meets the expected behavior.

Key Features

Browser Automation: Automates Chrome browser using Selenium WebDriver.

Search Validation: Tests the search functionality of a table on the Selenium Playground page.

Dynamic Element Handling: Locates elements dynamically using XPath.

Pytest Framework: Utilizes Pytest to handle setup, execution, and teardown of test cases.

Prerequisites

Install the required Python packages:

pip install selenium pytest webdriver-manager

Code Breakdown

1. Constants

SELENIUM_PLAYGROUND_URL: URL of the Selenium Playground page to be tested.

SEARCH_TERM: The keyword used for searching in the table ("New York").

EXPECTED_RESULTS_COUNT: Number of table rows expected to match the search term (5).

2. WebDriver Setup

The driver fixture initializes the Chrome WebDriver using webdriver-manager to automatically download the appropriate driver version. It also sets an implicit wait to ensure smooth handling of dynamically loaded elements.

3. Test Case: test_search_functionality

This test case performs the following steps:

Navigate to the webpage: Opens the specified URL.

Locate and interact with the search box: Inputs the search term "New York."

Locate table rows: Fetches all rows of the table using XPath.

Filter visible rows: Filters rows to only include visible elements that match the search.

Validation: Asserts that the number of visible rows matches the expected count.

4. Execution

The script can be executed directly using Pytest:

pytest -v selenium_test.py

Expected Output

When Passed: The test confirms that the search functionality displays the correct number of rows matching the search term.

When Failed: The test provides an assertion error showing the discrepancy in the expected and actual number of results.

Example output:

service ====>>>> <selenium.webdriver.chrome.service.Service object at 0x...>
Searched for New York
table_rows ====>>>> [<selenium.webdriver.remote.webelement.WebElement object at 0x...>]
visible_rows ====>>>> [<selenium.webdriver.remote.webelement.WebElement object at 0x...>]
PASSED

Benefits of This Code

Professional Test Automation: Demonstrates proficiency in writing efficient and reusable test scripts.

Use of Best Practices: Implements fixtures for setup and teardown, ensuring clean resource management.

Dynamic Testing: Handles dynamic content like visible table rows intelligently.

Modern Tools: Showcases the use of webdriver-manager for simplifying WebDriver management.

