# Recipe Entity Extraction using CRF

## 📌 Project Overview

This project focuses on extracting key entities from recipe text using **Natural Language Processing (NLP)** and a **Conditional Random Field (CRF)** model.

The objective is to identify and classify three important entity types from recipe instructions:

- **Ingredient**
- **Quantity**
- **Unit**

The project covers data preparation, feature engineering, model training, validation, evaluation and error analysis.

---

## 🎯 Business / Project Objective

The objective is to automatically identify structured information from unstructured recipe text.

The extracted entities can help transform recipe text into structured data that can be used for:

- Recipe information extraction
- Ingredient identification
- Quantity and unit extraction
- Recipe search and recommendation systems
- Food and recipe data processing

---

## 📊 Dataset

The original dataset contained **285 recipes**.

During data preprocessing, **5 recipes were removed** because of mismatches between token and POS-tag lengths.

The final dataset contained:

- **280 recipes**
- Recipe text represented as token sequences
- Part-of-speech information
- Entity labels for ingredient, quantity and unit

The data was divided into training and validation sets using a **70:30 split**.

---

## 🏷️ Entity Labels

The CRF model was trained to identify the following entity categories:

| Entity | Description |
|---|---|
| Ingredient | Food ingredients mentioned in recipes |
| Quantity | Numerical quantities associated with ingredients |
| Unit | Measurement units associated with quantities |

Examples include quantities such as numerical values and units such as measurement terms used in recipe instructions.

---

## 🔄 Project Workflow

```text
Recipe Dataset
      ↓
Data Inspection
      ↓
Data Cleaning
      ↓
Token & POS-Tag Validation
      ↓
Feature Engineering
      ↓
Train / Validation Split
      ↓
CRF Model Training
      ↓
Entity Prediction
      ↓
Model Evaluation
      ↓
Error Analysis
```
## 🧹 Data Preparation

The preprocessing workflow included:

- Inspecting recipe records
- Checking token and POS-tag lengths
- Removing records with mismatched token/POS sequences
- Preparing the data for sequence modelling
- Creating training and validation datasets
- Addressing class imbalance during model training

After preprocessing, 280 recipes were retained for modelling.

## ⚙️ Feature Engineering

Features were created from the token and linguistic information available in the recipe data.

The feature engineering process was designed to provide the CRF model with contextual information for identifying entity labels.

The model uses sequence-level information rather than classifying each token independently.

## 🤖 Model

A Conditional Random Field (CRF) model was used for sequence labelling.

CRF is suitable for this task because the entity assigned to one token can depend on surrounding tokens and the sequence context.

Class weighting was also incorporated to address label imbalance in the training data.

## 📈 Model Evaluation

The model achieved an overall validation accuracy of:

### 98.05%

Entity-level validation results included:

| Entity | Accuracy |
|---|---:|
| Ingredient | 99.43% |
| Quantity | 98.54% |
| Unit | 89.39% |

The results demonstrate strong performance for ingredient and quantity extraction, while unit extraction presented relatively more classification challenges.

## 🔍 Error Analysis

Error analysis was performed to understand where the model made incorrect predictions.

A key challenge identified was ambiguity between unit and ingredient entities.

The analysis helped identify areas where additional contextual features or improved training data could potentially improve entity recognition performance.

## 🛠️ Tools & Technologies
- Python
- Natural Language Processing (NLP)
- Conditional Random Field (CRF)
- Sequence Labelling
- Feature Engineering
- POS Tagging
- Machine Learning
- Jupyter Notebook

## 📁 Repository Structure
```
Recipe-Entity-Extraction-CRF/
│
├── Recipe_Entity_Extraction_CRF_Gayatri_Behera.ipynb
├── Recipe_Entity_Extraction_CRF_Report_Gayatri_Behera.pdf
└── README.md
```
## ▶️ How to Run
```
Clone or download this repository.
Install the required Python libraries used in the notebook.
Open:
Recipe_Entity_Extraction_CRF_Gayatri_Behera.ipynb
Run the notebook cells sequentially.
Review the preprocessing, feature engineering, CRF training, evaluation and error-analysis sections.
```
## 📌 Project Outcome

This project demonstrates an end-to-end NLP sequence-labelling workflow, from recipe data preprocessing and feature engineering to CRF model training, validation and error analysis.

The model achieved 98.05% validation accuracy and successfully extracted ingredient, quantity and unit entities from recipe text.

## 👩‍💻 Author

Gayatri Behera

Data Analyst | Python | SQL | Power BI | Machine Learning | Engineering Analytics
