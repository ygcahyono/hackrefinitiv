# Hackathon Refinitiv FTP 22-23

The aim of the [Hackathon](https://developers.refinitiv.com/en/use-cases-catalog/uni-hackathon) is to aid students to apply their academic knowledge within both a commercial and technically secure environment, enabling students to put themselves in the shoes of the professional working in financial and commercial fields.

- [X] News Headline Data (Last 15 Months)
- [X] Decide the companies or industries (Decision: Footsie FTSE100)
- [X] Pull out ESG Controversy Data for Footsie 2022 - 2023
- [X] Pull out News Headline Data for Footsie 2022 - 2023
- [ ] Pull out ESG Controversy Data for every company from 2021 - 2023
- [ ] Pull out News Headline Data for every company from 2021 - 2023
- [ ] Enhance the ESG News Filter
- [ ] Fin-BERT fine-tune model with current ESG News
- [ ] Ensemble Model or Severity Rate (Simple Math) on top of Fin-BERT to classify the actual ordinal label (A,B,C, etc.)

---
# **How To**

## **List of Footsie**

FTSE100 listed companies [link](https://www.londonstockexchange.com/indices/ftse-100/constituents/table?page=5)

## **Collect Headline Data from Refinitiv EIKON.**

There is a nice article by Jason Ramchadani talking about how to set proper query to pull out news headline data from Refinitiv EIKON, you can access [here](https://developers.refinitiv.com/en/article-catalog/article/introduction-news-sentiment-analysis-eikon-data-apis-python-example).

Using Refinitiv API is quite challenging because there is not enough documentation for that and also there are a lot of customisation. For retrieving the headline news we can use `get_news_headline` function with these arguments you can pass on:

- **query**:	
string, optional. Search criteria for the news headlines The query can contain RIC codes, company names, country names and operators (AND, OR, NOT, IN, parentheses and quotes for explicit search…). Tip: Append 'R:' in front of RIC names to improve performance. Default: Top News written in English
- **count**:	
int, optional. The maximum number of headlines to retrieve. Value Range: [1-100]. Default: 10

- **date_from**:	
string. Beginning of date range. String format is:'%Y-%m-%dT%H:%M:%S'. e.g. 2016-01-20T15:04:05.

- **date_to**:	
string. End of date range. String format is: '%Y-%m-%dT%H:%M:%S'. e.g. "2016-01-20T15:04:05".

- **raw_output**:	
boolean. Set this parameter to True to get the data in json format if set to False, the function will return a data frame The default value is False

- **debug**:	
boolean. If this parameter is set to True, the json request and response are printed.


To construct well writen query for the news headline we can head up to **news monitor** write your criteria on the search bar, copy and paste the result to your jupyter notebook.

---

**Team member**: Radhea, Maia, Yogi