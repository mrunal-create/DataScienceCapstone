# DataScienceCapstone

## Introduction:
Mental health issues are often misunderstood or not fully grasped by the general public. This lack of understanding can lead to fear, discomfort, and negative perceptions about mental health conditions. Media portrayals of mental health often perpetuate negative stereotypes, leading to misconceptions and fear. Overcoming mental health stigma requires a multi-faceted approach that involves education, raising awareness, promoting empathy and understanding, challenging stereotypes, and ensuring accessible and quality mental health care. Mental health directly impacts an individual's overall well-being, quality of life, and ability to function effectively in daily life. Good mental health is essential for experiencing happiness, fulfilment, and a sense of purpose. Mental health and physical health are closely intertwined. Untreated mental health issues can lead to or worsen physical health problems, such as cardiovascular diseases, weakened immune systems, and chronic conditions.

## Core Rationale:
Chatbots offer a readily available and accessible platform for individuals seeking support. They can be accessed anytime and anywhere, providing immediate assistance to those in need. Chatbots can offer empathetic and non-judgmental responses, providing emotional support to users. While they cannot replace human interaction entirely, they can be a helpful supplement, especially in moments of distress.

## Dataset 
The dataset was curated from online FAQs related to mental health, popular healthcare blogs like WebMD, Mayo Clinic and Healthline, and other wiki articles related to mental health. 

## Model Finetuning:
This is the major step in the entire project. I have used Gemma 2B pre-trained model and finetuned it to using the QLoRA technique on my custom mental health dataset. The entire finetuning process took less than an hour and it was finetuned entirely on Nvidia A100 from Google Colab Pro. But, it could also be trained on free-tier GPU using Nvidia T4 provided by Colab. In that case, we have to ensure to use max_steps less than 150. 

NOTE: Try changing hyperparameters in TrainingArguments and LoraConfig based on your requirements. With the settings mentioned in notebook, I achieved 0.031 training loss after 100 steps.
