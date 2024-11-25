# Embarrassingly Shallow Autoencoders for Sparse Data (EASE)

In this repository, we show an implementation of the Collaborative Recommendation System **EASE**.

Following the article **[Embarrassingly Shallow Autoencoders for Sparse Data](https://arxiv.org/pdf/1905.03375)**.


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

