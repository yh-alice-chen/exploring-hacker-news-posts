# Exploring Hacker News Posts: Engagement Patterns in Ask HN and Show HN

## Introduction

[Hacker News](https://news.ycombinator.com) is a platform initiated by the startup incubator Y Combinator, where user-submitted stories receive votes and comments. The site is highly popular within technology and startup communities, and posts reaching the top listings can attract hundreds of thousands of visitors. This project explores two specific post categories: `Ask HN` and `Show HN`. `Ask HN` posts pose a specific question to the community; `Show HN` posts share a project, product, or item of interest.

## The Goal

The primary objective is to compare these two post categories to determine:

- Whether `Ask HN` or `Show HN` posts receive more comments on average
- Whether posts created at specific times receive more comments on average

## Data Source

The [dataset](https://dq-content.s3.amazonaws.com/356/hacker_news.csv) contains approximately 20,000 rows. It was derived from an [original dataset](https://www.kaggle.com/datasets/hacker-news/hacker-news-posts) of nearly 300,000 rows by filtering out submissions with zero comments and taking a random sample from the remaining entries.

## Repository Structure

```
├── exploring-hacker-news-posts.ipynb    # Main analysis notebook
├── hacker_news_dataset_cleaned.csv      # Hacker News dataset
└── README.md
```

## Data Analysis

The analysis separates posts into `Ask HN`, `Show HN`, and other categories, then calculates average comment counts for each. As `Ask HN` posts attract higher engagement, the temporal analysis — examining comment volume by hour of submission — focuses exclusively on this category.

## Conclusion

`Ask HN` posts receive an average of approximately 14.04 comments per post, compared to 10.32 for `Show HN` posts. The hour of submission has a significant influence on engagement. The top five hours for `Ask HN` comment volume are:

| Rank | Hour (EST) | Average Comments per Post |
|---|---|---|
| 1 | 15:00 | 38.59 |
| 2 | 02:00 | 23.81 |
| 3 | 20:00 | 21.53 |
| 4 | 16:00 | 16.80 |
| 5 | 21:00 | 16.01 |

To maximise community engagement, submissions should be categorised as `Ask HN` and published during the mid-afternoon window, specifically around 15:00 EST.

## Tools and Techniques

- **Language:** Python 3
- **Libraries:** Standard library only (`csv`, `datetime`)
- **Concepts applied:** Data cleaning, list and dictionary operations, string parsing, datetime formatting, nested loops, sorting lists of lists

## How to Run

1. Clone the repository
2. Ensure `hacker_news.csv` is in the same directory as the notebook
3. Open `exploring-hacker-news-posts.ipynb` in Jupyter Notebook or JupyterLab
4. Run all cells in order

## Source

Built as part of the Dataquest guided project series.
