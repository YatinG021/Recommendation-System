# Movie Recommendation System Using Matrix Factorization

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: YATIN GOGIA

*INTERN ID*: CT04DH1053

*DOMAIN*: MACHINE LEARNING

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTOSH

*DESCRIPTION* :

This Movie Recommendation System harnesses the power of matrix factorization, a widely utilized collaborative filtering technique, to generate personalized movie suggestions. Such systems are fundamental to streaming platforms, entertainment apps, and e-commerce portals, significantly improving user engagement through individualized recommendations.

## Dataset Overview

For this project, the popular MovieLens dataset from Kaggle is used, known for its extensive user–movie rating records. It contains both metadata for thousands of movies and millions of user ratings, making it ideal for building robust and scalable recommendation engines.

The dataset primarily consists of two files:

- **movies.csv**: Contains movie ID, title, and genre.
- **ratings.csv**: Records user-movie interactions, including user ID, movie ID, rating (1–5), and timestamp.

## Step-by-Step Implementation

### 1. Data Loading and Preprocessing

- Load the movies and ratings datasets using pandas.
- Handle missing values to ensure clean data.
- Convert data types appropriately for user IDs, movie IDs, and ratings.
- Merge movies metadata with ratings based on movie IDs for better interpretability.

### 2. Exploratory Data Analysis (EDA)

- Analyze rating distributions, unique users and movies count, and general popularity trends.
- Filter users or movies with too few ratings to reduce sparsity issues.

### 3. Building the User-Item Rating Matrix

- Construct a matrix with rows representing users and columns representing movies.
- Fill cells with user ratings; unrated entries are set as 0 or NA.
- This matrix is typically sparse and serves as input for matrix factorization.

### 4. Matrix Factorization – Core Algorithm

- Decompose the user-item matrix into two lower-dimensional matrices representing user and movie latent features.
- Multiply these matrices to estimate missing ratings.
- Methods like Singular Value Decomposition (SVD), Non-negative Matrix Factorization (NMF), or Alternating Least Squares (ALS) are commonly used.

### 5. Model Training

- Train the factorization model to minimize error (e.g., Root Mean Squared Error) between actual and predicted ratings.
- Use libraries such as `scikit-learn` for NMF or `surprise` for SVD implementations.

### 6. Generating Recommendations

- Predict ratings for unseen movies for a given user.
- Recommend top-scoring movies based on predicted preferences.
- Retrieve movie titles and genres by joining predictions with the original metadata.

### 7. Evaluation Metrics

- Assess model quality with metrics such as:
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
- Evaluate on a test set unseen during training to ensure generalization.

### 8. Visualization and User Interface

- Include plots showing rating distribution, popularity histograms, and performance metrics.
- Optionally, a user interface (CLI or notebook widgets) can offer real-time recommendations by user ID.

## Conclusion and Applications

This project demonstrates how matrix factorization can effectively transform complex user-movie relationships into actionable movie recommendations. The system is scalable and accurate, handling large and sparse datasets typical in real-world applications. It lays a solid foundation for developing recommender systems for movies, music, books, products, and more.

## Future Enhancements

- Incorporate content-based filtering with movie metadata.
- Develop hybrid recommendation models.
- Integrate implicit feedback like watch time or click data.
- Deploy the model via REST API or web application for broader access.

---

This repository provides a comprehensive, step-by-step approach to building and evaluating a collaborative filtering based Movie Recommendation System using matrix factorization techniques.
## OUTPUTS
## Top Movie Recommendations Table Output

_Displays the top 10 movie recommendations for a specific user. Each entry includes the movie ID and its title, generated based on the learned user preferences and predicted ratings._

<img width="610" height="199" alt="Image" src="https://github.com/user-attachments/assets/39f97eee-c8e8-4476-bd96-6ac771994501" />

## Learning Curve: RMSE Over Training Iterations

_Plots the RMSE (Root Mean Square Error) against the number of training iterations. This curve visualizes performance improvement and convergence of the matrix factorization model._

<img width="799" height="483" alt="Image" src="https://github.com/user-attachments/assets/869c3308-05a9-44a2-ba9f-6d632b9b652e" />

## Top 10 Movie Recommendations – Bar Plot Visualization

_Shows a horizontal bar chart of the top 10 recommended movies for the user, with predicted ratings on the x-axis and movie titles on the y-axis, providing a visual summary of the model’s recommendations._

<img width="1002" height="318" alt="Image" src="https://github.com/user-attachments/assets/e5fece9e-5622-499b-91cd-9af4e7ac1ebf" />



