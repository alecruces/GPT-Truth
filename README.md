# Truth and AI: The Impact of Fine-Tuning GPT-3.5 on Lie Detection

> Evaluating a fine-tuned GPT-3.5 model’s effectiveness in distinguishing truthful from deceptive opinions.

<p align="center">
<img src="https://github.com/alecruces/GPT-Truth/assets/67338986/2e5fa825-4747-4fe3-a103-1fe6808ba833" alt="LLM2" style="width:400px;height:auto;"/>
</p>

## Keywords
LLM, AI, neuroscience, Fine-tuning
---

## Table of Contents

1. [About the Project](#about-the-project)
2. [Key Features](#key-features)
3. [Key Results](#key-results)
4. [Data Overview](#data-overview)
5. [Methodology](#methodology)
6. [Screenshots and Graphs](#screenshots-and-graphs)
7. [Technologies Used](#technologies-used)
8. [Setup & Installation](#setup--installation)
9. [Usage](#usage)
10. [Contributing](#contributing)
11. [License](#license)
12. [Contact](#contact)

---

### About the Project

This study explores the performance of a fine-tuned GPT-3.5 model in detecting deception, inspired by Loconte et al. (2023). We utilize a dataset of opinions labeled as truthful or deceptive and evaluate whether fine-tuning can improve detection accuracy. The study demonstrates that GPT-3.5 outperforms FLAN-T5 in this task, revealing a truth bias but showing enhanced generalization capabilities.

### Key Features

- **Enhanced Detection Accuracy**: The fine-tuned GPT-3.5 model achieved high accuracy (86.6%) in distinguishing between truthful and deceptive statements.
- **Performance Comparison**: GPT-3.5-turbo-0163 surpasses FLAN-T5 in accuracy, precision, and F-score across several opinion-based topics.
- **Truth Bias Analysis**: Examination of the model’s cognitive biases, particularly a truth bias resulting in higher false-positive rates.

### Key Results

- **Model Accuracy**: The average accuracy across folds is 0.866, indicating consistent performance and minimal overfitting.
- **Truth Bias**: The model displays a tendency to classify opinions as truthful, reflected in a higher number of false positives.
- **Performance on Topics**:
  - Highest Accuracy: Gay Marriage (89.0%)
  - Lowest Accuracy: Cannabis Legalization (83.8%)

### Data Overview

The dataset contains opinion statements categorized by topic and labeled as either truthful or deceptive.

- **Source**: Scenario 1 opinions dataset as used by Loconte et al. (2023).
- **Sample Size**: 2500 statements.
- **Cross-Validation**: 4-fold cross-validation, with a 75%-25% train-test split.

### Methodology

The project uses a structured fine-tuning process on the GPT-3.5-turbo-0163 model, with cross-validation and explainability analysis:

- **Fine-Tuning Process**: GPT-3.5 is fine-tuned for 3 epochs per fold using the specified dataset, with labels assigned as either True (T) or False (F).
- **Metrics**: Key metrics—accuracy, precision, recall, and F-score—are calculated per cross-validation fold.
- **Explainability Analysis**: A Common Language Effect Size (CLES) analysis is conducted on linguistic features, identifying patterns associated with truthful or deceptive statements.

### Screenshots and Graphs

These visuals enhance understanding of the model’s performance and bias tendencies:

1. **Cross-Validation Performance (Table)**  
   The following table summarizes model evaluation metrics (accuracy, precision, recall, F-score) across four folds, showing consistency and reliability.

   | Metric       | Model 1 | Model 2 | Model 3 | Model 4 | Average Value | Standard Deviation |
   |--------------|---------|---------|---------|---------|---------------|---------------------|
   | Accuracy     | 0.8816  | 0.8512  | 0.8688  | 0.8624  | 0.8660        | 0.0110              |
   | Precision    | 0.8692  | 0.8904  | 0.8775  | 0.8558  | 0.8732        | 0.0126              |
   | Recall       | 0.8971  | 0.8100  | 0.8548  | 0.8669  | 0.8572        | 0.0313              |
   | F-score      | 0.8829  | 0.8483  | 0.8660  | 0.8571  | 0.8636        | 0.0128              |

2. **Confusion Matrix (Heatmap)**  
   Displays the distribution of true positives, true negatives, false positives, and false negatives, indicating a truth bias in the model’s classification.

   <p align="center">
  <img width="483" alt="confusion_matrix" src="https://github.com/user-attachments/assets/79df202e-2d4a-4813-a49a-e3777aa0e5b2">
  </p>

3. **Accuracy Comparison by Topic (Bar Chart)**  
   Shows accuracy scores for various topics (e.g., Gay Marriage, Immigration), highlighting the model's effectiveness across distinct subjects.

   <p align="center">
  <img width="585" alt="results_scenario" src="https://github.com/user-attachments/assets/2e111ba2-efb1-49b0-b3cb-ab65f72b0699">
  </p>

4. **Moving Average Training Loss and Accuracy (Line Charts)**  
   Plots the training accuracy and loss across epochs, reflecting model convergence during fine-tuning.

   <p align="center">
  <img width="1008" alt="losses" src="https://github.com/user-attachments/assets/ac2dfc7f-1204-44b8-a8a7-6de79aa54383">
  </p>

5. **CLES Analysis for Linguistic Features (Bar Chart)**  
   Visual representation of the top linguistic features that differentiate truthful from deceptive statements, as measured by CLES.

   <p align="center">
  <img width="743" alt="CLES" src="https://github.com/user-attachments/assets/846558f9-f443-4d4d-a695-01eca4a2a872">  
  </p>

### Technologies Used

> 🛠️ Highlighting essential tools and methods.

- ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white): Main programming language.
- **OpenAI API**: For model fine-tuning and evaluation using GPT-3.5-turbo-0163.
- **Explainability Analysis**: Linguistic feature analysis using Common Language Effect Size (CLES).

### 8. Setup & Installation

Clone the repository and install dependencies to replicate the study:

```bash
# Clone the repository
git clone https://github.com/username/GPT-Truth.git

# Navigate to the project directory
cd GPT-Truth

# Install dependencies
pip install -r requirements.txt
```

### Usage

The repository includes the following files:

- **`GPT_3_5_Opinioni_Scenario1.ipynb`**: Jupyter notebook for the full workflow, from data loading to model fine-tuning and evaluation.
- **`Report.pdf`**: Detailed report of the study’s methodology and findings.
- **`Presentation.pdf`**: Summary presentation of key points and visual results.

To run the project, open `GPT_3_5_Opinioni_Scenario1.ipynb` in Jupyter Notebook and execute the cells sequentially.

### Contributing

Contributions are welcome! Please refer to the contributing guidelines for more details.
