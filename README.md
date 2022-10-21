# BBC News Scraper

Scrape news articles from BBC using google search.

## Description

Search for news articles from BBC news through google search engine.

You can pick how many pages you would like to fetch from.

The articles will be formatted and ready to be saved as json or sent to your DB.

PS : Feel free to change the news source but note that the article formatter only supports BBC articles.

## Getting Started

### Installing

* Download the repository

```
git clone https://github.com/riad-azz/bbc_news_scraper.git
```

* Navigate to the repository folder

```
cd bbc_news_scraper
```

* Install required packages

```
pip install -r requirements.txt
```

### Executing program

* Fetching articles
```python
from bbc_scraper import NewsScraper

scraper = NewsScraper()
scraper.get_news(q="News", pages=1)
```

* If you would like to save the articles after fetching them (_File will be saved as a json_)
```python
from bbc_scraper import NewsScraper

scraper = NewsScraper()
scraper.save_news(q="News", pages=1, filename='news', save_path="./news")
```

## Help

* If you are facing problems with getting 0 results even though there are results, just update the user agents in (_scrape_news/bbc_scraper/utils.py_) to the latest ones.

```python
UserAgents = [
    "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:105.0) Gecko/20100101 Firefox/105.0",
    "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36 "
    "Edg/106.0.1370.47 ",
    "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36",
    "Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36",
    "Mozilla/5.0 (Windows NT 10.0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36",
    "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36 "
    "OPR/91.0.4516.20 "
]
```

* Article example

```python
{
  "title": "Title",
  "link": "https://www.bbc.com/news/article-name-example",
  "desc": "Random description example, random text example random text example.",
  "thumbnail": "https://www.example.com/news/image_name_id.png",
  "source": {
    "name": "BBC News",
    "short": "BBC"
  },
  "published": "2022-01-24 12:00:00",
  "article": "Lorem Ipsum is simply dummy text of the printing and typesetting industry."
  "Lorem Ipsum has beenthe industry's standard dummy text ever since the 1500s, when an"
  "unknown printer",
  "author": "Author Name",
  "tags": [
    "random-tag",
    "tag-random"
  ],
  "photos": [
    "https://www.example.com/news/image_name_id_01.png",
    "https://www.example.com/news/image_name_id_02.png",
    "https://www.example.com/news/image_name_id_03.png",
  ]
}
```

## Authors

Riadh Azzoun - [@riad-azz](https://github.com/riad-azz)

## Version History

* 0.1
    * Initial Release

## License
#### PS : Do not use commercially without [@BBC](https://bbc.com/) permission.
This project is licensed under the [MIT] License - see the LICENSE.md file for details