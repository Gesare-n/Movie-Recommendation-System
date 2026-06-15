# Production-Grade Movie Recommendation System

## Project Overview
This project implements an industry-standard movie recommendation engine designed to enhance user engagement and retention on digital entertainment platforms. By leveraging advanced supervised modeling techniques, including Collaborative Filtering (SVD), Content-Based Filtering, and Neural Collaborative Filtering (NCF), the system provides highly personalized movie suggestions that address the "choice paralysis" and "cold start" challenges common in the streaming industry.

## Key Features
- **Hybrid Recommendation Engine**: Combines the behavioral insights of Collaborative Filtering with the attribute-based precision of Content-Based Filtering.
- **Advanced Evaluation Metrics**: Utilizes NDCG@10 (Normalized Discounted Cumulative Gain) and Precision@K to measure ranking effectiveness, moving beyond simple rating accuracy (RMSE).
- **Temporal Validation Strategy**: Implements a time-based train-test split to ensure model performance on future, unseen data, simulating a real-world production environment.
- **Deep Learning Baseline**: Introduces Neural Collaborative Filtering (NCF) using PyTorch to capture complex, non-linear user-item interactions.
- **Cold Start Solution**: Employs movie metadata (genres and tags) to provide intelligent recommendations for new content and users with sparse history.

## Repository Structure
```
.
├── Industry_Standard_Recommendation_System.ipynb  # Main project notebook with analysis and modeling
├── ml-latest-small/                               # Dataset directory (MovieLens 100k)
│   ├── links.csv
│   ├── movies.csv
│   ├── ratings.csv
│   ├── tags.csv
│   └── README.txt
└── README.md                                      # Project documentation
```

## Getting Started
### Prerequisites
Ensure you have the following Python packages installed:
- `pandas`
- `numpy`
- `scikit-learn`
- `scikit-surprise`
- `torch`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Movie-Recommendation-System.git
   cd Movie-Recommendation-System
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn scikit-surprise torch
   ```

### Running the Project
Open the `Industry_Standard_Recommendation_System.ipynb` notebook in a Jupyter environment to view the full analysis, modeling process, and evaluation results.

## Data Source
The project uses the [MovieLens ml-latest-small dataset](https://grouplens.org/datasets/movielens/latest/), which contains 100,836 ratings and 3,683 tag applications across 9,742 movies by 610 users.

## Evaluation Results
| Metric | SVD Model Performance |
| :--- | :--- |
| **RMSE** | 0.8775 |
| **NDCG@10** | 0.8558 |

## Business Impact
- **Increased Engagement**: Personalized discovery leads to longer user sessions.
- **Reduced Churn**: Relevant recommendations improve subscriber satisfaction and retention.
- **Content ROI**: Ensures new and niche content is discoverable, maximizing the value of the entire library.

## Future Roadmap
- **Real-time Optimization**: Implementing streaming data pipelines for instant profile updates.
- **Model Explainability**: Integrating tools like LIME to provide transparent "Why this was recommended" features.
- **Enterprise Scalability**: Transitioning to cloud-based Spark environments for global-scale deployment.


