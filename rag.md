![image](https://github.com/user-attachments/assets/3b5b5a8f-54bb-4271-9c5c-177cd3abff5d)

# Enhanced Product Categorization with Retrieval-Augmented Generation (RAG)

[Github Jupyter Notebook](https://github.com/chloeeliu/LLMs-application/blob/main/Enhanced%20Product%20Categorization%3A%20Leveraging%20RAG%20and%20GPT%20for%20Precision%20and%20Efficiency/rag_revised.ipynb)


![image](https://github.com/user-attachments/assets/da97223a-2fad-499f-90ab-90c07457d00a)




# Outline
- [Introduction](#Introduction)
- [Achievements](#Achievements)
- [Project Development](#ProjectDevelopment)
  - [Traditional_NLP](#Traditional_NLP)
  - [RAG with GPT3.5](#RAG)
- [Challenges](#Challenges_Faces)
  - [Chunk Strategies](#Chunk_Strategies)
  - [Hallucination](#Hallucination)





# Introduction


Project Description: 

This project aimed to revolutionize the way product titles are matched with category trees by integrating NLP techniques with Retrieval-Augmented Generation (RAG).

Objective: 

while analyze competitor’s products, it is neccessary to map the product to the internal categorization, which is crucial for competitor analysis.  

while uploading new product from our supplies, with this enhanced method to find product category can increase the accuracy and efficiency of product information, which are crucial for inventory management.

![image](https://github.com/user-attachments/assets/7bce431f-534b-4b25-83f0-89fcd21fc3f4)



# Achievements


Accuracy: 96%+

- Implemented a hybrid model using Retrieval-Augmented Generation (RAG) and GPT, which surpassed traditional NLP models by 23% in accuracy.
- High Precision Retrieval: Achieved a remarkable 99% accuracy rate in identifying the top 20 candidate sets for product categorization, demonstrating the efficacy of the optimized retrieval process.
- Effective Matching Generation: The use of prompt engineering with GPT resulted in reaching 96% accuracy in matching products to their correct categories.

![image](https://github.com/user-attachments/assets/05858446-9bcc-4cfb-a116-c1fe416caff0)


# ProjectDevelopment

## Traditional_NLP


**Steps:**

- Tokenization and preprocessing. for example, performing stemming or lemmatization.

- IDF Calculation: Calculate the inverse document frequency for each term.

- TF-IDF Calculation:Calculate the TF-IDF score for each term in the product title based on TF and IDF values.

- TF-IDF Vectorization:Construct a TF-IDF vector for the product title based on the calculated TF-IDF scores.

- Cosine Similarity Calculation:Calculate the cosine similarity between the TF-IDF vector of the product title and the category vectors in the hierarchical tree.

- Prediction: Based on the highest cosine similarity score



**Achieve** 80% accuracy in top 5 candidates. Typical badcases fails to capture contextual information of product and category.



## RAG

**Steps:**

- **Indexing:** Construct the hierarchical category tree with jsonl format.


![image](https://github.com/user-attachments/assets/e03ab021-5973-466b-ba0a-e68d043b4c87)

![image](https://github.com/user-attachments/assets/79f93aa4-ff88-4feb-b80a-7b547ab23248)


- **Vectorization:** Employed the text-embedding-3-small model for optimal vector dimensionality to ensure robust and scalable indexing.

![image](https://github.com/user-attachments/assets/fd8e41d8-ac6a-474f-a5f9-eff4496b543d)


- **Retrieval:** Fine-tuned the retrieval algorithms using cosine distance to balance cost and precision effectively.

![image](https://github.com/user-attachments/assets/a48e4c72-215c-4087-ad18-730fc493a42c)


- **Query and Generation:**: Find the most matching category from the candicates by use of the capacity of llms. Significantly lower the hallucination rate by limiting the candidate token quantity.

![image](https://github.com/user-attachments/assets/2eae3375-4e20-4e7a-ace0-a5ffcc118e39)



# Challenges_Faces

## Chunk_Strategies

raise several chunk strategies:

1. use product title as bridge to connect category with new product titles.

2. first, stem and simplify product title only keep main info, then do the step above.

3. directly use category jsonl as chunk then prompt choose from candidate. [ best performance and lowest cost] above

![image](https://github.com/user-attachments/assets/5803e44a-6da3-4833-ba8a-4ffa33be7448)

## Hallucination

In the multi-classification tasks involving long prompts, the language model (e.g., GPT) often generated hallucinated or irrelevant responses. This issue was particularly challenging as it compromised the accuracy and reliability of the product categorization.

Addressing Hallucination: To mitigate this issue, we integrated Retrieval-Augmented Generation (RAG) and utilized cosine similarity measures. This approach helped narrow down the classification candidates, effectively reducing the potential for hallucination by focusing the language model's responses on more probable and relevant categories.



