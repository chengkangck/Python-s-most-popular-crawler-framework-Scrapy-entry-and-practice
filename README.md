# Python-s-most-popular-crawler-framework-Scrapy-entry-and-practice
Python's most popular crawler framework Scrapy entry and practice

Introduction: Scrapy, a fast, high-level web scraping framework developed by Python for scraping web sites and extracting structured data from pages. Scrapy is versatile and can be used for data mining, monitoring, and automated testing. Anyone can easily modify it according to their needs. It also provides many types of crawler base classes, such as BaseSpider, sitemap crawler, etc. The latest version also provides support for web2.0 crawlers. 

**Section 1.project introduciton**
## scrapy introduction

## installation of scrapy

## Pit often encountered during scrapy installation

## mongodb installation

## scrapy framework, components, data flow

## scrapy data scraping

**Section 2.Scrapy framework, mongodb database installation and scrapy practice**

### Introduces the installation of scrapy framework and mongodb database in detail. 

### through the scrapy framework architecture, explains the role of each component of scrapy, and how scrapy flows in the framework when scrapy is capturing data

### Demonstrates how scrapy is configured in the project, how to write it, how to parse and grab the data, and finally stores the data in mongodb.


### 2-1 scrapy installation and problems encountered during installation

Install Scrapy: pip install scrapy
Problems encountered during installation:

1 pip cannot request the https website and requires the ssl module to be installed:  sudo yum install -y openssl-devel

2 Compiling and installing Python needs to be recompiled after installing openssl-devel:

3 Twisted installation failed, at this time you need to go to a website to search for download: https://pypi.org/

### 2-2 scrapy introduction, components, data flow

How do we do data scraping without Scrapy?

urllib or requests

Multi-threaded or coroutine

Encapsulating the http header class

Wrapper proxy class

Encapsulated data storage class

Encapsulating deduplication classes

Package anomaly detection class

Make a bunch of wheels, headache

What is Scrapy?

Scrapy is an asynchronous processing framework based on Twisted. It is a crawler framework implemented in pure Python. Users only need to customize and develop a few modules to easily implement a crawler to capture web page content or various pictures. The coupling between the modules is very low, and the expansion is flexible.
What does Scrapy look like?

That Scrapy architecture diagram will not be let go, you can find it just by searching

### 2-3 mongodb database installation

### 2-4 New scrapy project

Scrapy project combat: grab the Douban movie top250, save the data as csv, json and store it in the mongo database
Destination URL: https://movie.douban.com/top250

New Project

scrapy startproject douban

cd into the douban project and execute scrapy genspider douban_spider movie.douban.com

Run the crawler: scrapy crawl douban_spider

Debug website: scrapy shell www.baidu.com

clear goal

Making reptiles

Store content

### 2-5 Clear goals

Write items.py

### 2-6 writing spider files

### 2-7 Save data

Save to json file: scrapy crawl douban_spider -o test.json

Save to csv file: scrapy crawl douban_spider -o test.csv

Save to mongodb:

### 2-8 IP proxy middleware writing

### 2-9 Writing user-agent middleware
