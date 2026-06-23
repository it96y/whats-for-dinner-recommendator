# What's for dinner Recommendation System: A recipe Recommendation Model Based on Ingredients

An experimental content-based recommendation prototype developed on Kaggle designed to address the daily struggle: *"What should I eat today?"*. The system suggests recipes based on the ingredients currently available in a user's kitchen, filtering and ranking candidates using natural language processing and machine learning.

## System Overview & Features

- **Content-Based Recommendation:** Matches user-provided ingredient keywords against a large-scale structured recipe dataset.
- **Automated Text Normalization:** Cleans text by converting to lowercase and stripping numerical quantities, measurement units, special characters, parentheses, and non-discriminative stopwords.
- **Taste & Flavor Classification:** Groups recipes into three core flavor profiles (**sweet**, **savory**, and **low-sodium**) based on an optimized keyword rule-matching extraction pipeline.

## Dataset

- **Source:** *Food.com Recipes with Search Terms and Tags* dataset (published by Shuyang Li et al. on Kaggle), containing ~500,000 raw recipes spanning 18 years of user uploads.
- **Data Selection:** Filtered down to **214,246 valid records** post-cleaning.
- **Class Balancing:** To resolve severe class imbalance (where `sweet` and `low-sodium` heavily outnumbered `savory`), a resampling strategy was applied to establish a perfectly balanced training dataset of **6,000 total samples** (2,000 samples per class).

## Inputs & Outputs

- **Main Input:** A raw text string or keyword list of available ingredients (e.g., `"flour banana chocolate egg"`).
- **Main Output:** Top 5 ranked recipes containing:
  - Recipe Name (`name`)
  - Taste Profile Label (`appetite`)
  - Full Ingredients List (`ingredients`)
  - A comparison of available vs. required missing ingredients.

## Evaluation & Performance

Evaluated on an independent test partition of 1,200 samples, the classification and recommendation pipeline delivered high accuracy and stability:

- **Overall Accuracy:** 89.00%
- **Weighted F1-Score:** 0.8922

### For further understanding and analysis report of my project, please check the file *model_description.pdf*.

### Project Kaggle URL
https://www.kaggle.com/code/uyenvynguyen/gk-thnn
