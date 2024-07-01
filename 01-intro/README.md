
# LLM Zoomcamp Homework 1

This folder contains the solution for Homework 1 of the LLM Zoomcamp. The purpose of this homework is to learn more about searching information through several documents and practice using Elasticsearch.

## Contents

- `homework.ipynb`: Contains the solution to the homework.
- `elasticsearch.ipynb`: An introductory notebook exploring and documenting various types of queries and clauses used in Elasticsearch.
- `data/books.json`: A JSON file with examples of "book" documents for use in the `elasticsearch.ipynb` tutorial. The structure of the documents is as follows:

    ```json
    {
        "id": 1,
        "book": "Astronomy",
        "book_name": "Cosmos",
        "edition": "1st",
        "author": "Carl Sagan",
        "publication_year": 1980,
        "publication_month": 9,
        "publication_day": 1
    }
    ```

    The file contains 30 books.

- `requirements.txt`: Contains the libraries required to run the notebooks.

## Setup

To set up the environment and run the notebooks, follow these steps:

1. Install the required libraries:

    ```bash
    pip install -U pip && pip install -r requirements.txt
    ```

2. Launch Elasticsearch using Docker:

    ```bash
    docker run -it \
        --rm \
        --name elasticsearch \
        -p 9200:9200 \
        -e "discovery.type=single-node" \
        -e "xpack.security.enabled=false" \
        docker.elastic.co/elasticsearch/elasticsearch:8.4.3
    ```

With Elasticsearch running, you can explore the notebooks and complete the homework.
