# Deep Vision AI assignment
# Word Sense Disambiguation
### "Replicating" the research paper and understanding the key features

Paper: https://arxiv.org/pdf/1908.07245.pdf
Code: https://github.com/HSLCY/GlossBERT
## Introduction
Here, I would like to explain my understanding of the key features and details about how the Gloss+Bert makes sense out of the text and gets the context of the specific word which is given to the model.
Understanding the Sentence/Word’s context with the rest of the sentence plays a very key role in many of the NLP tasks, where one of the major use cases is also in the field of Aspect Based sentiment analysis where we can get the sentiment of the target word which is being used.
In this paper, they have explained how they have used the help of WordNet along with obtaining the senses of the words and later training them with BERT, and how they have improved from the previous implementation of the Bi-LSTM approach which was mostly like a sentence labeling task. 

## Business Problem
In cases where the organization has text-based data where they need context-based need.
For the problem of the reviews dataset where the company might need the context of the product that the consumer might be speaking about that particular product.

## Model Used
GlossBERT(Sent-CLS-WS) We use context gloss pairs with weak supervision as input. We take the final hidden state of the first token [CLS] and add a classification layer (label ∈ {yes, no}), which weakly highlights the target word by the weak supervision.
Like : 

![alt text](https://github.com/arulpraveent/NLP_Task/blob/Rupesh_Malla/Screenshot%202022-10-30%20at%207.54.33%20PM.png)


## The approximate pipeline of the entire notebook


![alt text](https://github.com/arulpraveent/NLP_Task/blob/Rupesh_Malla/Screenshot%202022-10-30%20at%208.13.58%20PM.png)

## Improvements that can be made in my submission: 
1. The use of more data for training would definitely improve the performance where I have used only 1000 and later 10000 data points due to lack of GPU power in kaggle kernel after my Google Collab’s free credit GPU expired
2. Incorporating other recently released models like Roberta and other newer models into modeling 
3. Use of additional layers/models on top of the core BERT-based models 
4. Using text preprocessing and cleaning methods for the input data while deploying
5. Reducing the complexities of all the redundant functions and using some of the built-in tools which have been recently released rather than building them like the truncate function in my notebook.

# Results 

Here with different meanings of the word " Play" my model understands the meaning in all the instances and shows the results accurately

![alt text](https://github.com/arulpraveent/NLP_Task/blob/Rupesh_Malla/Screenshot%202022-10-30%20at%208.03.30%20PM.png)


