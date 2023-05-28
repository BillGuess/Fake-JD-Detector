# Fake Job Description Prediction

## Task Goal
* Build a system to predict whether a JD is fake or not (Deep learning solution is better)

## Questions
1. Readme with the following question
    1. How to run your code?
    2. Write down what kind of ML solution will you use for this task.
    3. Why did you choose this solution?
    4. What is your model’s performance?
    5. Briefly describe what's the metrics will you use for the prediction model and why? What number will you set as the baseline?
2. Training model
    - All code you used for training your model (Include how you serialize the model)

## Data
This dataset contains 18K job descriptions out of which about 800 are fake. The data consists of both textual information and meta information about the jobs. The dataset can be used to create classification models which can learn the job descriptions which are fraudulent.

## Files
* [data_observation_splitting.ipynb](data_observation_splitting.ipynb) - data observation and split data to training and validation
* [model_training_validation.ipynb](model_training_validation.ipynb) - build fine-tuned BERT model and validation model
* [Discussions.md](Discussions.md) - a report for task, discussions about this task

## How to Execute on Google Colab
1. Do some prepare on your Google drive
    1. Create folder for dataset, splitted training data, validation data, model
    2. Create folder for testing data, if you want
2. Run ipynb file on Google colab
    1. Don't forget mount your drive on colab
    2. Pay attention to comments in the notebook

## Method
### Used model
A fine-tune BERT model for classification task, classifies job-postings is fake or not
* Observation of data text length (fake-job-postings usually has short text length than 2000) and references, text length and words in text are perhaps key features
* Unbalanced data may cause traditional ML fail, however DL can achieve good by using small data transfer learning

### Metrics
Accuracy, recall, precision are used as metrics to measure performance
* Because of unbalanced data, accuracy may not be of reference value and recall may be more important
* Straightforward metrics are easier to explain and understand

### Baseline
Using company_profile is empty or not to predict as baseline
* Accuracy: 0.83, recall: 0.67, precision: 0.17
* More detail, see [data_observation_splitting.ipynb](data_observation_splitting.ipynb)

### Performance

## References
* [kaggle: Real/Fake Job Posting Prediction](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)
* [進擊的 BERT：NLP 界的巨人之力與遷移學習](https://leemeng.tw/attack_on_bert_transfer_learning_in_nlp.html)
