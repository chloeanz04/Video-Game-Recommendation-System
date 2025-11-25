# Video Game Recommendation System

## 1. Project Overview
This project implements a personalized recommendation system for video games, designed to help users discover new titles based on their preferences and interaction history. The system leverages machine learning techniques to tackle information overload, ensuring users receive relevant and highly personalized suggestions.

**Core Objectives:**
- Develop and evaluate high-performing recommendation models.
- Compare different filtering approaches (e.g., Collaborative Filtering vs. Content-Based).
- Provide a foundational framework for deployment and testing of recommendations.

## 2. Data Source
- **Dataset:** [Insert the name of the dataset used, e.g., Steam Games Dataset, IGN Reviews, etc.]
- **Description:** The dataset includes detailed game features (developers, genres, tags) and rich user interaction data (ratings, playtime, reviews) used to build the user-item interaction matrix.

## 3. Methodology
The project explored two main recommendation approaches:

### 3.1. Content-Based Filtering
- **Technique:** Utilized **[SPECIFIC_TECHNIQUE, e.g., TF-IDF Vectorizer and Cosine Similarity]** on game metadata (title, description, genre tags) to identify games with highly similar attributes.
- **Goal:** Recommend games similar to those the user has enjoyed in the past, effectively leveraging game features.

### 3.2. Collaborative Filtering
- **Technique:** Implemented **[SPECIFIC_TECHNIQUE, e.g., Singular Value Decomposition (SVD), Matrix Factorization, or KNN-based Filtering]** based on the User-Item Interaction Matrix.
- **Goal:** Suggest games that users with similar tastes and historical behavior have liked, leveraging the 'wisdom of the crowd'.

## 4. Model Performance
Model performance was evaluated using standard recommender system metrics.

| Model | Approach | Evaluation Metric | Result |
| :--- | :--- | :--- | :--- |
| Model 1 | [e.g., Content-Based + Cosine Similarity] | [Metric] | [Insert Result] |
| Model 2 | [e.g., Collaborative Filtering + SVD] | [Metric] | [Insert Result] |
| **Best Performing Model** | [Insert Best Model Name] | [Metric] | [Insert Best Result] |

## 5. Technology Stack
- **Language:** Python, Jupyter Notebook
- **Key Libraries:** `pandas`, `numpy`, `scikit-learn`, `surprise`/`tensorflow`/`pytorch`, `matplotlib`, `seaborn`

## 6. Repository Structure
.
├── DEMO/ # Live demo files or result screenshots
├── [GROUP 5]_Video_Games_RecSys_CODE.ipynb # Jupyter Notebook with main code, EDA, and model testing
├── [GROUP 5]_Video_Games_RecSys_REPORT.pdf # Final project report with analysis and results
├── README.md # Project description
└── [Data_File_Name].csv/.json # Dataset file (if included)

## 7. Setup and Installation
1. **Clone the repository:**
```bash
git clone https://github.com/chloeanz04/Video-Game-Recommendation-System.git
cd Video-Game-Recommendation-System
```
2. **Install dependency**
```bash
pip install -r requirements.txt
```

