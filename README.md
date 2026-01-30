# Selenium_Python_Challenge1
Run the script

from selenium import webdriver
from selenium.webdriver.common.by import By
from time import sleep

driver = webdriver.Chrome()
driver.get("https://the-internet.herokuapp.com/")
driver.maximize_window()

# o Find the heading "Welcome to the-internet" using TAG_NAME.
 heading = driver.find_element(By.TAG_NAME, "h1")
 sleep(3)
 print(heading.text)
# o Find the "Checkboxes" link using LINK_TEXT.
driver.find_element(By.LINK_TEXT, "Checkboxes").click()
sleep(3)
driver.back()
sleep(3)
# o Find how many <li> (list item) elements are on the page
list = driver.find_elements(By.TAG_NAME, "li")
count = 0
for item in list:
     count = count + 1
 print(count)
