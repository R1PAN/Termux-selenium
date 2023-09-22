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



Example
-------
| Jenis             | Kode                                                                                  |
|-------------------|---------------------------------------------------------------------------------------|
| Chrome Headless   | ```python\nfrom selenium import webdriver\noptions = webdriver.ChromeOptions()\noptions.add_argument("--no-sandbox")\noptions.add_argument("--disable-dev-shm-usage")\noptions.add_argument("--headless")\ndriver = webdriver.Chrome(options=options)\ndriver.get("https://www.google.com")\ndriver.save_screenshot("/sdcard/download/screenshot_chrome_headless.png")\ndriver.quit()\n``` |
| Firefox Headless  | ```python\nfrom selenium import webdriver\noptions = webdriver.FirefoxOptions()\noptions.add_argument("--headless")\ndriver = webdriver.Firefox(options=options)\ndriver.get("https://www.google.com")\ndriver.save_screenshot("/sdcard/download/screenshot_firefox_headless.png")\ndriver.quit()\n``` |
| Chrome Non-Headless | ```python\nfrom selenium import webdriver\noptions = webdriver.ChromeOptions()\noptions.add_argument("--no-sandbox")\noptions.add_argument("--disable-dev-shm-usage")\noptions.add_argument("--display=:1") # localhost:1 -> display ID = 1\ndriver = webdriver.Chrome(options=options)\ndriver.get("https://www.google.com")\ndriver.save_screenshot("/sdcard/download/screenshot_chrome_non_headless.png")\ndriver.quit()\n``` |
| Firefox Non-Headless | ```python\nfrom selenium import webdriver\noptions = webdriver.FirefoxOptions()\noptions.add_argument("--display=:1") # localhost:1 -> display ID = 1\ndriver = webdriver.Firefox(options=options)\ndriver.get("https://www.google.com")\ndriver.save_screenshot("/sdcard/download/screenshot_firefox_non_headless.png")\ndriver.quit()\n``` |
