---
---

#### Dockerfile
```
FROM selenium/standalone-chrome
RUN sudo apt-get update && \
    sudo apt-get install -yqq python3 python3-pip && \
    sudo rm -rf /var/lib/apt/lists/*
ADD . /code
WORKDIR /code
RUN python3 -m pip install -r requirements.txt
CMD ["python3", "-m", "unittest"]
```

#### docker-compose-yml
```
version: '3'
services:
  selenium:
    build: .
    ports:
     - 4444:4444
    volumes:
     - .:/code
     - /dev/shm:/dev/shm
```

#### tests.py
```python
# Run with hidden browser
options = webdriver.ChromeOptions()
options.add_argument('--headless')
browser = webdriver.Chrome(options=options)
```

### Test design
Page Object Design Pattern is recommended to be used on Selenium tests.

- [Selenium documentation](https://www.seleniumhq.org/docs/06_test_design_considerations.jsp#page-object-design-pattern)
- [Blog](https://www.pluralsight.com/guides/getting-started-with-page-object-pattern-for-your-selenium-tests)
