# 📰 Sentiment Analysis of Shopee in Indonesian News Media

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Web Scraping](https://img.shields.io/badge/Web-Scraping-green)
![NLP](https://img.shields.io/badge/NLP-Natural_Language_Processing-blue)
![NLTK](https://img.shields.io/badge/NLTK-3776AB?style=for-the-badge&logo=nltk&logoColor=white)

## 📖 Overview
Since its launch in 2015, Shopee has grown into one of Indonesia's most popular e-commerce platforms. To understand its public perception, this project performs sentiment analysis by scraping news articles related to Shopee from a major Indonesian news outlet, **detik.com**. The goal is to analyze the sentiment conveyed in the news and explore the key topics and entities associated with Shopee in the media.

## 📊 Dataset
Unlike previous projects, the dataset for this analysis was not downloaded but **created from scratch** using web scraping techniques.

* **Source:** News articles from **detik.com**.
* **Scraping Method:** A custom Python script using the `requests` and `BeautifulSoup` libraries was developed to gather articles containing the keyword "Shopee".
* **Final Dataset:** The process resulted in a dataset of **133 unique news articles**, each including the headline, publication date, and full content.

## ⚙️ Project Workflow
The project followed an end-to-end data science pipeline:

1.  **Web Scraping:** Collected 133 relevant news articles from detik.com.
2.  **Text Pre-processing:** The raw text data was extensively cleaned and prepared for analysis. This involved:
    * Removing duplicate articles.
    * Converting text to lowercase.
    * Removing punctuation, special characters, and Indonesian stopwords.
    * Applying stemming for the Indonesian language using the `Sastrawi` library.
3.  **Sentiment Analysis:** The sentiment for each news headline was calculated using `NLTK`'s `SentimentIntensityAnalyzer`.
4.  **Exploratory Data Analysis (EDA):** Various visualizations were created to analyze the data, including:
    * **Word Cloud** and **Term Frequency** charts to identify the most common words.
    * **Link Graph** to visualize the connections between the most frequent terms.
5.  **Social Network Analysis (SNA):** A network graph was constructed to analyze the centrality and relationships between key terms such as 'shopee', 'indonesia', and 'perusahaan' (company).

## 📈 Key Findings & Insights
* **Term Frequency:** The most frequent and central words in the news corpus were **`shopee`**, **`indonesia`**, and **`untuk`** (for), indicating that news coverage often frames Shopee within a national context.
* **Sentiment:** The overall sentiment of news articles regarding Shopee was found to be **predominantly positive**.
* **Social Network Analysis:** The term `indonesia` emerged as the node with the highest centrality, acting as a bridge connecting `shopee` with `perusahaan` (company). This suggests that media narratives often focus on Shopee's role and impact as a major corporate entity within Indonesia.

![image](https://github.com/user-attachments/assets/e331993b-4607-40ee-ad09-44b1d3d796f4)
