---
title: Building a Book Recommendation System
excerpt: A system recommends books to users based on their preferences
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/bf70872858e3ded6f68bbcc654c70245.png
---
## **Business Scenario**

The project is designed to recommend books to users based on their preferences. It uses data scraped from free scraping website [Books to Scrape](https://books.toscrape.com) and provides personalized recommendations through a web-based interface. This project integrates data scraping, preprocessing, machine learning, and a user-friendly interface to deliver a complete book recommendation solution, which could be used in e-commerce platforms, libraries, or book-related applications to enhance user experience and drive engagement.

## **Techniques**

- **Web Scraping**: Libraries like `beautifulsoup4`, `selenium`, and `scrapy` are used to scrape book data (e.g., titles, prices, ratings, descriptions) from websites.
- **Data Preprocessing**: `pandas` is used for data cleaning and transformation (e.g., cleansing prices, extracting stock numbers, mapping ratings). Regular expressions (`re`) are used to clean text and extract specific patterns.
- **Recommendation Engine**: `scikit-learn` is used to implement a **content-based recommendation system** using **TF-IDF vectorization** and **cosine similarity** to find books similar to a user's query.
- **Interactive User Interface**: `streamlit` library is used to create a web-based UI for users to interact with the system, input queries, and view recommendations.

## **Workflow**

### 1. **Data Collection**
- Scrape book data using one of three methods: `beautifulsoup4`, `selenium`, or `scrapy`.
### 2. **Data Preprocessing**
- The scraped data is cleaned and transformed (e.g., removing special characters, converting prices, mapping ratings).
### 3. **Building Recommendation System**
- The system uses TF-IDF vectorization to analyze book titles or descriptions and computes cosine similarity to recommend books similar to the user's query.
### 4. **Model Deploying**
-  A web-based interface built with `streamlit` allow users to interact with the system to get personalized book recommendations based on text input or filter data.

## **Functionalities**

- Get book recommendations by similar title or description
<img src="/assets/obsidian/bf70872858e3ded6f68bbcc654c70245.png" />

<img src="/assets/obsidian/1c6505653c3e19e0f8720e3b3feb2284.png" />

<img src="/assets/obsidian/de56ebb98b303f04a5919ebc2cffd34b.png" />

- Filter books by category, rating, and price range

<img src="/assets/obsidian/bacd956e83df6432227c36b093b7f1ce.png" />

<img src="/assets/obsidian/ad73877c8b48f729af9445206bcfdff2.png" />

## **Demo**

<iframe width="560" height="315" src="https://www.youtube.com/embed/PA00fRVP-dg?si=wltEM71Xi7oqb1d1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

