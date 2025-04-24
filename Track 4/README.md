# Legal Holding Entailment Classification

## Overview
Sentence-pair classification for legal entailment using the CaseHold dataset from LexGLUE.

## Dataset
- **Link**: XXX
- **Train set**: 
- **Val set**: 
- **Test set**: 

## Task
- Train a 2-class model on the train set.
- Validate the trained model on the val set.
- Test the best model on the test set.

- Determine if a legal holding is entailed by a court case context
- Predict 0 (not entailed) or 1 (entailed)

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


