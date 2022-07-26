# Documentation for Umigon

Umigon is a free application for sentiment analysis available as a [web app and as an API here](https://nocodefunctions.com/umigon/sentiment_analysis_tool.html).

This repository contains the documentation for Umigon.

# Overview of the coding architecture

Click on any blue box to get to the repo and get more details (coming soon).

![a description of the sub-projects composing Umigon](https://docs.google.com/drawings/d/e/2PACX-1vQDDpnqjIxHu0u0_Xu0ozKdANNlYBLvdIVEy3ESIoQU8lBpswpZQmR1uVzP6QKERl8L0_N0nVnhPXYw/pub?w=627&h=465)

Here is the overview:

① Definitions are important. umigon-model describes a data model that allows to manipulate precisely different parts of a text: words, puncutation, emojis, emoticons, hashtags and more.

 ② Once we have these essential definitions, we can tokenize a text. This means breaking a text into meaningful segments, such as words but not only.

 ③ Then, we identify the ngrams in the text. An ngram is a fragment of text composed of several words. We know "United" and "States" are in the text, but thanks to this step we will also have "United States".

 ④ This repository gathers heuristics. A heuristic is a rule that will be applied whenever a word is found in the text. For instance, a heuristics says that "AWFUL" carries a negative sentiment (it is a bit more complicated but you get the idea).

 ⑤ This repo is called "core" because this is where the projects 1, 2, 3 and 4 get leveraged to analyze the sentiment of a text. The text is tokenized, ngrams are added to it, and then heuristics are applied to each fragment. We get the sentiment of the text

 ⑥ Sometimes, several conflictual sentiments are found in a text, even if the short texts that Umigon is specializing in (tweets, social media posts or comments...). This repo applies a series of decisions to arbitrate and arrive at a final, single sentiment.

 ⑦ In the preceding steps (2 to 6), all the  procedures that were applied and all the information that got extracted is carefully stored according to the data model (1). This repo conducts a translation from the to data model to a language humans (end users) can understand and appreciate.

⑧ The repo containing the documentation for Umigon, such as this document.
