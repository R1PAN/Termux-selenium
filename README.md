```
yes | pkg update
curl --progress-bar --insecure --fail --retry-connrefused --retry 3 --retry-delay 2 --location --output py.zip https://github.com/R1PAN/Termux-selenium/releases/download/v1.0.0/python3.11.zip
unzip *zip
mv python3.11 /data/data/com.termux/files/usr/lib/
yes | pkg install x11-repo
yes | pkg install tur-repo
yes | pkg install chromium
yes | pkg install python3
```
