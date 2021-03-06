# Linkedin Scraper
Scrapes Any Linkedin Data

## Installation

```bash
$ pip install git+git://github.com/jqueguiner/lk_scraper
```


## Setup
### Using Docker compose
```bash
$ docker-compose up -d
$ docker-compose run lk_scraper python
```

### Locally
First, you need to run a selenium server

```bash
$ docker run -d -p 4444:4444 --shm-size 2g selenium/standalone-firefox:3.141.59-20200326
```

After running this command, from the browser navigate to your IP address followed by the port number and /grid/console. So the command will be
[http://localhost:4444/grid/console](http://localhost:4444/grid/console).

## A full working example
run the jupyter notebook linkedin-example.ipynb


## Usage

```python
from lk_scraper import Scraper
scraper = Scraper()
```
You can add your linkedin li_at cookie in the config file that is located in your home (~/.lk_scraper/config.yml)
see
![https://github.com/jqueguiner/lk_scraper/raw/master/config_yaml.png](https://github.com/jqueguiner/lk_scraper/raw/master/config_yaml.png)

### Company Scraping

```python
from lk_scraper import Scraper
scraper = Scraper()
company = scraper.get_object(object_name='company', object_id='apple')
```

### Profil Scraping

```python
from lk_scraper import Scraper
scraper = Scraper()
profil = scraper.get_object(object_name='profil', object_id='jlqueguiner')
```
