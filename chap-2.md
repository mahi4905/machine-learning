# Chapter 2: Types of Machine Learning

---

# Learning Objectives

After completing this chapter, you will be able to:

- Understand why Machine Learning is divided into different types.
- Explain Supervised Learning.
- Explain Unsupervised Learning.
- Explain Semi-Supervised Learning.
- Explain Reinforcement Learning.
- Identify which type of ML a real-world problem belongs to.

---

# Why Different Types of Machine Learning?

The type of Machine Learning depends on **what kind of data we have**.

The biggest question is:

> **Do we already know the correct answer (label)?**

If yes → Supervised Learning

If no → Unsupervised Learning

If only some data has labels → Semi-Supervised Learning

If an agent learns by interacting with an environment → Reinforcement Learning

---

# Overview

```
Machine Learning
│
├── Supervised Learning
├── Unsupervised Learning
├── Semi-Supervised Learning
└── Reinforcement Learning
```

These are called **Learning Paradigms**.

---

# 1. Supervised Learning

## Definition

Supervised Learning is a type of Machine Learning where the model learns using **labeled data**.

A label is the correct answer we want the model to learn.

---

## Example

Suppose we want to predict whether a student will pass.

| Hours Studied | Attendance | Passed |
|---------------|------------|---------|
|2|60%|No|
|4|75%|No|
|6|85%|Yes|
|8|95%|Yes|

Notice that we already know the answer.

```
Features
     +
Correct Answer(Label)
         ↓
Model Training
         ↓
Prediction
```

---

## Components

Features (Input)

```
Hours Studied
Attendance
```

Label (Output)

```
Passed
```

---

## Goal

Learn a mapping:

```
Input
    ↓
Model
    ↓
Output
```

The model learns from examples.

---

# Types of Supervised Learning

There are two major categories.

---

## A. Regression

Output is a **continuous numerical value**.

Examples

House Price

```
₹ 52,75,000
```

Temperature

```
34.5°C
```

Salary Prediction

```
₹12,40,000
```

Examples

- House Price Prediction
- Salary Prediction
- Rainfall Prediction
- Stock Price Prediction

Algorithms

- Linear Regression
- Ridge Regression
- Lasso Regression

---

## B. Classification

Output is a category.

Examples

```
Spam
Not Spam
```

```
Yes
No
```

```
Cat
Dog
Horse
```

Examples

- Disease Prediction
- Email Spam Detection
- Face Recognition
- Fraud Detection

Algorithms

- Logistic Regression
- Decision Tree
- Random Forest
- SVM
- KNN
- Naive Bayes
- XGBoost

---

# Regression vs Classification

| Regression | Classification |
|------------|---------------|
| Predicts numbers | Predicts categories |
| Output is continuous | Output is discrete |
| Example: House Price | Example: Spam Detection |

---

# 2. Unsupervised Learning

## Definition

Unsupervised Learning uses **unlabeled data**.

There are no correct answers.

The algorithm tries to discover hidden patterns.

---

## Example

Customer information

| Age | Salary |
|------|---------|
|22|30000|
|25|35000|
|50|100000|
|55|120000|

Notice something?

There is NO column like

```
Customer Type
```

The algorithm finds groups automatically.

```
Customer Data

↓

Algorithm

↓

Group A
Group B
Group C
```

---

# Main Tasks

## Clustering

Grouping similar data.

Examples

- Customer Segmentation
- Friend Suggestions
- Product Grouping

Algorithms

- K-Means
- Hierarchical Clustering
- DBSCAN

---

## Dimensionality Reduction

Reduce the number of features while preserving useful information.

Suppose we have

```
100 Features
      ↓
PCA
      ↓
10 Features
```

Benefits

- Faster training
- Less storage
- Better visualization

Algorithms

- PCA
- t-SNE
- UMAP

---

# Supervised vs Unsupervised

| Supervised | Unsupervised |
|------------|--------------|
| Has labels | No labels |
| Learns input → output mapping | Finds hidden patterns |
| Used for prediction | Used for exploration |

---

# 3. Semi-Supervised Learning

## Definition

Some data has labels.

Most data has no labels.

Example

Suppose we have

```
10,000 Images

Only 500 are labeled.
```

Instead of labeling all images manually,

we use Semi-Supervised Learning.

```
Small Labeled Dataset

+

Large Unlabeled Dataset

↓

Model
```

---

## Why Use It?

Labeling data is expensive.

Examples

- Medical Images
- Satellite Images
- Research Data

---

# 4. Reinforcement Learning

## Definition

An agent learns by interacting with an environment.

Instead of labels,

it receives rewards and penalties.

---

## Components

```
Agent

↓

Action

↓

Environment

↓

Reward

↓

Learn Better Action
```

---

## Example

Robot Learning

```
Move Left

Reward = +10
```

```
Hit Wall

Reward = -5
```

Eventually,

the robot learns the best actions.

---

## Examples

- Self-driving Cars
- Robotics
- Chess
- AlphaGo
- Game Playing

---

# Comparison

| Type | Labels | Goal |
|------|--------|------|
| Supervised | Yes | Predict output |
| Unsupervised | No | Discover patterns |
| Semi-Supervised | Few | Improve learning using unlabeled data |
| Reinforcement | Rewards | Learn best actions |

---

# Which Algorithms Belong Where?

## Supervised

- Linear Regression
- Logistic Regression
- Decision Tree
- Random Forest
- SVM
- KNN
- Naive Bayes
- XGBoost

---

## Unsupervised

- K-Means
- Hierarchical Clustering
- DBSCAN
- PCA

---

## Reinforcement

Examples

- Q-Learning
- SARSA
- Deep Q Networks (DQN)

---

# Real-World Examples

| Problem | Learning Type |
|----------|---------------|
| House Price Prediction | Supervised (Regression) |
| Student Pass/Fail Prediction | Supervised (Classification) |
| Spam Detection | Supervised (Classification) |
| Customer Segmentation | Unsupervised |
| Movie Recommendation (finding similar users/items) | Often Unsupervised |
| Robot Navigation | Reinforcement |
| Self-driving Car Decision Making | Reinforcement |
| Medical Images with only a few labels | Semi-Supervised |

---

# Decision Tree to Identify the Learning Type

```
Do you have labels?

        │
    ┌── Yes ───────────────┐
    │                      │
Output is a number?   Output is a category?
    │                      │
Regression          Classification

        │
        No
        │
Need to discover patterns?
        │
      Yes
        │
Unsupervised Learning

        │
Only a few labels?
        │
      Yes
        │
Semi-Supervised Learning

        │
Learning through rewards?
        │
      Yes
        │
Reinforcement Learning
```

---

# Interview Questions

1. What is Supervised Learning?
2. What is a label?
3. Difference between Regression and Classification?
4. Difference between Supervised and Unsupervised Learning?
5. What is Clustering?
6. What is Semi-Supervised Learning?
7. Why is Semi-Supervised Learning useful?
8. What is Reinforcement Learning?
9. Give three examples of each learning paradigm.
10. Is K-Means supervised or unsupervised? Why?

---

# Key Takeaways

- Machine Learning is divided based on **how the model learns**.
- **Supervised Learning** uses labeled data.
- **Regression** predicts continuous values.
- **Classification** predicts categories.
- **Unsupervised Learning** uses unlabeled data to discover hidden patterns.
- **Semi-Supervised Learning** combines a small labeled dataset with a large unlabeled dataset.
- **Reinforcement Learning** learns through rewards and penalties.
- Choosing the correct learning paradigm is the first step before selecting an algorithm.
