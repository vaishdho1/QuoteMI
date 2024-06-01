# Quote Multilabel Classification and Interpretation

## Project Overview

This project focuses on developing a system to classify and interpret motivational quotes using various Natural Language Processing (NLP) techniques. Given the importance of quotes in providing perspective, humor, and concise insights, the project aims to categorize quotes accurately and provide clear interpretations.

## Team Members

- Rashmi Vagha (rvagha@umass.edu)
- Rohit Kadappa Gundakalli (rgundakalli@umass.edu)
- Vaishnavi Panchvati (vpanchavati@umass.edu)
- Varun Tarikere Shankarappa (vtarikeresha@umass.edu)

## Problem Statement

In today's stress-filled era, quotes serve as a valuable source of encouragement and perspective. Quotes need to be categorized appropriately for various applications such as text analysis, enhancing chatbots, and supporting virtual learning. The project aims to classify quotes into multiple labels and provide interpretations to enhance their contextual understanding.

## Project Scope

### Initial Goals
- Explore multi-class classification of quotes.
- Use BERT, T5, and RoBERTa for classification.

### Adjusted Goals
- Shift to multi-label classification for a more challenging dataset.
- Use smaller models (DistilBERT, T5, GPT2, RoBERTa) due to compute constraints.
- Implement Gemma 2B and T5 3B models for zero-shot, one-shot, and few-shot prompting for interpretation.

## Related Work

The project builds on previous research in text classification and NLP, specifically focusing on the fine-tuning of Transformer-based models like BERT, RoBERTa, and T5. The evolution of text classification tasks from coarse-grained to fine-grained, including multi-label classification, has been a key area of focus.

## Dataset

### Data Collection and Preprocessing

The dataset used is Quotes-500k, which contains approximately 500,000 quotes with corresponding labels. Key preprocessing steps included:
- Removing specific and non-generic labels.
- Employing stratified sampling to ensure balanced label distribution.
- Limiting quote length to between 25 and 256 characters.

### Classification Dataset
- Final dataset: 87,941 quotes with 5 labels (Love, Life, Inspirational, Philosophy, Humor).
- Approximately 30,000 quotes were sampled for final classification.

### Interpretation Dataset
- Selected top 10 frequently appearing labels.
- Manually picked and interpreted 40 quotes per label to ensure interpretability.

## Baselines

### Classification
- **DistilBERT**: Baseline model, fine-tuned for multi-label classification using a sigmoid function over an additional linear layer.
- **DistilGPT-2**: Fine-tuned with an additional linear layer and softmax for multi-label classification.
- **T5**: Fine-tuned using sequence-to-sequence modeling with binary cross-entropy for label prediction.

### Interpretation
- **Zero-shot prompting**: Used as the baseline for quote interpretation.

## Approach

### Classification
- **RoBERTa**: Pretrained 'roberta-base' model fine-tuned for classification with additional layers.
- **DistilGPT-2**: Fine-tuned for multi-label classification using softmax and additional linear layers.
- **T5**: Used encoder-decoder architecture for label prediction with prompt enhancement.

### Interpretation
- **Models**: T5 (3B) and Gemma (2B) used for zero-shot, one-shot, and few-shot prompting.
- **Sentence Transformer**: Employed to enhance few-shot prompting by selecting relevant quotes.

## Evaluation

- **Metrics**: Jaccard score for multi-label classification accuracy, along with f1-score, precision, and tag-wise accuracy.
- **Error Analysis**: Conducted to identify challenging examples and improve model performance.

## Results and Findings

Through extensive experimentation and analysis, the project evaluated the performance of various models in quote classification and interpretation. The use of prompting techniques significantly improved the interpretability of quotes.

## Conclusion

The project successfully developed a system for multi-label classification and interpretation of quotes, leveraging Transformer-based models and advanced prompting techniques. The findings highlight the potential of using smaller, efficient models for complex NLP tasks in resource-constrained environments.

For more detailed information and results, refer to the attached report.

---

This README provides a comprehensive overview of the Quote Multilabel Classification and Interpretation project, outlining the problem statement, approach, and key findings. For any further queries or contributions, please contact the team members via the provided email addresses.