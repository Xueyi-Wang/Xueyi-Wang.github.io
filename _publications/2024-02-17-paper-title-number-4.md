---
title: "Fall detection with a nonintrusive and first-person vision approach"
collection: publications
category: manuscripts
permalink: /publication/2024-02-17-paper-title-number-4
excerpt: 'This paper is about fixing template issue #693.'
date: 2023-09-19
# venue: 'GitHub Journal of Bugs'
# paperurl: 'http://academicpages.github.io/files/paper3.pdf'
# citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---
Falls have been widely recognized as one of the most dangerous incidents for the elderly and other people with mobility limitations. This problem has attracted wide scientific interest, which has led to several investigations based on nonvision wearable sensors and static cameras. We investigate the challenge of fall detection and recognition using egocentric wearable cameras, which, besides portability and affordability, capture visual information that can be further leveraged for a broad set of lifelogging applications. In this work, five volunteers were equipped with two cameras each, one attached to the neck and the other to the waist. They were asked to simulate four kinds of falls and nine types of nonfalls. The newly collected dataset consists of 5858 short video clips, which we make available online. The proposed approach is a late fusion methodology that combines spatial and motion descriptors along with deep features extracted by a pretrained convolutional neural network. For the spatial and deep features, we consider the similarity of such features between frames in regular intervals of a given time window. In this way, it is the transition between such frames that are encoded in our approach, while the actual scene content does not play a role. We design several experiments to investigate the best camera location and performance for indoor and outdoor activities and employ leave-one-subject-out cross-validation to test the generalization ability of our approach. For the fall detection (i.e., two-class) problem, our approach achieves 91.8% accuracy, 93.6% sensitivity, and 89.2% specificity.
