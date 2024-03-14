---
layout: page
title: Auditing Cantonese GPT
description: Fairness, Accountability and Transparency in Machine Learning (FAccT)
img: https://media.licdn.com/dms/image/D5612AQG8OZj2KQEQtg/article-cover_image-shrink_720_1280/0/1694623029215?e=2147483647&v=beta&t=DwGrBLpQS7BA7eYSvw3T2NTNCXjAzw8l86KSTQTb77A
importance: 1
category: Study
---

## Project summary
Migration, trade and terrorism networks are centre to research efforts in the past decades and each of them have received a considerable amount of attention in their specific domains. However, little work has been done to understand the dynamics between these networks, particularly how temporal growth of one network may induce shocks in another. In this work, we examine how we can leverage techniques in multiplex, temporal networks to disentangle global trends of migration, trade and terrorism from 1990 to 2020. 

### Supervisor 

This project is conducted under the Oxford Internet Institute and taught by Dr. Ana Valdivia and Dr. Luc Rocher.

### Software

Python, OpenAI API

## Current progress

You can find the project page on [GitHub](https://github.com/jyeungtin/CANTGPT).

### Why Cantonese?

Notwithstanding the potential biases in LLMs, the model engineers are actively developing de-biasing tools and safety guardrailing frameworks. These LLM guardrails are designed to prevent usage of LLMs for malicious intents. However, the performance of guardrails differ across languages. In a study of jailbreaking with User Prompt Injection Attack (UPIA) in GPT-4, it was revealed that attacks with low-resource languages (LRL) can constantly bypass guardrails (~79%), meanwhile high-resource languages (HRL) are more robust against UPIA with a success rate of only 11% (Yong et al., 2024). Now, despite that Simplified Mandarin (zh-CN) and Taiwanese Mandarin (zh-TW) are considered as high-resource languages, it is rather ambiguous whether Cantonese (ISO 639-3: Yue) falls under this category. This is due to fact that although Cantonese uses the traditional Chinese characters, similar to zh-TW, they have unique words that are not present in Chinese and Taiwanese Mandarin. For example, 這個是甚麼? (What is this?) is almost entirely different in Cantonese, that is 呢嗰喺咩嚟. Coupled with the spoken nature of the Cantonese, and thus its ambiguous sufficiency in the training data, the resource level of Cantonese is yet to be known. Considering paucity of LLM research on Cantonese, this study sets out to understand the landscape of biases in a language that is used by more than 80 millions - more than Italian!