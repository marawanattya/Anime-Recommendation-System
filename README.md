# Anime Recommendation System

This repository contains an Anime Recommendation System that leverages Collaborative Filtering, Content-Based Filtering, and a Hybrid Approach to recommend anime to users. The system is built using Python and popular libraries such as Pandas, Scikit-learn, and Surprise.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Installation](#installation)
4. [Usage](#usage)
   - [Collaborative Filtering](#collaborative-filtering)
   - [Content-Based Filtering](#content-based-filtering)
   - [Hybrid Approach](#hybrid-approach)
   - [Knowledge-Based Recommendations](#knowledge-based-recommendations)
5. [Evaluation](#evaluation)
6. [Contributing](#contributing)


## Introduction

The Anime Recommendation System is designed to provide personalized anime recommendations to users based on their preferences and viewing history. The system employs three main recommendation techniques:

- **Collaborative Filtering**: Uses user-item interactions to predict what a user might like based on similar users.
- **Content-Based Filtering**: Recommends items similar to those a user has liked in the past, based on item features.
- **Hybrid Approach**: Combines Collaborative and Content-Based Filtering to improve recommendation quality.
- **Knowledge-Based Recommendations**: Uses genre information to recommend anime based on user preferences.

## Dataset

The dataset used in this project is the [Anime Recommendations Database](https://www.kaggle.com/CooperUnion/anime-recommendations-database) from Kaggle. It contains two main files:

- `anime.csv`: Contains information about anime such as title, genre, type, episodes, rating, and members.
- `rating.csv`: Contains user ratings for anime.

## Installation

To run this project, you need to have Python installed along with the following libraries:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib scikit-surprise
```

You can download the dataset using the following commands:

```bash
kaggle datasets download CooperUnion/anime-recommendations-database
unzip anime-recommendations-database.zip
```

## Usage

### Collaborative Filtering

Collaborative Filtering is implemented using the Singular Value Decomposition (SVD) algorithm from the Surprise library. The model is trained on user ratings and evaluated using RMSE, MAE, Precision, Recall, F1-score, and Accuracy.

### Content-Based Filtering

Content-Based Filtering is implemented using cosine similarity on anime features such as genre, type, and rating. The system recommends anime similar to those a user has liked in the past.

### Hybrid Approach

The Hybrid Approach combines Collaborative and Content-Based Filtering to provide more accurate recommendations. The system uses a weighted combination of recommendations from both methods.

### Knowledge-Based Recommendations

Knowledge-Based Recommendations use genre information to recommend anime based on user preferences. The system uses TF-IDF vectorization and cosine similarity to find similar anime.

## Evaluation

The performance of each recommendation method is evaluated using Precision, Recall, F1-score, and Accuracy. The results are visualized using bar plots.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.



This README provides an overview of the Anime Recommendation System, including installation instructions, usage examples, and evaluation metrics. For more details, please refer to the code and comments in the respective Python scripts.
