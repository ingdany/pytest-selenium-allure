# pytest-selenium-allure
This is a test to return allure reports after a pytest selenium framework.

# Install package
`pip install allure-pytest`

# Download and install Allure
https://mvnrepository.com/artifact/io.qameta.allure/allure-commandline/2.8.1

# Execution
`pytest -v -s test.py --alluredir=path`

# Jenkins

1. Install Allure plugin
2. Go to Global Tool configuration -> Allure Commandline
3. Click Add Allure Commandline
4. Click Install Automatically, i choose option 2.8.1
5. Click Add Installer
6. Apply and save
7. Go to configure your item
8. Use advanced options to set your *custom workspace*
9. Set Execute Batch Command

```
call c:/src/python/django/dev/scripts/activate.bat
cd /src/python/selenium/test
pytest -v -s --alluredir='reports' test.py
```

10. Post Build Actions

Path = reports

11. Apply and save.
