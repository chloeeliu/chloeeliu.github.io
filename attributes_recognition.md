# Fashion Attributes Extraction for Trend Analysis and Enhance Application with CLIP and Reasoning Captcha

![image](https://github.com/user-attachments/assets/23c37e2a-fe5e-42f0-9b3d-abbf0d663920)


# Outline
- [Introduction](#Introduction)
- [Achievements](#Achievements)
- [Project Development](#ProjectDevelopment)
  - [Example Showcase](#ExampleShowcase)
  - [Traditional CNN](#Traditional_CNN)
  - [Project Development](#ProjectDevelopment)
- [Project Development](#ProjectDevelopment)


# Introduction

**Objective:** To automate the extraction of fashion attributes like sleeve type, waistline, and material from clothing titles and images, facilitating efficient trend analysis.

 

**Background:** Traditional methods using manual annotations to train CNN models for this task resulted in low accuracy (60%) and high costs, both in terms of time and resources.

 
**Solution:** We propose using a multimodal approach with advanced AI models such as GPT, GEMINI, and CLAUDE. This method involves recognizing raw fashion attributes and then accurately mapping them to an internal library using text similarity, aiming to improve accuracy, reduce costs, and accelerate the process.

**Responsibility:** 
- Algorithm role with prompt engineering, few shot designing and agent building. Work closely with senior NLP Algorithm testing and analyzing in python jupyter notebook.

 

# Achievements


![image](https://github.com/user-attachments/assets/45fcd05c-fb03-4402-8abb-d7903098bc94)


**High Accuracy in Attribute Extraction:** Successfully extracted and mapped key product attributes from competitor imagery and titles with prompt engineering, few-shot learning, and supervised fine-tuning, achieving 95% accuracy across 78 different attributes.

**Agent System Integration:** Break down the task and implemented an agent system that coordinated cv, LMMs, Clip models and integrated feedback, which enhanced overall accuracy by an additional 5%.


# ProjectDevelopment

## ExampleShowcase

![image](https://github.com/user-attachments/assets/205c1f38-5525-44f3-87d2-7879673c763b)

Fashion attribute recognition requires a comprehensive analysis of the entire image, which includes the background, skin color, lighting, and shadows. These elements are crucial for accurately identifying and understanding the nuances of fashion attributes.

Traditional CNN methods often rely on simplistic feature recognition techniques that disregard these critical elements, resulting in reduced accuracy, especially in complex scenarios.

In contrast, Large Language Models (LLMs) such as GPT-4 demonstrate superior performance in this task. This advanced approach enables a deeper understanding of the image as a whole, significantly improving the identification of fashion attributes.

## Traditional_CNN

![image](https://github.com/user-attachments/assets/93520b7d-8e36-4091-bbbf-b5988af0cb0d)


**Steps:**
- Manual Annotation: Annotating images with bounding boxes to delineate features about 50,000.
- Main Part Recognition: The model identifies core elements bounding box, such as the upper and lower garments, shoes, and accessories.
- Training a Multi-label Classification CNN Model: The model is trained to classify multiple attributes simultaneously. The performance metrics are **Precision, Recall, and F1 score, which are 0.7453, 0.8344, and 0.7874**, respectively.

**Pros and Cons:**
**Pros:**
- Capable of mapping attributes to an internal attribute library, allowing for structured data organization.

**Cons:**
- High annotation cost
- Lower accuracy. This is especially true for distinguishing finer detail attributes, as the model doesn't effectively learn the characteristic features of these attributes.


## LMMs - GPT-4 & Gemini

 ![image](https://github.com/user-attachments/assets/6a20d664-6956-4910-ae09-35ae5ac45f1e)


**Steps:**
- Provide Input: The input consists of images and titles (to identify the main subject) along with prompts. (Insert prompts and example outputs here.)

- Textual Mapping: The model maps the provided text to understand and categorize the attributes.

**Pros and Cons:**
**Pros:**
- Highly versatile, accurate and  rapid in processing inputs.

**Cons:**

- Hallucination: The model might generate plausible but incorrect information based on the prompt.

- Specialized Domain Knowledge: GPT-4 might not be aware of domain-specific concepts. For example, the term "2 in 1" is a common style in fashion known as a false two-piece, which the model might not accurately understand.

- Direct Naming Issue: The model cannot directly return internally defined attribute names specific to a company. Instead, it necessitates text matching to correlate its outputs with the company’s specific attribute lexicon.


# Enhancing Application

## 4.1 Application of CLIP in Search Keyword Trend Analysis

![image](https://github.com/user-attachments/assets/f663b4b3-5965-45e1-9066-3bf00053bd61)


**Steps:**

- Deploy Open-source CLIP: Begin with deploying the open-source version of CLIP (Contrastive Language–Image Pre-training).
- Fine-Tuning the Model: Next, adjust and optimize the model by using an internal dataset of product titles and images as encoding pairs.
- Embedding Millions of Products: Create embeddings for millions of products to facilitate detailed analyses and comparisons.
- Engineering Pipeline Construction: Build an engineering framework that allows users to input text queries and retrieves similar products based on their search.



**Achievement:**

- AB Testing Validation: Conducted AB tests to validate the model's product selections, resulting in a 2.5% higher exposure rate compared to the general market during the same period.

<img width="1489" alt="image" src="https://github.com/user-attachments/assets/8f20cf2a-3ac1-48e3-846c-4ce86aac98db">



## 4.2 Break down Captcha with GPT4 Azure OCR Enhancement

![image](https://github.com/user-attachments/assets/98694f6c-af70-4d97-bba5-9b08028ecf9b)


**Steps:**
- Enable Azure GPT-4 OCR Enhancement: Initiate the process by activating the GPT-4 OCR enhancement feature in Azure.

- Apply Coordinate Grid to Captcha: Add a coordinate grid overlay to the Captcha image for precise identification.

- For the solution:

  - First GPT-4 Call for Logic Questions: Make the initial call to GPT-4 asking logic-based questions, such as "What is the lowercase letter corresponding to the yellow letter?". The response might be: "A lowercase letter 'a' in green."

  - Second GPT-4 Call for Bounding Box: The next call to GPT-4 requests the bounding box of the identified "green lowercase a".

`Please detect and locate the green lowercase d  letter present in the provided image successfully. 
Return its bounding box coordinate. Provide the results in the following format:

{"bbox": [x_min, y_min, x_max, y_max]}

Where:
- the image size is (327, 164)
- x_min, y_min are the coordinates of the top-left corner of the green lowercase d  bounding box
- x_max, y_max are the coordinates of the bottom-right corner of the green lowercase d  bounding box

The bounding box coordinates should be in pixels, with (0, 0) representing the top-left corner of the image and (326, 163) representing the bottom-right corner.

Additionally, if there are any characters that are partially obscured or difficult to recognize with certainty, please include them in the results with your best estimate of the character.`

  - Calculate Bounding Box Centroid: Determine the centroid of the bounding box coordinates to guide the user interface for the correct click response.

**Achievement:**

Average 87% accuracy in breaking down captcha within five try.
![image](https://github.com/user-attachments/assets/6ee7cc91-b638-4b25-8800-c5941fe97c2a)
