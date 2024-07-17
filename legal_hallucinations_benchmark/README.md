# Legal Hallucinations Benchmark

## Description
The Legal Hallucinations Benchmark is a dataset created by Dahl et al. as part of a collaboration between Yale Law School and Stanford University for the paper [Large Legal Fictions: Profiling Legal Hallucinations in Large Language Models](https://arxiv.org/abs/2401.01301), subsampled and lightly edited for compatability with Paxton AI. The original, raw dataset published by the authors can be [found on Huggingface.](https://huggingface.co/datasets/reglab/legal_hallucinations)

The Legal Hallucinations Benchmark contains eight task categories, each with 200 question/answer pairs, for a total of 1600 samples. All of these questions were run through Paxton AI's Case Law feature, and the platform's answers are provided in the dataset, along with a GPT-4 evaluation categorizing the answer as one of correct, hallucination, or abstention.

The tasks in detail are:
- Affirm or Reverse: Predicting whether a higher court affirmed or reversed a lower court's decision in a given case.
- Case Existence: Identify whether a given case actually exists in the legal record, for cases that do exist..
- Fake Case Existence: Identical to the above, but with fictitious cases. This tests the AI's ability to recognize and flag non-existent cases, or abstain from answering when it does not know.
- Citation Retrieval: Given the title of a case, retrieve the correct citation with proper formatting.
- Court ID: Identify which court heard a particular case.
- Fake Dissent: Trick questions asking the AI to explain a dissenting opinion from a judge where no such dissenting opinion exists. The correct answer is either to abstain or, in some cases, identify that the judge in question actually affirmed the decision and/or delivered the majority opinion of the court.
- Fake Year Overruled: Trick questions asking the AI to name the year that a given Supreme Court case was overruled for cases that have not been overruled. The correct answer is to say that the case has not been overruled.
- Majority Author: Identify the author of a majority opinion in a given case.

## Published
Published July 18th, 2024.

## Dataset Structure
The dataset contains the following columns:

- task: The task, as described above.
- query: The query provided to Paxton
- answer: The correct answer as provided by Dahl et al.
- paxton_response: Paxton's unedited response to the query.
- is_correct: A binary indicator for whether or not the answer is correct.
- is_hallucination: A binary indicator for whether or not the answer is a hallucination.
- is_abstention: A binary indicator for whether or not the answer is an abstention.

Note that the final three columns will always sum to 1. Each answer must fall into exactly one of those three categories.

## Access
This dataset is available in CSV format and can be downloaded from this repository.
