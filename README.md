# Liputan6 Text Summarization with BERT

This project focuses on text summarization using BERT models for Indonesian language. The project use open source dataset from
HuggingFace (source: https://huggingface.co/datasets/id_liputan6). Below are the details of the project.

## Used Pretrained Models:

1. [cahya/bert2bert-indonesian-summarization](https://huggingface.co/cahya/bert2bert-indonesian-summarization)
2. [Alfahluzi/bert2bert-extreme](https://huggingface.co/Alfahluzi/bert2bert-Large)

## Fine-Tuned Models:

The pretrained model `cahya/bert2bert-indonesian-summarization` was fine-tuned with different learning rates and batch sizes. Here are the fine-tuned models:

1. Learning rate 1e-5, Batch size 2
2. Learning rate 5e-5, Batch size 2
3. Learning rate 1e-5, Batch size 4
4. Learning rate 5e-5, Batch size 4

## Model Evaluation

The best performing model is fine tuned model with `learning rate 1e-5 and batch size 2` with the following Rouge scores:

- Rouge1: 0.342
- Rouge2: 0.126
- RougeL: 0.262
- RougeLSUM: 0.243

The fine-tuned model results can be accessed [here](https://huggingface.co/alfandy/bert2bert-batch2-lr1e-5-summarization) 

### Model Results:

| Model                                          | Type                    | Rouge1 | Rouge2 | RougeL | RougeLSUM |
|------------------------------------------------|-------------------------|--------|--------|--------|-----------|
| cahya/bert2bert-indonesian-summarization      | Pretrained              | 0.312  | 0.111  | 0.252  | 0.225     |
| Alfahluzi/bert2bert-extreme                   | Pretrained              | 0.065  | 0.000  | 0.049  | 0.038     |
| model_batch_4_lr_5e-5                         | Pretrained + Fine Tuned | 0.333  | 0.120  | 0.251  | 0.235     |
| model_batch_2_lr_5e-5                         | Pretrained + Fine Tuned | 0.328  | 0.117  | 0.250  | 0.232     |
| model_batch_4_lr_1e-5                         | Pretrained + Fine Tuned | 0.320  | 0.117  | 0.245  | 0.227     |
| model_batch_2_lr_1e-5 (best model)            | Pretrained + Fine Tuned | 0.342  | 0.126  | 0.262  | 0.243     |

