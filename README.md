# JewelID: Similarity Search for Jewelry Images

Similarity Search for Jewelry Images using **Vision Transformer (ViT-base)** for _feature extraction_ and **FAISS** for _indexing and searching_.

## Overview

- Scraped around 10,000 images of various jewelry products such as rings, bracelets, earrings, chains.
- Extracted the features of the images using ViT.
- Used FAISS for storing and indexing the vector embeddings and for efficient retrival of the embeddings.
-  Retrieved the top 5 similar images for the query.
-  Visualized the attention map of the query image to find out where the ViT model focuses on.

## FAISS

- Implemented two different indices: FlatIndex and PQIndex (Product Quantization).
- The results of both indices are given below:

|Index|Memory|Time|
|-----|------|----|
|Flat|29316141 B|3.64ms|
|PQ|862862 B|2.32ms|

PQ has *memory reduction* of **97.1%** and a *speed-up* of **36.2%.**

## Example Inference
An example query image is given and its corresponding similar images with their distances are given below:
![download](https://github.com/user-attachments/assets/c0021291-92b9-4654-9d74-1329d85aebf3)

The attention map of the query image is also attached below:
![download](https://github.com/user-attachments/assets/02ce4c02-adca-49cf-b397-a51a7044345e)

