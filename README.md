# Earnings Call Transcript Database and Analysis with NLTK in Python

## The goal/inspiration

Nick and Jack, the hosts of Robinhood Snacks Daily, often talk about how many times a certain word is mentioned during a company's earnings call. For example, "Mirrors" appeared 40 times while "Lululemon" was only mentioned 25 times by the executive team, indicating Mirrors is the focus of investors and long-term strategy for customer engagement. 

These earnings call transcripts provide invaluable insights. However, it is quite challenging to extract valuable information from these transcripts, conduct analysis, compare transcripts from multiple companies and multiple years, and observe future trends.

The goal of this project is to make earnings call analysis easy and save time for our users. 

## Demo

**Function 1: Get Words Frequency by Choosing A Company and Year**

![count](https://user-images.githubusercontent.com/44503223/123526036-dd3cf780-d69a-11eb-9552-38237dcf9560.gif)

**Function 2: Followed by interesting keyword counts in the previous step, now we will pull sentences from the earnings call transcript to understand more context.**

![recovery](https://user-images.githubusercontent.com/44503223/123526346-dc0cca00-d69c-11eb-9d66-b9d3d5fe4064.gif)

**Function 3: The Word Trends.**

Due to Covid-19, the hospitality industry was hit hard. The keyword in 2020 is "recovery". China was mentioned 86 times by the Marriott executive team and analysts in 2020's earnings call. 

![record](https://user-images.githubusercontent.com/44503223/123528921-3748b780-d6b1-11eb-918a-1d37eb40bf6c.gif)

**Function 4: The Sentiment**

Based on previous analyses, recovery is the focus of 2020. Next, we are going to explore the sentiment related to recovery. Two possible scenarios: 1) people may think the recovery will be slow and the situation will be unstable, or 2) people have a positive view of the future due to the fast recovery in China once Covid-19 is under control.

Screenshot of some sentences' sentiment scores:

![Sentiment](https://user-images.githubusercontent.com/44503223/123529363-079bae80-d6b5-11eb-92bd-aa1215c607ea.png)

The overall sentiment score distribution:

![overall](https://user-images.githubusercontent.com/44503223/123529720-b4c3f600-d6b8-11eb-92d1-8fd6f580a344.png)

Overall, the company executives have a very positive view of recovery and potential performance rebounce. 

## Data source

#### Transcripts downloaded from a company's Investor Relations page using Python

Firstly, we have collected the earnings call transcript pdf links on companies' official websites. 

![URLS](https://user-images.githubusercontent.com/44503223/123524315-fdff5000-d68e-11eb-858e-2234ed961f80.png)

Then, we downloaded and saved each file as PDF, and consolidate all PDFs into a .pkl file. 

![pkl](https://user-images.githubusercontent.com/44503223/123524101-ab716400-d68d-11eb-8cca-010352b3a66c.png)

The final data structure looks like this... Each row will have one quarter's earnings call transcript from one company.  

![final df](https://user-images.githubusercontent.com/44503223/123524144-f1c6c300-d68d-11eb-9c8c-e6bda286ed6d.png)


## Technologies used

Python (request, NLTK, pandas, ipywidgets, pdfplumber)


## Learn More

For more information, please check out the [Project Portfolio](https://tingting0618.github.io) page.
