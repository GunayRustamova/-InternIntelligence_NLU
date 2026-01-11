# Named Entity Recognition with BERT

This project implements a Named Entity Recognition system using BERT-base-cased fine-tuned on the WikiANN dataset. The model identifies persons, organizations, and locations in text with 83.8% F1 score.

## Dataset
- WikiANN (English): 20,000 training samples from Wikipedia
- Entity types: PER (Person), ORG (Organization), LOC (Location)
- Split: 20k train, 10k validation, 10k test

## Model Architecture
- Base model: bert-base-cased
- Fine-tuning: 3 epochs with learning rate 2e-5
- Batch size: 16
- Training time: 6.6 minutes on T4 GPU

## Performance Metrics
- Overall F1 Score: 0.838
- Precision: 0.825
- Recall: 0.851
- Accuracy: 0.935

### Per-Entity Performance
| Entity | Precision | Recall | F1-Score |
|--------|-----------|--------|----------|
| PER    | 0.881     | 0.915  | 0.898    |
| LOC    | 0.841     | 0.872  | 0.856    |
| ORG    | 0.754     | 0.770  | 0.762    |

View full training metrics: [Weights & Biases Dashboard](https://wandb.ai/gunayrustamova-/ner-bert-finetuning?nw=nwusergunayrustamova)

![Training Metrics](wandb_metrics.png)

## Requirements
- transformers
- datasets
- torch
- wandb
- seqeval

## Running the Code
1. Open notebook in Google Colab
2. Enable GPU runtime
3. Run all cells
4. Model saves to ./ner-bert-final/
