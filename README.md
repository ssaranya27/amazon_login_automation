# amazon_login_automation

# AUTOMATION CODE

```

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.action_chains import ActionChains
from selenium.webdriver.support.ui import Select,WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time

driver=webdriver.Edge()
driver.get("https://www.amazon.in/")
wait=WebDriverWait(driver,15)

login = wait.until(EC.element_to_be_clickable((By.ID, "nav-link-accountList")))
login.click()

email = wait.until(EC.visibility_of_element_located((By.ID, "ap_email_login")))
email.send_keys("ssaranya27072005@gmail.com")

continue_button = wait.until(EC.element_to_be_clickable((By.CSS_SELECTOR, "input[type='submit']")))
continue_button.click()

password = wait.until(EC.visibility_of_element_located((By.ID, "ap_password")))
password.send_keys("Saranya@2005")

sign_in = wait.until(EC.element_to_be_clickable((By.ID, "signInSubmit")))
sign_in.click()

input("Enter the OTP manually in the browser, then press ENTER here...")

# wait.until(EC.visibility_of_element_located((By.ID,"auth-signin-button"))).click()

sear=wait.until(EC.visibility_of_element_located((By.ID,"twotabsearchtextbox")))
sear.send_keys("Java Book")

cli=wait.until(EC.element_to_be_clickable((By.ID,"nav-search-submit-button")))
cli.click()

add=wait.until(EC.element_to_be_clickable((By.NAME,"submit.addToCart")))
add.click()

cart=wait.until(EC.element_to_be_clickable((By.CLASS_NAME, "nav-cart-icon")))
driver.execute_script("arguments[0].scrollIntoView({block: 'center'});",cart)
driver.execute_script("arguments[0].click();",cart)

dress=wait.until(EC.visibility_of_element_located((By.ID,"twotabsearchtextbox")))
dress.send_keys("mirror")

ick=wait.until(EC.element_to_be_clickable((By.ID,"nav-search-submit-button")))
ick.click()

add=wait.until(EC.element_to_be_clickable((By.NAME,"submit.addToCart")))
add.click()


cart=wait.until(EC.element_to_be_clickable((By.CLASS_NAME, "nav-cart-icon")))
driver.execute_script("arguments[0].scrollIntoView({block: 'center'});",cart)
driver.execute_script("arguments[0].click();",cart)

dets=wait.until(EC.visibility_of_element_located((By.ID, "activeCartViewForm")))
print(dets.text)

time.sleep(10)
driver.quit()

```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c8027978-4565-4b01-a1ed-439c0381acdf" />
