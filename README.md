# Fine-tune-Transformer-summarization

The repo stores code as part of the graduate research project for MCS of CSUN.

The research uses several pretrained transformers checkpoints from Huggingface API, downstreaming and fine-tuning to text summarization tasks.

Assessments include T5, T5-small, BART, Encoder-Decoder model with bert, and ProphetNet. 

For more information, check CSU ScholarWorks "FINE-TUNING TRANSFORMERS: ASSESSMENTS OF TRANSFORMER-BASED MODELS DOWNSTREAM TO TEXT SUMMARIZATION"

---

## Abstract

Text summarizing is one of the core tasks in natural language processing while the classical summarizing approach is currently facing a major problem in adapting to the demands of information retrieval. Having a trustworthy and accurate automatic summarizer
is becoming increasingly vital. The huge potential is seen as the rapid development of the transformer family. In practice, selecting the right one from a large number of models becomes a new problem that rarely studied and researched on. This research paper focus on implementing several popular transformer models - BERT, BART, T5 and ProphetNet, figuring
out their different characters and properties by fine-tuning and down streaming them to summarization on several datasets, then evaluate them from ROUGE Scores, training time and training sample size. Through this process, we find that transformers are powerful machine in natural language processing and in extremely need for data to fine-tune. Although shows different properties, they all tend to perform better when parameters and pre-trained datasets are bigger.

## Introduction

The huge potential is seen as the rapid development of the transformer family. Finetuning transformer is a way to exploit the full power of this state-of-art technology. However, in the practice, there are many limitations such as small dataset or computing cost preventing us to train an idealistic model just as good as data scientists trained in the lab with huge computing power. And there are also lots of models to choose to train as more and more people switching to the transformers and improve the inner architecture, making it harder to decide which one is most suitable to train on for their specific summarization
task.

## Partial Project Outputs

**Tokenized training data overview**

|     Dataset    |     Mean Length    |     T5-small    |     BART    |     BERT    |     ProphetNet    |
|---|---|---|---|---|---|
|     XSUM    |     Article     |     525    |     489    |     479    |     478    |
|  |     % > 512    |     38.3%    |     35.0%    |     34.2%    |     34.1%    |
|  |     Summary     |     30    |     28    |     28    |     27    |
|  |     % > 64    |     0.5%    |     0.2%    |     0.2%    |     0.2%    |
|     CNN/Daily    |     Article     |     923    |     822    |     848    |     847    |
|  |     % > 512    |     77.7%    |     72.2%    |     73.6%    |     73.5%    |
|  |     Summary     |     66    |     60    |     58    |     57    |
|  |     % > 64    |     55.2%    |     39.4%    |     31.8%    |     29.3%    |
|     Wikihow      |     Article     |     796    |     750    |     743    |     742    |
|  |     % > 512    |     55.7%    |     52.4%    |     51.8%    |     51.7%    |
|  |     Summary    |     73    |     76    |     68    |     67    |
|  |     % > 64    |     41.4%    |     43.3%    |     38.6%    |     38.0%    |


**Training Output**
![](/Fine-tune-Transformer-summarization/blob/master/Image/train_output.png)

**Result with different training size**
![](/Fine-tune-Transformer-summarization/blob/master/Image/MergedLoss.png)

**Results of the fine-tune**
![](/Image/RougeResult.png)