---
layout: page
title: Multilingual text analysis of Chinese state media on the Russo-Ukrainian War
description: Comparing traditional China Daily and Global Times
img: https://raw.githubusercontent.com/jyeungtin/jyeungtin.github.io/master/assets/img/sentiment_chart.png
importance: 1
category: Study
---

<img src = "https://raw.githubusercontent.com/jyeungtin/jyeungtin.github.io/master/assets/img/sentiment_chart.png" style="width:100%;">


## Project summary
The study aims to challenge the unitary interpretation of state-controlled media in the field of  political communication to build towards a better typology of state media. If inter-state-media  platform-dependent content variation does exist, new approaches towards studying state media  and the effects of such on society, in China at least, must be sought. Apart from comparing two  outlets, the research aims to investigate the difference based on (1) reporting language, which are English versus Chinese; and (2) platform, which are traditional news site versus social media (i.e.,  Weibo). 

## Methodology
Global Times and China Daily were chosen as the studied subjects due to the difference in their bureaucratic ranks plus their target audience, which is determined by its main reporting language. 

### Weibo-Scraper 
Python was used for the project for data collection cleaning and analyses. 

Various libraries are utilized throughout distinct phases of the project. To collect data from China Daily, a keyword  search using ‘Ukraine’ is conducted. Due to the dynamic page navigation, Selenium is used to 
perform the crawling and click simulation; and to scrape the individual  pages containing news articles. Weibo-Scraper is used to scrape the micro-blogs from the Global times account. Tokenization, stop-word, punctuation, case-specific word removal and named entities recognition are done through SpaCy.

### Rule-based sentiment analysis
A rule-based approach sentiment analysis was adopted using the pre-trained VADER dictionary.  VADER was used as it is one of the most versatile dictionaries that can be applied to various  domains without harming the validity of the results. Despite originally being designed for social  media text analysis, it has offered beyond average performance overall (Ribeiro et al., 2016). Moreover, VADER does not merely count negative and positive words, but that considers the existence of modifiers such as amplifiers, negations, capitalizations and degree modifiers (Hutto & Gilbert, 2014). 

### Multilingual topic modelling

To identify case-specific topics across languages and platform, the paper adjusted the multilingual text analysis strategy designed by Lind et al. (2021) to allow for a quantitative and qualitative comparison across cases and languages. Machine translation approach was first adopted for the Chinese corpus (Lucas et al., 2015) as there is not enough relevant and validated multilingual dictionaries created for this research topic. EasyNMT is used to perform machine translation with Opus-MT from the Helsinki-NLP corpus. Two sub-corpora including a full sub-corpus and a noun-only sub-corpus were then created for each outlet with a view to producing more efficient topic modelling algorithms (Martin and Johnson, 2015). Gensim was used to perform topic modelling with Latent Dirichlet Allocation (LDA, Blei et al., 2003). 

## Results
### Visibility analysis

After data cleaning, 622 micro-blogs are resulted for Global Times and 630 unique articles are resulted for China Daily. According to the visibility analysis, Global Times and China Daily fairly overlaps in their proportional frequency of posts per day between March 13 and April 12. We see clear simultaneous spikes on April 1 and April 6, and a strong overlapping drop on April 10.

### Named entities recognition (NER) ranking

Per the results of named entities recognition, Global Times and China Daily mentioned similar locations and organizations with NATO and EU being the most popular organizations and U.S. the most mentioned location.

### Sentiment analysis

<img src = "https://raw.githubusercontent.com/jyeungtin/jyeungtin.github.io/master/assets/img/sentiment_chart.png" style="width:100%;">

No significant difference in rolling average sentiment scores was found between Global Times and China Daily using a confidence level of 95%. Both outlets fluctuate in a rather similar patterns with sentiment scores floating around neutral to very slightly positive or negative. 

### Topic models: What do they talk about?
LDA was used to conduct the topic modelling. The performance of the default topic models using u_mass and c_v coherence measures. Both measures show that the full corpora performed generally better than the noun-only corpora, thus only the full corpora were kept for  analysis. Consequently, Global Times and China Daily results in 5 and 3 topics respectively, with  only one complete overlap of topic, which is NATO and the West. A face validity check was conducted to ensure the topic labels are applied accurately.

Global Times focus on “hardcore” interactions between the two camps as well as negative news such as specific sanctions and critical diplomatic reactions. China Daily, incongruously, reports more on China’s role in peaceful negotiations and international stability. Although remains negative, the economic consequences are comparatively more general than sanctions, for example the rise in oil and food prices. 

| **Outlet**       | **Suggested topic label**               | **Top Keywords**                                                                          |
|------------------|-----------------------------------------|-------------------------------------------------------------------------------------------|
| **Global Times** | Russo-Ukrainian interaction             | Russian, Ukraine, accord, Russia, Ukrainian, military, time, medium, President, Zelenskyy |
|                  | Sanctions and bans                      | Russia, accord, Russian, gas, report, United, Council, time, local                        |
|                  | China’s talk with Russia                | Russia, China, President, sanction, Russian, Ministry, Foreign, Minister, say, Europe     |
|                  | Global diplomatic reaction              | Russian, Ukrainian, German, Minister, Ukraine, plan, Prime, time, no, local               |
|                  | NATO and the West                       | Ukraine, Japan, Minister, Foreign, say, NATO, weapon, provide, military, Russia           |
| **China Daily**  | China’s role in international stability | Russian, China, Ukrainian, talk, military, President, peace, international, issue, people |
|                  | Economy and market                      | Percent, China, year, price, global, food, market, supply, economy, economic              |
|                  | NATO and the West                       | China, crisis, world, security, military, NATO, EU, sanction, year, relation              |

<br>

### Linking sentiment to topic models 

Two separate topics to sentiment matrices were created to investigate the allocation of positive,  neutral and negative sentiments in relations to the topic. Chi-square tests showed a significant association between topic and sentiment within China Daily, <em>X<sup>2</sup></em> (6, N = 627) = 26.4, p < .001. As for Global Times, results showed a significant association between topic and sentiment, <em>X<sup>2</sup></em> (8, N = 622) = 42.2, p < .001. Some topics are significantly more likely to be positive and vice versa across the outlets.

## Conclusion

In conclusion, the news sentiments of China Daily and Global Times are not more positive or negative than their counterparts. Nevertheless, intriguingly, China Daily and Global Times do differ in their topical interests, which demonstrates the media strategy that the two outlets play complimentary roles, which could be linked back to the dual-path propaganda tactic. China Daily allocated significantly more coverage on China’s constructive role during the war than the coverage of the “evilness” of NATO and the West, whereas Global Times is exactly the opposite. 

Methodically, this study has moderated the topic modelling strategy recommended by Lind et al. (2021) and has successfully made use of a cross-case qualitative-quantitative analysis of topic models. Such approach should be further developed for wider usage. The next step will be expanding the scope of this preliminary study and including more Chinese state media, both traditional news and social media, to provide stronger and more holistic statistical support for the phenomenon of inter-state-media content and platform variation. 

## Interested?

Feel free to contact me to know more about the project details.
