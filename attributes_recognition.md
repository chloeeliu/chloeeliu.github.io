![image](https://github.com/user-attachments/assets/228fa360-19eb-40e6-a876-061c37bdb433)
# Fashion Attributes Extraction for Trend Analysis and Enhance Application with CLIP and Reasoning Captcha

# Outline
- [Introduction](#Introduction)
- [Achievements](#Achievements)
- [Project Development](#ProjectDevelopment)
- [Example Showcase](##ExampleShowcase)
- [Traditional CNN](##Traditional_CNN)
- [Project Development](#ProjectDevelopment)
- [Project Development](#ProjectDevelopment)


# Introduction

**Objective:** To automate the extraction of fashion attributes like sleeve type, waistline, and material from clothing titles and images, facilitating efficient trend analysis.

 

**Background:** Traditional methods using manual annotations to train CNN models for this task resulted in low accuracy (60%) and high costs, both in terms of time and resources.

 
**Solution:** We propose using a multimodal approach with advanced AI models such as GPT, GEMINI, and CLAUDE. This method involves recognizing raw fashion attributes and then accurately mapping them to an internal library using text similarity, aiming to improve accuracy, reduce costs, and accelerate the process.

**Responsibility:** 
- Algorithm role with prompt engineering, few shot designing and agent building. Work closely with senior NLP Algorithm testing and analyzing in python jupyter notebook.

 

# Achievements

![image](https://github.com/user-attachments/assets/c69dad0d-5bf7-4daa-bb6c-b2695c1844be)


**High Accuracy in Attribute Extraction:** Successfully extracted and mapped key product attributes from competitor imagery and titles with prompt engineering, few-shot learning, and supervised fine-tuning, achieving 95% accuracy across 78 different attributes.

**Agent System Integration:** Break down the task and implemented an agent system that coordinated cv, LMMs, Clip models and integrated feedback, which enhanced overall accuracy by an additional 5%.


# ProjectDevelopment

## ExampleShowcase

Fashion attribute recognition requires a comprehensive analysis of the entire image, which includes the background, skin color, lighting, and shadows. These elements are crucial for accurately identifying and understanding the nuances of fashion attributes.

Traditional CNN methods often rely on simplistic feature recognition techniques that disregard these critical elements, resulting in reduced accuracy, especially in complex scenarios.

In contrast, Large Language Models (LLMs) such as GPT-4 demonstrate superior performance in this task. This advanced approach enables a deeper understanding of the image as a whole, significantly improving the identification of fashion attributes.

## Traditional_CNN

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


## LMMs - GPT-4

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
