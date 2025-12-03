# [Python] Video Game Recommendation System

## Overview
This project implements a personalized recommendation system for video games, designed to help users discover new titles based on their preferences.

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
  - 
Through 

---

## Methodology
The project explored two main recommendation approaches:

### Content-Based Filtering
- **Technique:** Utilized **TF-IDF Vectorizer, Truncated SVD, Cosine Similarity or KNN** on game metadata (title, description, genre tags) to identify games with highly similar attributes.
- **Goal:** Recommend games similar to those the user has enjoyed in the past, effectively leveraging game features.

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

