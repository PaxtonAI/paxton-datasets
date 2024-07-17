# Citator Benchmark

## Description
The Citator Benchmark is an attorney-reviewed dataset containing pairs of citing and cited legal cases along with the "status" of the Cited Case given the way the Citing Case has treated it. Each record was developed by selecting a piece of caselaw, finding one of its citing cases, and having an attorney review the cases to determine the treatment of the Cited Case by the Citing Case. The relationships are classified as "cautionary" or "likely good," reflecting the potential reliability of the Cited Case.

## Published
Published June 29th, 2024.

## Dataset Structure
The dataset contains the following columns:

- cited_case_name: Name of the case whose status is being evaluated.
- cited_case_citation: Citation of the cited case.
- citing_case_name: Name of the citing case.
- citing_case_citation: Citation of the citing case.
- label: The label chosen by the attorney for the status of the Cited Case given the Citing Case.
- paxton_classification: The status of the Cited Case given the Citing Case determined by Paxton.
- paxton_reasoning: Explanation or rationale provided by Paxton's AI regarding its classification.


## Access
This dataset is available in CSV format and can be downloaded from this repository.
