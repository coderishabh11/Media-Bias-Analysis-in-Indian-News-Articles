# Media Bias Analysis in Indian News Articles


![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Transformers](https://img.shields.io/badge/Transformers-Hugging%20Face-yellow?logo=huggingface&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red?logo=python&logoColor=white)


## Overview
This project focuses on the analysis of media bias within the Indian media landscape. It addresses the nuances of linguistic, cultural, and regional diversity in Indian journalism and provides a data-driven approach to identify and quantify media bias. By leveraging advanced Natural Language Processing (NLP) techniques, the project aims to explore key aspects of media bias, including sentiment, tone, political leaning, and contextual bias.

---

## Problem Statement
Media serves as a cornerstone of democracy, yet bias—whether overt or subtle—can undermine its role by distorting facts and promoting selective narratives. In India, with its socio-political complexities and diverse media ecosystem, studying and addressing media bias is particularly challenging. This project aims to:

- Analyze the evolution of media bias from 2020 to 2024.
- Study bias across various article types (e.g., opinions, reports, analyses).
- Investigate variations in bias across topics such as politics, healthcare, and sports.
- Examine the influence of article tone and political leanings on media bias.
- Explore the role of digital platforms in shaping media bias.

---

## Methodology
### 1. **Dataset Creation**
- **Source**: Articles were scraped from The Times of India and The Economic Times using Beautiful Soup.
- **Volume**: An initial collection of 1.5 million articles was narrowed to a subset of 50,000 articles.
- **Preprocessing**: Text cleaning, normalization, and metadata extraction.

### 2. **Categorization of Articles**
- Articles were classified into eight main categories: Politics, Culture & Lifestyle, Business, Health, Disaster, Economy, Sports, and Science & Technology.
- Subcategories were defined for detailed analysis using a Zero-Shot Classification approach.
- ![main category distribution (zero shot classification)](https://github.com/user-attachments/assets/c54d68b2-46dd-4889-9c8b-298026939413)

### 3. **Tone Detection**
- Sentiment analysis was conducted using the Twitter RoBERTa pretrained model to classify article tones into Very Negative, Negative, Neutral, Positive, and Very Positive.
- ![article_tone_distribution](https://github.com/user-attachments/assets/a03f8eff-eda1-4f59-be9a-13cfe688e7f1)

### 4. **Classification of News Types**
- Articles were categorized into News Reports, News Analysis, and Opinion using a semi-supervised approach combining manual labeling and BERT-based embeddings.
- ![news type distribution](https://github.com/user-attachments/assets/42b8d244-933c-454a-b369-9b7cecde533c)

### 5. **Political Leaning Detection**
- A lexicon-based approach with TF-IDF and BERT embeddings was employed to determine political leaning (Left, Right, Neutral).
- ![political leaning distribution](https://github.com/user-attachments/assets/a1c9ce6f-38b8-4f19-b09a-fee8da7ba59d)

### 6. **Bias Detection Model**
- A contextual bias score was computed using cosine similarity and a lexicon of 3,000 bias-related terms.
- A hybrid classification model using Longformer embeddings, sentiment scores, and article features was developed to classify biased versus unbiased articles.
- ![bias score by main category](https://github.com/user-attachments/assets/78b3db09-143e-41ef-bd21-dbcf00a4803a)
- ![bias-unbias by year](https://github.com/user-attachments/assets/87bb43be-62e4-4e8e-982d-0505efe462d9)

---

## Key Features
- **Custom Dataset**: Scraped and preprocessed articles tailored for the Indian media context.
- **NLP Techniques**: Leveraging state-of-the-art models such as RoBERTa, BERT, and Longformer.
- **Bias Quantification**: Introduction of a contextual bias score to measure divergence from neutrality.
- **Semi-Supervised Learning**: Innovative techniques to address the lack of labeled data.

### Libraries & Tools Used

![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas&logoColor=white)
![Numpy](https://img.shields.io/badge/Numpy-Numerical%20Computation-blue?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red?logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-blue?logo=python&logoColor=white)
![Transformers](https://img.shields.io/badge/Transformers-Hugging%20Face-yellow?logo=huggingface&logoColor=black)
![Scikit-learn](https://img.shields.io/badge/Scikit%20Learn-Machine%20Learning-orange?logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Modeling-blue?logo=xgboost&logoColor=white)

---

## Results
- **Article Categorization**: Distribution visualized across main categories and subcategories.
- **Tone Analysis**: Majority of articles exhibited a neutral tone.
- **Bias Trends**: Scatter plots and statistical analysis demonstrated variations in bias levels across topics and tones.

You can check these results in the `Results/` folder, which contains the generated plots and visualizations.

---

## Figures
- Distribution of articles across main categories (Bar Chart)
- Subcategory distributions (Pie Charts)
- Article tone distribution (Bar Chart)
- Political leaning trends (Bar Chart and Scatter Plot)
- Bias score variation (Scatter Plot)

---

## Technologies Used
- Python
- Jupyter Notebook
- Beautiful Soup
- Transformers (Hugging Face)
- Longformer
- XGBoost, KNN, and Voting Classifier
- Matplotlib, Seaborn (for visualizations)

---

## How to Use
1. **Clone Repository**:
   ```bash
   git clone <repository-link>
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run Analysis**:
   Open the Jupyter Notebook `Media_Bias_Analysis.ipynb` in your preferred editor (e.g., Jupyter Lab, Jupyter Notebook, or VS Code) and execute the cells in sequence.

4. **Visualize Results**:
   Check the `Results/` directory for generated plots and reports.

---

## Future Work
- Extend the dataset to include more diverse sources and regional languages.
- Integrate advanced transformer-based models for deeper analysis.
- Develop a web-based visualization dashboard for interactive exploration.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgements
- The Times of India and The Economic Times for providing the data.
- Hugging Face for the pretrained models.
- Python community for open-source libraries and frameworks.
