# BERT for Question Answering
## BERT-QuestionAnsweringSQuAD
In the notebook __BERT-QuestionAnsweringSQuAD.ipynb__ I fine tuned BERT for Question Answering on SQuAD. I used the BertForQuestionAnswering model.

For evaluation I used the official evaluation script for SQuAD.

### Results
Some tests:

![image](https://user-images.githubusercontent.com/60042402/167939414-81ee40c3-5fa4-4c8c-bb45-66f57a00677a.png)

The best results were for learning rate 2e-5. From the evaluation script I got:

![image](https://user-images.githubusercontent.com/60042402/167939465-ff44d4ab-a09f-43c4-aa41-98ed1fc95421.png)

![image](https://user-images.githubusercontent.com/60042402/167939509-29e23dc8-f59f-43de-a860-cfc5dcc5aefb.png)

Diagrams 3&4 show the possibilities that the model predicts that a queston will be inanswerable or not fot the questions which don't have answer and for the questions that hava answer.

## CrossEvaluation (Based on the paper "What do Models Learn from Question Answering Datasets?")
In the notebook __CrossEvaluation.ipynb__ I converted the triviaQA dataset to SQuAD format so that I can test fine-tuning BERT on SQuAD and evaluating it on TriviaQA and fine-tuning BERT on TriviaQA and evaluating it on SQuAD. Here, I used distilbert instead of bert because the TriviaQA dataset has larger texts and the training would be very slow. According to distilbert documentation, it is 40% faster and 97% as good in natural language understanding as bert.

### Results
![image](https://user-images.githubusercontent.com/60042402/167942268-8e305f2f-b90d-4db3-98e1-63701496029e.png)

