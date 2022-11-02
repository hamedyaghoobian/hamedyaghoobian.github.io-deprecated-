
---
title: A Peek Into Correspondences of Walter Benjamin Using BERT
toc: false
share: false
---





Note: _This research was conducted over a span of 4 weeks in Summer 2022 with Muhlenberg undergraduate student researcher, Christian Johansson._

# Introduction
German philosopher and critical theorist Walter Benjamin (1892-1940) was famously known for his avid letter writing habit. The surviving letters were compiled in a book The Correspondence of Walter Benjamin, 1910-1940 by the University of Chicago Press. Through the use of large pretrained language models, we analyzed these letters to arrive at more contextual representations. This is to showcase how advanced computational frameworks can be used in fields of social science and humanities to gain additional insights, or validation. Language models have the advantage of being able to process large amounts of data quickly. This can save on academic research time especially when dealing with large bodies of work or entire literary works of authors. Computational tools can be used toward arriving at bigger and more meaningful research questions. 


# Methods and Approach
We first constructed a tabular dataset of his letters to various correspondents, with various attributes. This was done by manually filling a spreadsheet from his compiled letters PDF as the encoding was to poorly done to port by code. The sheet was then exporting as a CSV file. Then, using Google’s Bidirectional Encoder Representations from Transformers (BERT), a Pre-trained Language Model, we analyzed the evolution of topics and emotions represented in these documents over time. This was accomplished by writing code that took data from our CSV file, cleaned it and fed to the models. 






