# Pilih Browser
<table>
  <tr>
    <th>Chromium</th>
    <th>Firefox</th>
  </tr>
  <tr>
    <td><pre><code>yes | pkg install x11-repo -y
yes | pkg install tur-repo -y
yes | pkg install chromium -y</code></pre></td>
    <td><pre><code>yes | pkg install x11-repo -y
yes | pkg install firefox -y
yes | pkg install geckodriver -y</code></pre></td>
  </tr>
</table>


# Code
<table>
  <tr>
    <th>Type</th>
    <th>Chromium</th>
    <th>Firefox</th>
  </tr>
  <tr>
    <td>Headless</td>
    <td><pre><code>from selenium import webdriver
options = webdriver.ChromeOptions()
options.add_argument("--no-sandbox")
options.add_argument("--disable-dev-shm-usage")
options.add_argument("--headless=new")
driver = webdriver.Chrome(options=options)
driver.get("https://www.google.com")
driver.save_screenshot("/sdcard/download/screenshot.png")
print("Please check screenshot image")
driver.quit()</code></pre></td>
    <td><pre><code>from selenium import webdriver
options = webdriver.FirefoxOptions()
options.add_argument("--headless")
driver = webdriver.Firefox(options=options)
driver.get("https://www.google.com")
driver.save_screenshot("/sdcard/download/screenshot.png")
driver.quit()</code></pre></td>
  </tr>
  <tr>
    <td>Non-Headless</td>
    <td><pre><code>from selenium import webdriver
options = webdriver.ChromeOptions()
options.add_argument("--no-sandbox")
options.add_argument("--disable-dev-shm-usage")
options.add_argument("--display=:1") # localhost:1 -> display ID = 1
driver = webdriver.Chrome(options=options)
driver.get("https://www.google.com")
driver.save_screenshot("/sdcard/download/screenshot.png")
driver.quit()</code></pre></td>
    <td><pre><code>from selenium import webdriver
options = webdriver.FirefoxOptions()
options.add_argument("--display=:1") # localhost:1 -> display ID = 1
driver = webdriver.Firefox(options=options)
driver.get("https://www.google.com")
driver.save_screenshot("/sdcard/download/screenshot.png")
driver.quit()</code></pre></td>
  </tr>
</table>
