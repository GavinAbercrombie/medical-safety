# medical-safety

Data from the AACL 2022 paper "Risk-graded Safety for Handling Medical Queries in Conversational AI".

Please cite as:

Gavin Abercrombie and Verena Rieser. 2022. Risk-graded Safety for Handling Medical Queries in Conversational AI. In *Proceedings of The 2nd Conference of the Asia-Pacific Chapter of the Association for Computational Linguistics*. Association for Computational Linguistics.

Bibtex:

@inproceedings{abercrombie-rieser-2022-risk,\
    title = {Risk-graded Safety for Handling Medical Queries in Conversational {AI}},\
    author = {Gavin Abercrombie and Verena Rieser},\
    booktitle = {Proceedings of The 2nd Conference of the Asia-Pacific Chapter of the Association for Computational Linguistics},\
    year = {2022},\
    publisher = "Association for Computational Linguistics"\
}

## Contents

This repo contains the following files:

- data
  - medical-safety-expert.csv: expert labelled data
  - medical-safety-negative.csv: non-medical queries
  
- code
  - medical-safety-convai.ipynb

## Data and labelling scheme

The corpus consists of input queries and output responses (up to three for each query). All of these are labelled by a domain expert annotator and some also have multiple labels provided by crowdworkers.

The file medical-safety-convai.csv contains 1,618 rows with the following fields (the column headers):

| Header                     | Description                                        |
| -------------------------- | -------------------------------------------------- |
| 'query'                    | Input query text                                   |
| 'query-expert'             | Expert label for the query                         |
| 'query-cws'                | List of crowdworker labels for the query           |
| 'alexa-response'           | Alexa response                                     |
| 'alexa-response-expert'    | Expert label for Alexa's response                  |
| 'alexa-response-cws'       | List of crowdworker labels for Alexa's response    |
| 'dialogpt-response'        | DialoGPT response                                  |
| 'dialogpt-response-expert' | Expert label for DialoGPT's response               |
| 'dialogpt-response-cws'    | List of crowdworker labels for DialoGPT's response |
| 'reddit-response'          | Reddit (r/AskDocs) response                        |
| 'reddit-response-expert'   | Expert label for response from Reddit              |
| 'reddit-response-cws'      | List of crowdworker labels for the Reddit response |

For further details, statistics, and a data statement, please see the paper.
