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
* Even so, it took over an hour to train model

## Ideas for improvement performance
Here I has some idea to improvement performance
### strategy for Sampling training data
* Over sampling or down sampling
* Ensure every sampling including minor class

### More complex loss function
* The loss function I used is only consider accuracy
* Recall, precision, text similarity should be considered

### Add other features
* Add categorical flag like "company_profile_null" to input text, let the fake-job-posting text with same pattern
* Add a fully connected layer with input are feature and text embedding, like following image
![image](https://github.com/BillGuess/Fake-JD-Detector/assets/87471415/e967f36c-65cd-4bc5-b71e-bf37d505dc29)

## What I learned in this task
In order to do this task, I also learned a lot of knowledge
### Transformer
Here I read some paper and blog, to understand transformer
* [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
* [淺談神經機器翻譯 & 用 Transformer 與 TensorFlow 2 英翻中](https://leemeng.tw/neural-machine-translation-with-transformer-and-tensorflow2.html)
* Self-attention layer input is whole sequence, so it can parallel computing
* But it loss the word order in sequence, positioning encoding is need
* Because of inputing whole sequence, it will be more compute costing than RNN

### Self-attention
* [超详细图解Self-Attention](https://zhuanlan.zhihu.com/p/410776234)
* Although the content is similar to others, but the examples of self attention are better understood for me
* The key point is self-product

## Design a framework for production
![image](https://github.com/BillGuess/Fake-JD-Detector/assets/87471415/1941eb89-49e8-4b94-ad67-9058a2350b79)

## References
* [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
* [How to Fine-Tune BERT for Text Classification?](https://arxiv.org/abs/1905.05583)
* [淺談神經機器翻譯 & 用 Transformer 與 TensorFlow 2 英翻中](https://leemeng.tw/neural-machine-translation-with-transformer-and-tensorflow2.html)
* [進擊的 BERT：NLP 界的巨人之力與遷移學習](https://leemeng.tw/attack_on_bert_transfer_learning_in_nlp.html)
* [BERT: How to Handle Long Documents](https://www.saltdatalabs.com/blog/bert-how-to-handle-long-documents)
* [超详细图解Self-Attention](https://zhuanlan.zhihu.com/p/410776234)
