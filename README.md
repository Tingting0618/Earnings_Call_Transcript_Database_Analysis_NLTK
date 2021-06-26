# Earnings Call Transcript Database And Analysis with Natural Language Toolkit in Python

## The goal/inspiration

During an earnings call, a public company's executives discuss the company's financial results and future projections with analysts, investors, and the media. 

These transcripts provide invaluable insights. However, it is quite challenging to extract valuable information from these transcripts, conduct analysis, compare transcripts from multiple companies, and observe future trends.

The goal of this project is to make earnings call analysis easy and save time for our users. 

## Demo

**Function 1: Get Words Frenquency by Choosing A Company and Year**

![count](https://user-images.githubusercontent.com/44503223/123526036-dd3cf780-d69a-11eb-9552-38237dcf9560.gif)

**Function 2: Followed by interesting key word counts in the previous step, now we are going to easily pull sentences from the earnings call transcript**

![recovery](https://user-images.githubusercontent.com/44503223/123526346-dc0cca00-d69c-11eb-9d66-b9d3d5fe4064.gif)


### Data source: Downloading all transcripts from a company's Investor Relations page using Python

Firstly, we have collected the earnings call transcript pdf links on companies' official websites. 

![URLS](https://user-images.githubusercontent.com/44503223/123524315-fdff5000-d68e-11eb-858e-2234ed961f80.png)

Then, we downloaded and saved each file as PDF, and consolidate all PDFs into a .pkl file. 

![pkl](https://user-images.githubusercontent.com/44503223/123524101-ab716400-d68d-11eb-8cca-010352b3a66c.png)

The final data structure looks like this... Each row will have one quarter's earnings call transcript from one company.  

![final df](https://user-images.githubusercontent.com/44503223/123524144-f1c6c300-d68d-11eb-9c8c-e6bda286ed6d.png)


### Technologies used

Python (request, NLTK, pandas, ipywidgets, pdfplumber)


## Learn More

You can learn more in the [Tingting Duan's Project Portfolio](https://tingting0618.github.io).

