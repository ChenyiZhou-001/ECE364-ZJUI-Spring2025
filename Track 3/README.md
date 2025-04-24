# Fake News Classification

## Overview
Binary classification task using titles and full text to distinguish real vs. fake news.

## Dataset
- **Link**: XXX
- **Train set**: 1531
- **Val set**: 326
- **Test set**: 331

## Task
- Train a 2-class model on the train set.
- Validate the trained model on the val set.
- Test the best model on the test set.
  
- Input: `title` + `text`
- Output: `REAL` or `FAKE`

**Evaluation metric**: 
- Accuracy
  
## Requirements
- < 15 million parameters
- Use DistilBERT, TinyBERT, or traditional models (Pretrained Models are allowed to use.)
- Pytorch, HuggingFace Transformers, scikit-learn

## Output Format
Id, Label

0, REAL

1, FAKE

...

