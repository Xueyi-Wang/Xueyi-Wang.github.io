---
title: "Personalized Sleep Prediction via Deep Adaptive Spatiotemporal Modeling and sparse data"
collection: publications
category: conferences
# permalink: /publication/2009-10-01-paper-title-number-1
# excerpt: 'This paper is about the number 1. The number 2 is left for future work.'
date: 2025-06-17
# venue: 'Journal 1'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
# paperurl: 'http://academicpages.github.io/files/paper1.pdf'
# bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
A sleep forecast allows individuals, and healthcare providers to anticipate and proactively address factors influencing restful rest, ultimately improving mental and physical well-being. This work presents an adaptive spatial and temporal model (AdaST-Sleep) for predicting sleep scores. Our proposed model combines convolutional layers to capture spatial feature interactions between multiple features and recurrent neural network layers to handle longer-term temporal dependencies. A domain classifier is further integrated to generalize across different subjects. We conducted several experiments using five input window sizes (3, 5, 7, 9, 11 days) and five predicting window sizes (1, 3, 5, 7, 9 days). Our approach consistently outperformed four baseline models, achieving its lowest RMSE (0.282) with a seven-day input window and a one-day predicting window. Moreover, the method maintained strong performance even when forecasting multiple days into the future, demonstrating its versatility for real-world applications. Visual comparisons reveal that the model accurately tracks both the overall sleep score level and daily fluctuations. These findings prove that the proposed framework provides a robust and adaptable solution for personalized sleep forecasting using sparse data from commercial wearable devices and domain adaptation techniques.
