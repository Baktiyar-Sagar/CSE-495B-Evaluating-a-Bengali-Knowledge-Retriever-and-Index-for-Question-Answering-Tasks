![image](https://github.com/user-attachments/assets/1a807445-828b-4cfa-b4fa-d460928b66c6)# Evaluating a Bengali Knowledge Retriever and Index for Question-Answering Tasks

## Description: 

* Bengali Knowledge Retriever that utilizes Retrieval Augmented Generation (RAG). RAG can ensure relatively high answer accuracy when it is paired with tasks such as question answering.
* When a user asks a query, a ColBERT retriever model extracts relevant documents from a Bengali Document Index, which will be used as context documents related to the query. 
* Then any Language Model will be able to factually and accurately answer the query in Bengali using the knowledge from the context documents.

### Dataset Statistics- Retriever Model and Document Index:

* Utilized the Bengali subset of [Mr. TyDi](https://huggingface.co/datasets/castorini/mr-tydi-corpus) Dataset to fine-tune a [pre-trained ColBERT v2 retriever model](https://huggingface.co/colbert-ir/colbertv2.0). 
This fine-tuned ColBERT model will be responsible for retrieving query documents and also used to create the retrieval index (document embeddings)
* Full corpus of Mr. TyDi Bangla set was used to create the index (304k docs). 


### Evalutation Metrics: 

![image](https://github.com/user-attachments/assets/b95d9b25-1edc-4777-abdb-536054429c5a)

![image](https://github.com/user-attachments/assets/438618aa-b8ab-4c29-874e-9d7857f0c8f3)

### Result Analysis:

* Although the results may seem underwhelming at first, if consider the fact that this retrieval result is over Bengali documents and 3.45% of the number of total documents used in ColBERT paper, it becomes clear that it is an outstanding result. 
It also reflects the fact that these results can be improved with more documents which will result in better information retrieval.









