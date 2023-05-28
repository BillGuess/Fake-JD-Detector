# Discussions about this task
## Bottlenecks
### Maximum length in number of tokens
The first bottlenecks I had met, long text will cause error
* I just let max_length fixed in this task
* A more effective approach should be improved from feature engineering, like filter URL, it need more referrnces
  * [BERT: How to Handle Long Documents](https://www.saltdatalabs.com/blog/bert-how-to-handle-long-documents)
  * [How to Fine-Tune BERT for Text Classification?](https://arxiv.org/abs/1905.05583)

### Computing resource
Computing resources limit the size of each training data
* I limited batch size and used smaple data, than increased runs of training

## Ideas for improvement performance
Here I has some idea to improvement performance
### More complex loss function
* The loss function I used is only consider accuracy
* Recall, precision, text similarity should be considered

### Add other features
* Add categorical flag like "company_profile_null" to input text, let the fake-job-posting text with same pattern

### A hybrid model combine ML and DL
* Add a fully connected layer with input are feature and text embedding
![image](https://github.com/BillGuess/Fake-JD-Detector/assets/87471415/e967f36c-65cd-4bc5-b71e-bf37d505dc29)


## What I learned in this task
In order to do this task, I also learned a lot of knowledge
### Transformer
### Self-attention
## Design a framework for production
![image](https://github.com/BillGuess/Fake-JD-Detector/assets/87471415/1941eb89-49e8-4b94-ad67-9058a2350b79)

## References
* [BERT: How to Handle Long Documents](https://www.saltdatalabs.com/blog/bert-how-to-handle-long-documents)
* [How to Fine-Tune BERT for Text Classification?](https://arxiv.org/abs/1905.05583)
