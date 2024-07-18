

# Enhanced Product Categorization: Leveraging RAG and GPT for Precision and Efficiency




## Introduction

![plot](https://github.com/chloeeliu/LLMs-application/blob/4dbcbd6a6cc1f12e0ee14b5b1098e042c6884fee/image/rag/1.jpg)

Project Description: 

This project aimed to revolutionize the way product titles are matched with category trees by integrating NLP techniques with Retrieval-Augmented Generation (RAG).

Objective: 

while analyze competitor’s products, it is neccessary to map the product to the internal categorization, which is crucial for competitor analysis.  

while uploading new product from our supplies, with this enhanced method to find product category can increase the accuracy and efficiency of product information, which are crucial for inventory management.


## Achievements

![plot](https://github.com/chloeeliu/LLMs-application/blob/4dbcbd6a6cc1f12e0ee14b5b1098e042c6884fee/image/rag/2.jpg)

Accuracy: 96%+

- Implemented a hybrid model using Retrieval-Augmented Generation (RAG) and GPT, which surpassed traditional NLP models by 23% in accuracy.
- High Precision Retrieval: Achieved a remarkable 99% accuracy rate in identifying the top 20 candidate sets for product categorization, demonstrating the efficacy of the optimized retrieval process.
- Effective Matching Generation: The use of prompt engineering with GPT resulted in reaching 96% accuracy in matching products to their correct categories.

## Technologies Used

- Chunk：Construct the hierarchical category tree with jsonl format.

![plot](https://github.com/chloeeliu/LLMs-application/blob/4dbcbd6a6cc1f12e0ee14b5b1098e042c6884fee/image/rag/3.jpg)

- Vectorization: Employed the text-embedding-3-small model for optimal vector dimensionality to ensure robust and scalable indexing.

- Retrieval Optimization: Fine-tuned the retrieval algorithms using cosine distance measures and SVM clustering to balance cost and precision effectively.

![plot](https://github.com/chloeeliu/LLMs-application/blob/4dbcbd6a6cc1f12e0ee14b5b1098e042c6884fee/image/rag/4.jpg)


## Challenges Faces

### Chunk strategies?

raise several chunk strategies:

1. use product title as bridge to connect category with new product titles.

2. first, stem and simplify product title only keep main info, then do the step above.

3. directly use category jsonl as chunk then prompt choose from candidate. [ best performance and lowest cost] above

![plot](https://github.com/chloeeliu/LLMs-application/blob/4dbcbd6a6cc1f12e0ee14b5b1098e042c6884fee/image/rag/5.jpg)

### Hallucination with long prompt?

In the multi-classification tasks involving long prompts, the language model (e.g., GPT) often generated hallucinated or irrelevant responses. This issue was particularly challenging as it compromised the accuracy and reliability of the product categorization.

Addressing Hallucination: To mitigate this issue, we integrated Retrieval-Augmented Generation (RAG) and utilized cosine similarity measures. This approach helped narrow down the classification candidates, effectively reducing the potential for hallucination by focusing the language model's responses on more probable and relevant categories.



 ### Leaf categories not unique?

Only use leaf categories in the prompt while predicting category may influence the accuracy, for the node categories also have some important information for this taks.

Take the artificial flowers as an example, the second level category shows the different occasions for the same leaf category, artificial flowers.


### Groundtruth not unique?

Because a product may belong to multiple categories simultaneously. If the answers are reasonable, both of them are correct.

Example:

White Miniature Jewelry Box, Jewelry Travel Case, Portable Jewelry Organizer For Earrings, Necklaces, Wedding Accessories, Travel Storage
