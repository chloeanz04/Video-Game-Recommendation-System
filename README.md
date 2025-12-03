# [Python] Video Game Recommendation System

## Overview

This project implements a personalized recommendation system for video games, designed to help users discover new titles based on their preferences.

The original project: [Video Game Recommendation Engine by SulmanK](https://github.com/SulmanK/Video-Game-Recommendation-Engine/blob/master/Video%20Game%20Recommendation%20Engine.ipynb)

The main goals were to understand, reimplement, and optimize the existing system. Our team selected this GitHub project as the base and focused on improving the **speed**, **flexibility**, and **diversity** of recommendations, while maintaining interpretability and academic clarity.

---

## Data Source
- **Dataset:** [GiantBomb API](https://www.giantbomb.com/api/)
- **Description:** The dataset contains detailed information about games, including:
  - `id`: unique identifier for each game  
  - `name`: name of the game  
  - `original_game_rating`: age rating according to US standards  
  - `original_release_date`: release date of the game  
  - `platform`: compatible gaming platforms  
  - `developers`: game developers  
  - `genre`: game genres  
  - `theme`: game themes  
  - `concept`: game style or concept  
  - `franchise`: series the game belongs to

Through EDA, the most suitable method for this dataset is **Content-Based Filtering** due to the following reasons:
- Only game information is required; no user data is needed.
- Well-suited for sparse datasets.
- Easy to implement.
- Vectorization method - **TF-IDF**:
  - The dataset contains short text data (mainly lists of tags), so more expensive methods are unnecessary.
  - TF-IDF highlights less common tags better than Count Vectorizer.
  - The algorithm is simple, which optimizes computational efficiency.


---

## Methodology
- **TF-IDF Vectorization**: Encodes categorical text attributes (`game_rating`, `developer`, `genre`, `theme`, `concept`) into numerical feature vectors.  
- **Cosine Similarity**: Measures similarity between games based on their TF-IDF vectors.  
- **K-Nearest Neighbors (KNN)**: Identifies the K most similar games for a given input game.  
- **Truncated SVD (Singular Value Decomposition)**: Reduces feature dimensionality to improve runtime performance.  
- **Single Filtering**: Recommends games by selecting titles that share similar attributes (genre, theme, concept, franchise, or developer) with the input games.
- **Web Demo** – Develops an interactive app to visualize and explore game recommendations.

---

## Results
| Method                  | Processing Time | Relevance to Input | Diversity of Recommendations | Suitable Scenario |
|-------------------------|----------------|------------------|------------------------------|-----------------|
| Cosine Similarity       | 12–13 s        | High – closely matches user’s played games | Moderate – sometimes not fully similar | When users want suggestions very close to their previous preferences |
| KNN                     | 6–7 s          | Medium – sometimes not truly similar | Less diverse – focuses on similar content | When users want to explore similar games |
| SVD + Cosine Similarity | 0.18–0.20 s    | High – similar to original Cosine results | More diverse – provides new options | When users want faster recommendations with some diversity |
| SVD + KNN               | 0.05–0.07 s    | Medium – similar to original KNN results | More diverse – provides new options | When users want very fast recommendations exploring new types of games |

## Repository Structure
```text
├── DEMO/ # Live demo files or result screenshots
├── [GROUP 5]_Video_Games_RecSys_CODE.ipynb # Jupyter Notebook with main code, EDA, and model testing
├── [GROUP 5]_Video_Games_RecSys_REPORT.pdf # Final project report with analysis and results
├── README.md # Project description
└── [Data_File_Name].csv/.json # Dataset file (if included)
```
## Setup and Installation
1. **Clone the repository:**
```bash
git clone https://github.com/chloeanz04/Video-Game-Recommendation-System.git
cd Video-Game-Recommendation-System
```
2. **Install dependency**
```bash
pip install -r requirements.txt
```

