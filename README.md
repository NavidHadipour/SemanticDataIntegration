# Team_21

This project focuses on the core problem of semantic data integration within the University domain. Our objective was to unify diverse, multi-source datasets related to higher education institutions and build a common structure (a mediated schema) capable of answering complex queries across all sources.

Team Information
Team: 21 Members: Sanaz Bayat, Shirin Shoghli, Shahrzad Torabi, Navid Hadipour Limouei

Datasets and Schema
We selected and integrated three key datasets: 
1- Colleges and Universities
2- Dataset National University Rankings
3- University and College Campuses 

These datasets were used to design a Mediated Schema for a unified representation.
The mediated schema consists of three main relations:
Colleges Universities, 
Student, 
Employee 

Competency Questions (CQs)
We developed ten competency questions to capture meaningful information within the domain, such as location, ranking, tuition, and contacts. These questions were formalized using Conjunctive Query (CQ) logic.
Example CQ: Which universities are located in the US?
$Q(\text{Name}) :- \text{Colleges Universities} (\text{Name}, \text{Country}), \text{Country} = \text{"US"}$

Schema Matching & EvaluationWe implemented multiple schema matching techniques and evaluated their performance:

1. Matchers Used String Matchers: Edit Distance Matcher 16and Jaro-Winkler Matcher.Semantic Matcher: Word2vec Matcher.

2. Combining Strategies We combined the results of the matchers using different strategies (Minimum, Maximum, and Average).

3. Best Performing Strategy The Average Strategy showed the best overall performance for our Mediated Schema (MS) against the three Data Sources (DS):

| Datset  | Min-F1 | Max-F1 | Avg-F1 |
| ------- | ------ | ------ | ------ |
| DS1-MS  | 0.6398 | 0.6587 | 0.7768 |
| DS2-MS  | 0.6318 | 0.6646 | 0.7900 |
| DS3-MS  | 0.6776 | 0.7378 | 0.7834 |

4. XML Parsing and Similarity (Task 3)We further evaluated schema matching using XML structures and calculated similarity based on path and node information.

Path Similarity: Evaluated using Jarowinkler similarity on schema paths.
DS1: F1-measure = 0.922
DS2: F1-measure = 1
DS3: F1-measure = 0.75

Node Similarity: Evaluated using Jaccard similarity on schema nodes.
DS1: F1-measure = 0.833
DS2: F1-measure = 0.75
DS3: F1-measure = 0.857

## Evaluation for the participants

| Participant             | T1(_25%_) | T2(_50%_) | T3(_25%_) | Total |
| ----------------------- | --------- | --------- | --------- | ----- |
| Shirin shoghli          | 25%       | 47,50%    | 0%        | 73%   |
| Shahrzad Torabi         | 25%       | 47,50%    | 0%        | 73%   |
| Sanaz bayat             | 25%       | 47,50%    | 0%        | 73%   |
| navid hadipour limouei  | 25%       | 47,50%    | 0%        | 73%   |
