# Medical Question Pairs (MQP) Dataset

This repository contains a dataset of 3048 similar and dissimilar medical question pairs hand-generated and labeled by Curai's doctors. The dataset is described in detail in [TODO cite paper].

## Methodology
We present our doctors with a list of 1524 patient-asked questions randomly sampled from the publicly available crawl of [HealthTap](https://github.com/durakkerem/Medical-Question-Answer-Datasets). Each question results in one similar and one different pair through the following instructions provided to the labelers:

1. Rewrite the original question in a different way while maintaining the same intent. Restructure the syntax as much as possible and change medical details that would not impact your response.
 e.g. "I'm a 22-y-o female" could become "My 26 year old daughter"
2. Come up with a related but dissimilar question for which the answer to the original question would be WRONG OR IRRELEVANT. Use similar key words.

The first instruction generates a _positive_ question pair (similar) and the second generates a _negative_ question pair (different). With the above instructions, we intentionally frame the task such that positive question pairs can look very different by superficial metrics, and negative question pairs can conversely look very similar. This ensures that the task is not trivial.

## Dataset statistics
The final dataset contains 4567 unique questions. The minimum, maximum, median and average number of tokens in these questions are 4, 81, 20 and 22.675 respectively showing there is reasonable variance in the length of the questions. The shortest question is `Are fibroadenomas malignant?`

An off-the-shelf medical entity recognizer finds around 1000 unique medical entities in the questions. Some of the top entity mentions were: `physician, pregnancy, pain, lasting weeks, menstruation, emotional state, cancer, visual function, headache, bleeding, fever, sexual intercourse`
