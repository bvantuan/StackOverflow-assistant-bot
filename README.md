# StackOverflow assistant bot
This repository contains my final project of an online course "Natural Language Processing" [(Coursera)](https://www.coursera.org/learn/language-processing)
organized by National Research University Higher School of Economics [(HSE)](https://www.hse.ru/). The project builds 
a conversational bot that will assist with search on StackOverflow. 

## Overview
The bot will be able to:
* answer programming-related questions (using StackOverflow dataset)
* chit-chat and simulate dialogue on all non programming-related questions
For a chit-chat mode we will use a pre-trained neural network engine available from [ChatterBot](https://github.com/gunthercox/ChatterBot).

## Architecture
* STEP 1 : Perform TF-IDF transformation on texts and StarSpace embeddings on Stack Overflow posts
* STEP 2 : Detect the intent of the user from the question (programming-related questions ou non programming-related questions)
* STEP 3 : Classify programming-related questions. It will predict exactly one tag (=programming language)
* STEP 4 : Find a relevant answer (a thread from StackOverflow) on a question 

## Dataset
* tagged_posts.tsv — StackOverflow posts, tagged with one programming language (positive samples).
* dialogues.tsv — dialogue phrases from movie subtitles (negative samples).

## Results
Chat with the bot: \
Q: Hey \
A: Which is your favourite soccer club? 

Q: How are you doing? \
A: I am doing well. 

Q: What's your hobby? \
A: you act like a child 

Q: How to write a loop in python? \
A: I think its about python \
This thread might help you: https://stackoverflow.com/questions/26736277 

Q: How to delete rows in pandas? \
A: I think its about python \
This thread might help you: https://stackoverflow.com/questions/24612584 

Q: python3 re \
A: I think its about python \
This thread might help you: https://stackoverflow.com/questions/10769394 

Q: What is the difference between c and c++ \
A: I think its about c_cpp \
This thread might help you: https://stackoverflow.com/questions/25180069 

Q: Multithreading in Java \
A: I think its about java \
This thread might help you: https://stackoverflow.com/questions/8318 

Q: Catch exceptions C++ \
A: I think its about c_cpp \
This thread might help you: https://stackoverflow.com/questions/336475 

Q: What is AI? \
A: I think its about java \
This thread might help you: https://stackoverflow.com/questions/8318 

## Repository Files:
* DataProcess.ipynb : Feature engineering
* StarSpace.ipynb : StarSpace embedding
* Model.ipynb : StackOverflow assistant bot

## References
* https://www.coursera.org/learn/language-processing
* https://github.com/gunthercox/ChatterBot
* https://code.google.com/archive/p/word2vec/


