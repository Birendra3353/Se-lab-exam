from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.options import Options
import time

chrome_options = Options()
chrome_options.add_argument("--start-maximized’)
service = Service("/path/to/chromedriver")

driver = webdriver.Chrome(service=service, options=chrome_options)

driver.get("https://www.facebook.com")
time.sleep(5)
expected_title = "Facebook – log in or sign up"
if expected_title in driver.title:
    print("✅ Facebook launched successfully!")
else:
    print("❌ Unexpected page title:", driver.title)
time.sleep
driver.quit()
