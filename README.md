# Spring2018
# Project 1:

----


### [SPOOKY Data Analysis: Comparing sentiments and topics between authors](doc/)
This is the first and only *individual* (as opposed to *team*) this semester. 
+ This project is conducted by David Arredondo

Term: Spring 2018
This folder is organized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```
Please see each subfolder for a README file.

### Project summary: Using sentiment analysis and topic modeling, I illustrate the differneces between the sentences of Edgar Allen Poe (EAP), H.P. Lovecraft (HPL), and Mary Wollstencraft Shelly (MWS).

#### Description of the Data
The SPOOKY data set consists of several thousand sentences from each of EAP, HPL, and MWS. These sentences were labeled with unique ids,
and with their respective authors.

I chose to work exclusively with the sentences seperated into three groups by auhtor.

Here's a quick illustration of the dataframes:

![Sentence Distribution by Author](https://github.com/GU4243-ADS/spring2018-project1-dca2123/blob/master/figs/num_spooky_sente.png)

Now, let's get started with the analysis.

#### Sentiment Analysis with Polarity Scores

First, I compared how positive, negative, or neutral each author is. Although these author wrote at least over 100 years ago,
positiveity and negativity are fundamental, basic concepts in human communication. The words communicating those sentiments are more
likely to remain the same or similar over time.

With that said, here's the authors scores compared:


