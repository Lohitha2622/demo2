1) from selenium import webdriver
from selenium.webdriver.edge.service import Service
from selenium.webdriver.common.by import By
import time

service=Service("C:\\Users\\K Joshna Rani\\Downloads\\edgedriver_win64\\msedgedriver.exe")

driver=webdriver.Edge(service=service)
driver.get("https://www.google.com")
time.sleep(5)

search_box=driver.find_element(By.NAME,"q")
print(search_box)
driver.quit()
2) from selenium import webdriver
from selenium.webdriver.edge.service import Service
from selenium.webdriver.edge.options import Options
import time

EDGE_DRIVER_PATH = r"C:\Users\K Joshna Rani\Downloads\edgedriver_win64\msedgedriver.exe"

edge_options = Options()
edge_options.add_argument("--start-maximized")

service = Service(EDGE_DRIVER_PATH)
driver = webdriver.Edge(service=service, options=edge_options)

# Open Facebook
driver.get("https://www.facebook.com")

print("Facebook login page opened.")
print("You have 60 seconds to login manually...")

# ✅ Wait for 60 seconds
time.sleep(5)

print("Time is up! Closing browser...")

driver.quit()
3)from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time
driver=webdriver.Edge()
driver.get("https://www.google.com")
time.sleep(2)
search_box=driver.find_element(By.NAME,"q")
search_box.send_keys("Selenium")
search_box.send_keys(Keys.RETURN)
time.sleep(3)
driver.quit()
