# Embarrassingly Shallow Autoencoders for Sparse Data (EASE)

In this repository, we provide an implementation of the Collaborative Recommendation System **EASE**, following the article **[Embarrassingly Shallow Autoencoders for Sparse Data](https://arxiv.org/pdf/1905.03375)**.

### Additional Links
- Basic explanation and execution of the code in this **[YouTube Video](https://www.youtube.com/watch?v=CaB4iXd8s_Y)**.
- **Dataset:** [MovieLens Dataset](https://grouplens.org/datasets/movielens/) - Widely used benchmark dataset for recommendation systems.
- **DOI Reference for MovieLens Dataset Paper:** [DOI Reference MovieLens](https://doi.org/10.1145/2827872).

## About EASE (Embarrassingly Shallow Autoencoders for Sparse Data)

EASE (Embarrassingly Shallow Autoencoders for Sparse Data) is a simple and efficient collaborative filtering method for recommendation systems. 
Unlike deep learning models, EASE uses a shallow, linear structure to predict user-item interactions, making it computationally efficient and scalable for large, sparse datasets.

Key benefits:
- **Simplicity:** Easy to implement with minimal hyperparameter tuning.
- **Efficiency:** Solves a ridge regression problem in closed form.
- **Scalability:** Handles large-scale data effectively.

## Installing

### Pre Requisites

Clone the repository using
```bash
git clone https://github.com/thiago-shimada/ease-recsys.git && cd ease-recsys
```

Install all requirements with
```bash
pip install -r requirements.txt 
```

## Usage

To run the EASE algorithm, simply execute the provided Jupyter Notebook:
1. Open the Notebook
```bash
jupyter notebook ease.ipynb
```
2. Inside the notebook, you will:
- Import the dataset.
- Preprocess the data.
- Train the EASE model.
- "Train" the other reccomendation algorithms
- Evaluate its performance.
Ensure you follow the sequential code cells in the notebook to reproduce the results.

## Dataset

To test the algorithms and compare results, the MovieLens dataset was used, which consists of user ratings for movies. It is a widely used benchmark dataset for recommendation system research, containing:
- **Users:** Users identified by unique IDs.
- **Movies:** Information about movies, including titles, genres, tags and other metadata.
- **Ratings:** User-provided ratings on a scale (1 to 5), indicating their preferences for specific movies.

## Implemented Algorithms

| **Model**              | **Description**                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------|
| EASE                   | Embarrassingly Shallow Autoencoders for Sparse Data.                                      |
| UserKNN                | User-based k-nearest neighbors approach for collaborative filtering.                      |
| ItemKNN                | Item-based top-N recommendation algorithm.                                                |
| ItemAttribute (Tag)     | Item-based recommendation using tags as attributes.                                      |
| ItemAttribute (Genre)   | Item-based recommendation using genres as attributes.                                    |

### Metrics Summary Table

| **Metric**    | **Description**                                                                 |
|---------------|---------------------------------------------------------------------------------|
| MAP@10        | Precision of ranked relevant items in the top-10 recommendations.             |
| RECALL@10     | Proportion of relevant items successfully recommended in the top-10.           |
| PRECISION@10  | Proportion of relevant items within the top-10 recommendations.               |
| NDCG@10       | Ranking quality considering relevance and position of top-10 recommendations. |


## Results

Below is a table summarizing the performance of EASE compared to baseline methods:

| **Method**            | **MAP@10** | **RECALL@10** | **PRECISION@10** | **NDCG@10** |
|------------------------|------------|---------------|------------------|-------------|
| EASE                  | 0.500151   | 0.561554      | 0.190559         | 0.613284    |
| UserKNN               | 0.481937   | 0.535752      | 0.181939         | 0.593925    |
| ItemKNN               | 0.466341   | 0.526220      | 0.178440         | 0.580364    |
| ItemAttribute (Tag)   | 0.271000   | 0.285861      | 0.098413         | 0.365783    |
| ItemAttribute (Genre) | 0.197262   | 0.206168      | 0.072867         | 0.276307    |

The results show that EASE achieves the best performance across all evaluation metrics (MAP@10, RECALL@10, PRECISION@10, and NDCG@10), demonstrating its effectiveness in recommendation tasks compared to traditional collaborative filtering methods like UserKNN and ItemKNN, as well as attribute-based methods.


This updated version includes the YouTube link for a comprehensive understanding and practical demonstration of the code.


