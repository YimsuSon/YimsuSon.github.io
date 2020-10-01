---
title: 4.Model Overfitting
excerpt: Computer Science


#최상위 사진
header:
  image: /assets/images/foo-bar-identity.jpg
  teaser: /assets/images/foo-bar-identity-th.jpg

gallery:
  - url: /assets/images/unsplash-gallery-image-1.jpg
    image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
  - url: /assets/images/unsplash-gallery-image-3.jpg
    image_path: assets/images/unsplash-gallery-image-3-th.jpg
    alt: "placeholder image 3"
    


 #사이드바 설정 
sidebar:
  - title: "Role"
    nav: sidebar-sample

# 해당 글 목차
toc: true
toc_sticky: true

toc_label: "Yimsu's Blog"
toc_icon: "cog"


## 테그설정

categories:
  - DataMining

tags:
  - DataMining
  - "2020"
  - "2020.09"



---

### 1.Model Overfitting
    - Reason for Model Overfitting

        - Limited Training Size

        - High Model Complexity

            - Multiple Comparison Procedure

    - Classification Errors

        - Training errors (apparent errors)
            - Errors committed on the training set

        - Test errors
            - Errors committed on the test set

        - Generalization errors
            - Expected error of a model over random selection of records from same distribution


    - Effect of Multiple Comparison Procedure
        - Consider the task of predicting whether stock market will rise/fall in the next 10 trading days

        - Random guessing:
            - P(correct) = 0.5

        - Make 10 random guesses in a row:

    - Approach:
        - Get 50 analysts
        - Each analyst makes 10 random guesses
        - Choose the analyst that makes the most number of correct predictions

    - Probability that at least one analyst makes at least 8 correct predictions

    - Many algorithms employ the following greedy strategy:
        - Initial model: M
        - Alternative model: M’ = M ∪ γ,    where γ is a component to be added to the model (e.g., a test condition of a decision tree)
        - Keep M’ if improvement, Δ(M,M’) > α

    - Often times, γ is chosen from a set of alternative components, Γ = {γ1, γ2, …, γk}

    - If many alternatives are available, one may inadvertently add irrelevant components to the model, resulting in model overfitting


    - Notes on Overfitting

        - Overfitting results in decision trees that are more complex than necessary

        - Training error does not provide a good estimate of how well the tree will perform on previously unseen records

        - Need ways for estimating generalization errors


### 2.Model Selection
    - Using Validation Set
    - Incorporating Model Complexity
    - Estimating Statistical Bounding
    - Model Selection for Decision Trees


### 3.Model  Evaluation 