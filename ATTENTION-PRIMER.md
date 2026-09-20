# Attention Primer

A one-place starter reference for the two papers that kicked off the attention era. All figures below are the headline numbers reported in each paper's abstract (arXiv abstracts, live lookups; nothing padded from memory).

## Attention Is All You Need (arXiv 1706.03762)

The Transformer: a new, simple architecture based solely on attention mechanisms, dispensing with recurrence and convolutions entirely. Superior in quality while being more parallelizable and requiring significantly less time to train.

Headline results from the abstract:

- **WMT 2014 English-to-German: 28.4 BLEU**, improving over the existing best results, including ensembles, by over 2 BLEU.
- **WMT 2014 English-to-French: 41.8 BLEU**, a new single-model state-of-the-art, after training for 3.5 days on eight GPUs — a small fraction of the training cost of the best models from the literature.
- The abstract also states the model generalizes well by applying successfully to **English constituency parsing** with both large and limited training data, but reports **no figure** for parsing in the abstract itself.

## BERT (arXiv 1810.04805)

BERT (Bidirectional Encoder Representations from Transformers) pre-trains deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers; the pre-trained model can be fine-tuned with just one additional output layer, without substantial task-specific architecture modifications.

Headline results from the abstract — **new state-of-the-art on eleven NLP tasks**, including:

- **GLUE score: 80.5%** (7.7 point absolute improvement)
- **MultiNLI accuracy: 86.7%** (4.6 point absolute improvement)
- **SQuAD v1.1 question answering Test F1: 93.2** (1.5 point absolute improvement)
- **SQuAD v2.0 Test F1: 83.1** (5.1 point absolute improvement)

### Practical angle: the standard Google base-uncased checkpoint

- **Hugging Face Hub model repo id:** `google-bert/bert-base-uncased`
- **Pipeline task:** `fill-mask`
- **License:** `apache-2.0`
- The model card's citation tag (`arxiv:1810.04805`) confirms the BERT paper's arXiv id.
