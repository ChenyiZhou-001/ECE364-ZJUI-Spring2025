# Multiple Choice Legal Holding Selection

## Overview
Multiple-choice classification to select the correct legal holding for a given case context.

## Dataset
- **Link**: https://drive.google.com/drive/folders/1XlhW-HD3GBCKM5rWvpP_UWpiEsl_NK2a?usp=sharing
- **Train set**: 4500
- **Val set**: 3900
- **Test set**: 3600
- Each instance consists of a legal case `context`, a list of 5 potential `endings` (holdings), and a `label` (0-4) indicating the index of the correct holding.

## Task
- Train a 5-class model on the train set.
- Validate the trained model on the val set.
- Test the best model on the test set.

- Given a legal case `context` and 5 candidate `endings` (holdings), select the correct holding that accurately summarizes or follows from the context.
- Predict the index (`label`) corresponding to the correct holding (0, 1, 2, 3, or 4).

**Evaluation metric**: 
- Accuracy
  
## Requirements
- < 15 million parameters
- Use DistilBERT, TinyBERT, LegalBERT, or traditional models (Pretrained Models are allowed to use.)
- Pytorch, HuggingFace Transformers, scikit-learn

## Output Format
Id, Label

0, 1

1, 0

...


