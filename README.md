# Truth and AI: The Impact of Fine-Tuning GPT-3.5 on Lie Detection
---

## Description
This study evaluates the performance of a fine-tuned GPT-3.5 model in detecting deceptive opinions. Inspired by Loconte et al. (2023), we utilize a dataset of opinions labeled as either truthful or deceptive and apply a fine-tuning process to enhance GPT-3.5’s capabilities in deception detection. The findings reveal that the fine-tuned GPT-3.5 outperforms the FLAN-T5 model (as presented in the referenced article) in accuracy and exhibits the use of statistically significant linguistic features to distinguish between truthful and deceptive statements. This research contributes to the potential applications of large language models in fields requiring deception detection.

<p align="center">
<img src="https://github.com/alecruces/GPT-Truth/assets/67338986/2e5fa825-4747-4fe3-a103-1fe6808ba833" alt="LLM2" style="width:400px;height:auto;"/>
</p>

## Keywords
LLM, AI, neuroscience

## Data 
- **Dataset:** Opinions under Scenario 1 used in Loconte et al. (2023)

## Methods
- **LLM Fine-Tuning:** Chat GPT-3.5-turbo-0163 fine-tuning
- **Common Language Effect Size (CLES)**

## Software
- Python
  
## Files  
- **Report:** `Report.pdf`
- **Presentation:** `Presentation.pdf`

## Model Evaluation
### Table 1: Summary of Model Evaluation Metrics by Cross-Validation Fold

| Metric       | Model 1 | Model 2 | Model 3 | Model 4 | Average Value | Standard Deviation |
|--------------|---------|---------|---------|---------|---------------|---------------------|
| Accuracy     | 0.8816  | 0.8512  | 0.8688  | 0.8624  | 0.8660        | 0.0110              |
| Precision    | 0.8692  | 0.8904  | 0.8775  | 0.8558  | 0.8732        | 0.0126              |
| Recall       | 0.8971  | 0.8100  | 0.8548  | 0.8669  | 0.8572        | 0.0313              |
| F-score      | 0.8829  | 0.8483  | 0.8660  | 0.8571  | 0.8636        | 0.0128              |

From Table 1, the average accuracy of the models is 0.87 with a standard deviation of 0.0110. The consistent performance across different splits suggests that the models are not overfitting to the training set and are generalizing well.

### Confusion Matrix
Cognitive biases in GPT-3.5 reveal a truth bias, a psychological tendency where individuals are inclined to believe others are truthful, regardless of actual deception. In terms of error classification, GPT-3.5 has a higher number of false positives compared to false negatives. This indicates a tendency to classify results as true (T), regardless of the actual nature of the opinion.

<p align="center">
<img src="https://github.com/user-attachments/assets/107547e1-dc33-4974-be3a-9628ed9f95be" alt="Confusion Matrix" style="width:400px;height:auto;"/>
</p>


