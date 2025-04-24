# Fake News Classification

## Overview
Binary classification task using titles and full text to distinguish real vs. fake news.

## Dataset
- **Link**: https://drive.google.com/drive/folders/1NubH-XpmA4QtQv9B6sc3Qr3MGb6jqEYM?usp=sharing
- **Train set**: 31442
- **Val set**: 6736
- **Test set**: 6739

- Label: (1 for Fake, 0 for True)
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

0, 1

1, 0

...

