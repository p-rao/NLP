# CSE 635 Natural Language Processing (NLP)
Final Project for CSE 635 NLP - Social Media Mining for Health Monitoring

Social media is a popular medium for the public to voice their opinions and thoughts on
various health related topics. A recent Pew Research Center study says that nearly half of
adults worldwide and two-thirds of all American adults use social networking on a regular
basis. Due to the wealth of data available, researchers have been analyzing social media data
for health monitoring and surveillance. However, social media mining for health issues is
fraught with many linguistic variations and semantic complexities in terms of the various
ways people express medication-related concepts and outcomes. This project requires
processing imbalanced, noisy, real-world, and substantially creative language expressions
from social media to extract and classify mentions of adverse drug reactions (ADRs) in
tweets.

There are 4 tasks involved in this project:
# Task 1: Automatic classification of adverse effects mentions in tweets
Classify the tweets reporting an adverse effect (AE) from those that do not. For each tweet,
the data set contains: (i) the user ID, (ii) the tweet ID, and (iii) the binary annotation
indicating the presence or absence of ADRs.
Dataset:
Training data: 25,672 (2,374 positive and 23,298 negative)
Evaluation data: approximately 5,000 tweets.
Evaluation metric: F-score for the ADR/positive class.
Link: https://data.mendeley.com/datasets/rxwfb3tysd/2/files/d2ae709b-c21e-420a-8de8-8b0f3abcfafe

# Task 2: Extraction of Adverse Effect mentions
Identify the text span of the reported ADRs and distinguish ADRs from similar non-ADR
expressions. ADRs are multi-token, descriptive, expressions, so this subtask requires
advanced named entity recognition (NER) approaches. The data for this sub-task includes
2000+ tweets which are fully annotated for mentions of ADRs and Indications. This set
contains a subset of the tweets from Task 1 tagged as hasADR plus an equal number of
noADR tweets. Some tweets in the noADR subset were annotated for mentions of
Indications to allow students to develop techniques to deal with this confusion class.
For each tweet, the data set contains: (i) the tweet ID, (ii) the start and (iii) end of the span,
(iv) the annotation indicating an ADR or not and (v) the text covered by the span in the
tweet.
Dataset:
Training data: 2,367 (1,212 positive and 1,155 negative)
Evaluation data: 1,000 (~500 positive, ~500 negative)
Evaluation metric: Strict and Relaxed F1-score, Precision and Recall
Link: https://data.mendeley.com/datasets/rxwfb3tysd/2/files/bc16c731-36b9-40fc-bfee-242495f7f139

# Task 3: Normalization of adverse drug reaction mentions (ADR)
This is an end-to-end task, where the objective is to detect tweets mentioning an ADR and to
map the extracted colloquial mentions of ADRs in the tweets to standard concept IDs in the
MedDRA vocabulary (lower level terms). MedDRA (Medical Dictionary for Regulatory
Activities) is the standard nomenclature for monitoring medical products, and includes
diseases, disorders, signs, symptoms, adverse events or adverse drug reactions.
This task requires to understand the semantic interpretation of ADRs in order to map them to
standard concept IDs. This task is likely to require a semi-supervised approach to
successfully disambiguate ADRs. For each ADR mention, the publicly available data set
contains: (i) the tweet ID, (ii) the start and (iii) end of the span, (iv) the annotation indicating
an ADR or not, (v) the text covered by the span in the tweet and (iii) the corresponding ID of
the preferred term in the MedDRA vocabulary.
Dataset:
Training data: 2,367 (1,212 positive and 1,155 negative)
Evaluation data: 1,000 (~500 positive, ~500 negative)
Evaluation metric: Strict and Relaxed F1-score, Precision and Recall
Link: https://data.mendeley.com/datasets/rxwfb3tysd/2/files/1959c8c0-1538-4bfe-96d6-d1bb84dc6a70

# Task 4: Live Demonstration of an end-to-end system
Following up on the above tasks, students are required to build a website demonstrating an
end-to-end system of ADR mentions in the tweets in the class. You are required to highlight
the text span of ADR mentions/indications, annotation indicating ADR or not and overall
sentiment of the tweet. In addition to using evaluation data as the data source for your
website, you are also required to ingest more tweets on health-related topics.
Reference: https://www.aclweb.org/anthology/W19-3203.pdf

https://healthlanguageprocessing.org/smm4h/
