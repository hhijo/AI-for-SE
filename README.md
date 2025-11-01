📘 README – Safaricom Login Automation using Selenium
🧩 Project Overview

This project automates the login process for the Safaricom Login Portal using Selenium WebDriver in Python.
It demonstrates how AI-powered automation can enhance software testing by reducing manual test effort and improving test coverage.

The script tests:

✅ Valid login credentials

❌ Invalid login credentials

Each test waits for the necessary elements to load dynamically and verifies the outcome (success or error message).

⚙️ Requirements

Make sure the following tools and packages are installed:

1. Python Environment

Python 3.9+

pip (Python package manager)

2. Install Dependencies

Run the command below to install required packages:

pip install selenium

3. WebDriver

Download and install Google Chrome and the matching ChromeDriver version:

Chrome: https://www.google.com/chrome/

ChromeDriver: https://chromedriver.chromium.org/downloads

Make sure the ChromeDriver executable is in your system PATH.

🚀 How to Run the Tests

Save the test script as test_safaricom_login.py.

Open a terminal or command prompt in the project directory.

Run:

python -m unittest test_safaricom_login.py


This will execute two test cases:

test_valid_login

test_invalid_login

🧠 Test Logic Summary
Test Case	Description	Expected Result
test_valid_login	Logs in with correct credentials	Redirects to user dashboard or shows "Welcome" message
test_invalid_login	Attempts login with invalid credentials	Displays "Invalid login" or similar error
🕒 Handling Dynamic Pages

The test uses:

WebDriverWait(driver, 15).until(EC.presence_of_element_located((By.ID, "username")))


This ensures elements are fully loaded before Selenium interacts with them — ideal for dynamic sites like Safaricom’s.

🧪 Example Output
..
----------------------------------------------------------------------
Ran 2 tests in 12.7s

OK


If elements are not found or the login fails unexpectedly, Selenium will raise:

NoSuchElementException


In that case, verify the element IDs or use alternative locators (By.XPATH, By.CSS_SELECTOR).

🔒 Important Notes

Do not use real Safaricom credentials. Use dummy or test accounts.

Some Safaricom pages include security checks (CAPTCHAs) that block automated scripts.

For professional use, request access to a testing or staging environment.

🧰 Optional: Run Headless

To run without opening a browser window:

from selenium.webdriver.chrome.options import Options
options = Options()
options.add_argument("--headless")
driver = webdriver.Chrome(options=options)

🧾 Author

Wendy Atieno
Data Scientist | Software Automation Enthusiast
