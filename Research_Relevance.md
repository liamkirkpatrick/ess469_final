# Research Relevance
*Here I discuss the broad goals and methods of this project, as part of the CML Assignment*

The primary goal of this work is to improve understanding of the Denali Ice Core water isotope record. My prior work has already established that this record is an effective proxy for precipitation-weighted temperature at the site. However, this metric alone doesn't tell us much. We would like to understand how having a good PWT proxy over the last 1200 years helps us understand reigonal North Pacific climate evolution. Here, I work to produce a regression model which can predict PWT from reanalysis climate data. By developing a model that can predict PWT anomaly from reigonal cliamte, we will be able to gain an understanding of how this proxy relates to climate. This understanding can then be applied to the entire ice core record, providing insights into past climate. 

I propose to use a supervised approach. This is because we have a pretty clear set of training data with a known target. We can compute the PWT from 1970-2022 (the full range of "good" reanalysis data) at the Denali site, and then use other reanalysis fields to try to model this target. This makes an unsupervised approach unsuitable for our goal

This is a regression problem. It certainly would be possible to consider classification problems in this data (parituclarly in identifying modes of varability in the Pacific), but these would not work towards our central goal of understanding PWT. However, in order to directly understand how one variable (PWT at Denali) is impacted by others (

The goal of this work is not so much to develop a prediction algorythim which will be used on future, but to study the model itself. We want to ask qeustions like: which aspects of climate are responsible for driving changes in PWT? Of course, to ask this quiestion, we first have to build an effective model. This repository explores a range of approaches 
