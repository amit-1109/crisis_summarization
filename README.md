# Crisis Events  Summarization with BM25 and DFReeKLIM
This repository maintain the code used in the experiments reported in the proceeding paper "Facts Summarization at the TREC 2023: IIT(BHU) in CrisisFACTs Track", accepted for publication at The Thirty-Second Text REtrieval Conference (TREC 2023).

# Abstract: 
The CrisisFACTS Track tackles the challenges of gathering crucial facts from diverse disaster-related events through multi-stream fact-finding. This paper presents our innovative method for summarizing crisis events in the TREC 2023 CrisisFACTS track. Our approach involves a two-step summarization process utilizing retrieval and ranking techniques. Initially, a sparse retrieval framework treats content from various online streams as a document corpus. It uses term matching to retrieve relevant contents, termed “facts”, based on specific event day queries. Subsequently, pre-trained models assess the semantic similarity between query-fact and fact-fact pairs. These similarities are used to score and rank the facts, forming the basis for extracting daily event summaries. Relevant data are first retrieved using the IR technique from pyTerrier and then re-ranked. Top-k (k=32) posts are finally used to create summaries. Our model is not able to create good summaries for the event on a specific day. But We are confident that this approach holds potential for yielding promising results with “BM25 + DFReeKLIM” model, especially for labels with limited resources.

# Approach
We use BM25 + DFReeKLIM for document retrieval and re-ranking and use the top-k documents to generate relevant facts from social media posts and online news sources guided by the user's interest.

![Proposed_Method](https://github.com/amit-1109/crisis_summarization/assets/160917360/a3912f07-b89c-4c9e-ab88-60ae89ce4f8a)

# Reproducing
For generating facts, run this notebook: CrsisFACTS.ipynb
See CrisisFACTS utilities repository for getting evaluation code: github.com/crisisfacts/utilities

# How to cite
  @misc{irlabiitbhu,
    author = {Amit Yadav, Sukomal Pal},
    title = {Facts Summarization at the TREC 2023: IIT(BHU) in CrisisFACTs Track},
    year = {2023}
  }
