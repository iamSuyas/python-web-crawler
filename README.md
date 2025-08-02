# Web Crawler and Basic Vulnerability Scanner

This project is a **multi-threaded web crawler and vulnerability scanner** developed in Python. It scans a target website for **common security vulnerability**, such as:

- Missing security HTTP headers
- Insecure form implementations


---


### Credits
This project could not have possible without the help of (freeCodeCamp's)[https://www.freecodecamp.org/] article on web crawling. (Article Link)[https://www.freecodecamp.org/news/build-a-web-application-security-scanner-with-python/]!
## Features

- Multi-threaded crawling of internal links
- Detection of missing security headers:
  - Strict-Transport-Security
  - X-Content-Type-Options
  - X-Frame-Options
  - Content-Security-Policy
- Scans HTML forms for insecure configurations (e.g., `method="get"` or missing `action`)
- Logs results to a file (`vulnerability_scan_report.log`)



## Getting Started

### Prerequisites

- Python 3.x
- Install dependencies:

```bash
pip install requests beautifulsoup4 urllib3
````




## Running the Tool

1. Clone this repository:

```bash
git clone https://github.com/iamSuyas/python-web-crawler.git
cd python-web-crawler
```

2. Run the crawler:

```bash
python vulnerability-scanner.py
```

3. Enter the website URL when prompted:

```
Enter Website URL to scan: https://yourtarget.com
```

Use the following website for webcrawling (a website for web scraping):

``` bash
https://books.toscrape.com/
```

A full report is saved in `vulnerability_scan_report.log`.

---

## Limitations and Assumptions

* Does **not perform deep payload-based scanning** (e.g., SQLi, XSS, RFI).
* Only checks for **visible vulnerabilities** based on page content and headers.
* Does not check for **outtdated versions** of applications