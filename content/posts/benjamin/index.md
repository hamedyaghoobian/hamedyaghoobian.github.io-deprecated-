
---
title: A Peek Into Correspondences of Walter Benjamin Using BERT
toc: false
share: false
---

Note: _This research was conducted over a span of 4 weeks in Summer 2022 with Muhlenberg undergraduate student researcher, Christian Johansson._

# Introduction
Walter Benjamin, a renowned German philosopher and critical theorist (1892-1940), is celebrated for his prolific letter-writing. His letters, which were later compiled into a book titled "The Correspondence of Walter Benjamin, 1910-1940" [1], provide a rich resource for exploring the writer's evolving thoughts and emotions over time. In this study, we aim to leverage advanced computational frameworks, particularly large pretrained language models, to gain deeper insights into these letters.

Digital humanities has seen a growing interest in the use of language models for its ability to efficiently process large amounts of data, saving time and resources for researchers. Additionally, computational tools can offer a fresh perspective on research questions, yielding new discoveries and insights.

# Methods and Approach
We started by constructing a dataset of Walter Benjamin's letters, which was manually created from the compiled letters in PDF format. The dataset was represented in a tabular form, with attributes such as recipient, date, and content, and exported as a CSV file.

We then employed BERT (Bidirectional Encoder Representations from Transformers), a widely-used pretrained language model developed by Google, to perform topic and emotion analysis on the letters. Our analysis involved cleaning and preprocessing the data from the CSV file and feeding it into the BERT model.

# Data and Results
## Topic Modeling using BERT
The topic analysis of Walter Benjamin's letters revealed several recurring themes, such as time, letters, knowledge, work, books, Paris, and things, which align well with the philosopher's known interests and concerns. It is important to note that the themes identified by the BERT model are determined by prevalence rather than context specificity.

{{< figure src="recipients_emotion_dist.png" caption="Recipients Emotion Distibution Across Letters" theme="light" >}}
{{< figure src="emotions_year_dist.png" caption="Recipients Emotion Distibution Across Years" theme="light" >}}

## Emotion Analysis using BERT
To perform emotion analysis, we fine-tuned the DistilBERT model using the Emotion dataset, a collection of English tweets annotated with six basic emotions: anger, fear, joy, love, sadness, and surprise. The fine-tuned model was then applied to Walter Benjamin's letters, revealing a dominance of the "joy" class throughout his life, with a slight increase in the last decade. The model also categorizes letters originating from Poland as "sad."

It is important to acknowledge the limitations of current emotion recognition models, which may not accurately capture the complex emotions expressed in written text. Further refinement of the models and data used may be required to arrive at more robust results.


# References
[1] The Correspondence of Walter Benjamin, 1910-1940. Edited by Rolf Tiedemann. Translated by Edmund Jephcott. Chicago: University of Chicago Press, 1996.

