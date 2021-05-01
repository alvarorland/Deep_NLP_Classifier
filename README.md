Deep NLP Classifier

The Data

Sheet1.csv contains 80 user responses, in the 'responsetext' column The therapy chatbot prompt is 'Describe a time when you have acted as a resource for someone else'. If a response is 'not flagged', the user can continue talking to the bot. If it is 'flagged', the user is referred to help.

Sheet2.csv contains 125 resumes, in the 'resumetext' column. Resumes were queried from Indeed.com with keyword 'data scientist', location 'Vermont'. If a resume is 'not flagged', the applicant can submit a modified resume at a later date. If it is 'flagged', the applicant is invited to interview.

This data is used to identify the variables behind flagged therapy chatbot responses and flagged resume submissions. Flagged chatbot responses result in referring the user to professional mental health help and flagged resumes are invited to interview. 

Deep learning is a category of machine learning models that use multi-layer neural networks. Deep learning is a technique for implementing machine learning. It uses neural networks to learn, sometimes, using decision trees may also be referred to as deep learning, but for the most part deep learning involves the use of neural networks. A neural network is a collection of layers that transform the input in some way to produce an output.


https://www.kaggle.com/samdeeplearning/deepnlp

Methods

Models and Metrics:

This classification problem required a few tweaks to both the models and the metrics. The models built are as follows:

Support Vector Classifier, Random Forest, Gaussian Naive Bayes, Multinomial Naive Bayes, and a Tensorflow Deep Learning model.

This project will be deemed successful for the chatbot responses once a classification model with the highest accuracy possible is built. In this situation, correctly predicting a flagged user response and referring them to help is the goal. For the resume classifier, building a model that has the lowest possible false positive rate would constitute as a success

EDA

Here are a few of the relationships I visualized:

![Screenshot (22)](https://user-images.githubusercontent.com/72377927/116794624-0292f800-aa94-11eb-8d2a-577d6109c3d2.png)

![Screenshot (23)](https://user-images.githubusercontent.com/72377927/116794822-afba4000-aa95-11eb-98ab-43e10cbf2190.png)

![Screenshot (24)](https://user-images.githubusercontent.com/72377927/116794840-dd06ee00-aa95-11eb-9d7e-a9406b12b8e5.png)

![Screenshot (25)](https://user-images.githubusercontent.com/72377927/116794844-ded0b180-aa95-11eb-97e0-d23caa33b6bd.png)


Machine Learning:

![Screenshot (26)](https://user-images.githubusercontent.com/72377927/116795004-43d8d700-aa97-11eb-93b4-71217a4d69de.png)

![Screenshot (27)](https://user-images.githubusercontent.com/72377927/116795014-5b17c480-aa97-11eb-81cc-bf8804fd592a.png)

Results:

The random forest classifier gave the highest accuracy score for the chatbot responses at 0.75, 0.10 more than the multinomial naive bayes classifier. For the resumes, the multinomial naive bayes classifier gave a slightly higher accuracy score than the random forest. 0.72 for multinomial naive bayes and 0.65 for the random forest classifier.

The f1 score and precision score of the chatbot responses are 0.46 and 0.33, respectively for multinomialNB. For the resumes, the multinomialNB f1 score and precision scores are 0.4 and 0.75, respectively. Precision can be thought of as the fraction of positive predictions that actually belong to the positive class. The multinomialNB classifier on the resumes yield a high precision score, close to it's accuracy score. This model is what we're looking for in a resume classifier, a predictor that has a low false positive rate!

Further Research:

Comparing different chatbot prompt responses would give more insight into what responses are flagged or not. Granted, these prompts would have to be similar, in the same vein as the original. An example prompt could be 'Explain a situation where you provided comfort to someone.'

For the resumes, including other jobs in the tech industry would yield a more comprehensive assessment of what employer's look for in a resume when hiring. It would also be interesting to analyze data science resumes over a broader region. This may yield insights into what companies accross this hypotetical region require in a data scientist.
