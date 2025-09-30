# Application of Evidence-based Claim Verification with Commonsense Knowledge and Temporal Information

This organization includes all repositories needed to run fact-checking application based on Evidence-based Claim Verification with Commonsense Knowledge and Temporal Information thesis.
* The term "fact checking" is less accurate than "claim verification". By definition, "fact" is true by nature.
* However, other groups, especially those who don't focus on this field, are more familiar with the term "fact-checking".


## Modules
The application consists of several modules. Below is the holistic view of the application.


![System Diagram](https://github.com/thesis-anab/.github/blob/main/profile/system_diagram.png)

* [FrontEnd](https://github.com/thesis-anab/claim_verif_frontend): contains repo to the frontend application. 
* [ChronoFact Module](https://github.com/thesis-anab/claim_verif_system): contains repo to the ChronoFact module. This module provides API that takes `claim` as input, and perform the complete verification process to the claim.
* [CGAT Module](https://github.com/thesis-anab/cgat-verifier): contains repo to the CGAT verification module. This module provides API that takes `claim` and `top_k_sentences` and perform commonsense claim verification process.
* [Event Extraction Module](https://github.com/thesis-anab/event-extraction): contains repo that provides API that takes `sentences` as input and perform extract events from the sentences.
* [TACV Sentence Selection Module](https://github.com/thesis-anab/TACV-retrieval): contains repo to the TACV retrieval module. This module provides API that takes `claim` and `top_k_docs` as input, and perform sentence selection (read all sentences from the docs and retrieve top-k relevant sentences) to the claim.
* [Document Retrieval Module](https://github.com/thesis-anab/GENRE_Feverous_DocRet): contains repo to the Document Retrieval module. This module provides API that takes `claim` as input, and perform retrieval to extract top-k relevant documents to the claim.
* [OpenAI Caller Module]: contains repo that acts as helper. It provides API that takes prompt as input, and return generated output from LLM.

## Sequence Diagram
The picture below highlight the process on how each modules interact with each other.


![System Sequence Diagram](https://github.com/thesis-anab/.github/blob/main/profile/system_sequence_diagram_white.png)
