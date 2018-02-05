# Spring2018
# Project 1:

----


## [SPOOKY Data Analysis: Comparing sentiments and topics between authors](doc/)
 This project is conducted by David Arredondo

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

## Project summary: 
### Using sentiment analysis and topic modeling, I illustrate the differneces between the sentences of Edgar Allen Poe (EAP), H.P. Lovecraft (HPL), and Mary Wollstencraft Shelly (MWS).

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

With that said, here's the average polarity score of each author's sentences:

![Polarity Scores](https://github.com/GU4243-ADS/spring2018-project1-dca2123/blob/master/figs/spooky_sentiments.png)

EAP and HPL stray from neutral about the same amount on average.
MWS, comparitively, swings through positive and negative sentiments far more often.

EAP and MWS tend to be more positive than negative on average; HPL favors negativity.

#### Topic Modeling: Comparing and contrasting Non-negative Matrix Factorization (NMF) and Latent Dirichlet Allocation LDA)

I will focus mainly on the difference between LDA and NMF with MWS, because 1. this phase of the analysis is almost purely subjective and my analysis and bias would be redundant if indulged further, and 2. MWS had the most convincing topics.
See the python notebook for inter author topic comparison.

I chose tfidf as it provided, in my opinion, better results, and because nmf does not work with simple counts; it requires
tfidf, and I wanted to compare nmf and lda on as equal terms as possible.

Finally, I claim that nmf provides more human interpretable topics. Obviously, human interpretability is secondary for the author classification problem, but this is an oppurtunity to dicover which algorithm gets closer to human thought, as an intellectual exercise.

##### LDA
```
'0 smile self added secret actions permitted sense',
 '1 fancy force visited man vain nature great',
 '2 day passed night remained years saw hours',
 '3 began read greek possess plan books philosophy',
 '4 adrian say said struck health set true',
 '5 love passion cold knew easily farewell people',
 '6 air rose wind journey winter enemy came',
 '7 raymond perdita idris mother dear sister let',
 '8 miserable world die happy pain hopes native',
 '9 looked eyes voice sat men like evil',
 '10 went arrived common thou length thee various',
 '11 feelings did return human leave know morning',
 '12 entered plague city fell alas life months',
 '13 little replied change kindness discovered cause father',
 '14 feel heart words tears hand shall eyes'
```
For LDA, topics 2 and 14 seem reasonable, with 2 being the passage of time, and 14 as pwoerful feelings in te heart or soul.
Others are either indecipherable (topic 10), or complicated and difficult to qualify (topic 0).

##### NMF
```
 '0 eyes father saw like tears thought mind',
 '1 raymond lord replied secret lost room gave',
 '2 love let sympathy gratitude affection greece gentle',
 '3 did appear understand come know return pass',
 '4 life existence alas hope lost new feeling',
 '5 said dear better present best friend companion',
 '6 day night passed sun following hour close',
 '7 man old world young nature earth creation',
 '8 shall true die know make appear feel',
 '9 time long mean spent short greece come',
 '10 perdita mentioned evadne child length joined account',
 '11 adrian idris promised visit sister health feared',
 '12 heart remorse soul fear grief despair filled',
 '13 years passed age nearly old lived early',
 '14 death fear disease words dead oh evil'
```
NMF on the other hand, provides a whole slew of accurate and recognizable topics. These include the warm, positive emotions of topic 2,
and then intense negativity of topic 14. Topics 5, 6, 12 and 13 also allow clear interpretation. 
Only three or so topics are complete nonsense.

#### Visualization of LDA

Although I prefer Non-negative Matrix Factorization for its tendency to give subjectively better results,
LDA does have the advantage of a probability interpretation. NMF is a purely linear algebra way of reorganizing the data. 
I think that nmf works better because it doesn't force a probablity interpretation onto the data, and lets the data "speak for itself." 
However, nmf is then difficult to quantify explain, while LDA provides easy interpretation, such as 
"this term is most likely to occur in this topic." Thus, it makes for a better and more interperatable visualization.

Two ways to view the visualization:

1. Go to the python notebook in the docs section (it ends with .ipynb), and scroll down to the LDA visualization section.

2. First, fork this repo. Then click the below link. Now, click on the screen button (this is to the right of the button that says 
"History," and left of the edit button). This will open the folder containing the file. It does this via github desktop. Now, click on 
"LDA\_viz\_mws" 
This will open the html file in your browser of choice.

[LDA MWS Viz](https://github.com/GU4243-ADS/spring2018-project1-dca2123/blob/master/figs/LDA_viz_mws.html)

#### Installing Python

All data scientists should be at least passingly familiar with python, and should be able to run that code on their computers. Take this as an oppurtunity to become more familiar with the language, and better at collaborating with python coders.

[Click on this link to download anaconda](https://conda.io/docs/user-guide/install/index.html#regular-installation)

Choose the operation system you use, then follow the download instructions. 

I used a Jupyter notebook for my project. Jupyter notebooks also run R notebooks, in addition to python notebooks. They are worth
looking into.

