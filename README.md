# Sherbet
Official Repository for the Supervised Project (Sherbet) 
#Pilot Dataset Construction  
Program: M1 NLP – Université de Lorraine  
Supervisor: Iglika Nikolova-Stoupak  

---

## Overview

This repository contains the pilot dataset and data construction pipeline for the Sherbet project.

The objective of this pilot experiment was to validate the data collection and preprocessing pipeline and ensure the dataset is suitable for stylistic classification between:

- Simple Wikipedia
- Standard Wikipedia

This is the first step before training classification models.

---

## Dataset Construction Pipeline

The dataset was created using the official Wikipedia API.

Pipeline steps:

1. Retrieve paired articles from:
   - Simple Wikipedia
   - Standard Wikipedia

2. Clean the text:
   - Remove references
   - Remove formatting
   - Keep only plain text

3. Sentence segmentation

4. Sentence filtering:
   - Minimum length: 6 words
   - Maximum length: 50 words

5. Ensure equal number of sentences per version

6. Assign labels:
   - simple_wikipedia
   - standard_wikipedia

---

## Pilot Dataset Statistics

Total sentences: **1428**

| Class | Sentences |
|------|-----------|
| Simple Wikipedia | 714 |
| Standard Wikipedia | 714 |

The dataset is perfectly balanced, ensuring fair model training.

---

## Sentence Length Analysis

Average sentence length:

- Simple Wikipedia: **14.80 words**
- Standard Wikipedia: **21.17 words**

Standard Wikipedia sentences are approximately **43% longer**, confirming higher linguistic complexity.

This validates that the dataset captures meaningful stylistic differences.

---

## Dataset Format

Example CSV format:
sentence,label
"Water is a liquid.",simple_wikipedia
"Water is a transparent, tasteless, odorless liquid.",standard_wikipedia

Columns:

- sentence → text
- label → class

---

## Conclusion

The pilot experiment confirms that:

- Dataset is clean
- Dataset is balanced
- Stylistic differences are measurable
- Dataset is suitable for machine learning

---

## Next Step

Scale dataset to approximately 10,000 sentences using the same pipeline.

This will be used for training classification models.

---

## License

For academic use only – Sherbet Project
Université de Lorraine

