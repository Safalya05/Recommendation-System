# Udacity Project: Recommendation System

## Introduction

### Project Motivation

In the IBM Watson Studio, there is a large collaborative community ecosystem of articles, datasets, notebooks, and other A.I. and ML. assets. Users of the system interact with all of this. Within this scope, we created this recommendation system project to enhance the user experience and connect them with assets. This personalizes the experience for each user.

### About the Project

For this project I am required to analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles that I think they will like. Below is an example what the IBM Watson Studio platform looks like, and how the interactions are collected.

![IBM Watson Studio Dashboard](dashboard.png)

Though the above dashboard is just showing the newest articles, we can imagine having a recommendation board available here that shows the articles that are most pertinent to a specific user.

In order to determine which articles to show to each user, I need to perform a study of the data available on the IBM Watson Studio platform.


## Getting Started

These instructions will give you a copy of the project up and running on your local machine for development and testing purposes. It is to be noted that this project has been done on Linux, so all these instructions might not work on MacOS or Windows. I will recommend searching for the corresponding Windows or MacOS commands.

### Dependencies

The project relies on standard Python data science libraries. The **primary** dependencies are listed below. A complete list of packages and their specific versions can be found in the `environment.yml` file.

```
Python>=3.8
Pandas
Numpy
Matplotlib
Scikit-learn
Jupyter Notebook
```

### Installation

It is highly recommended to use `conda` to manage your environment and dependencies, as they will ensure reproducibility. `conda` also is great with Data Science related projects.

1. **Install conda:**

If you're on Arch Linux, you can install conda using an AUR helper like paru or yay. To install conda, you can use the following commands:

```bash
paru -S miniconda3
```

Or

```bash
yay -S miniconda3
```

2. **Clone the repository:**

First of all, you will need to get a local copy of the repository. You can do so using `git`. Run the command in your terminal:

```bash
git clone https://github.com/SoumyabrataBanik/udacity-dsnd-recommendation-systems-project.git
```

This will create a directory named `udacity-dsnd-recommendation-systems-project` in your current directory. You can head into the directory using the command:

```bash
cd udacity-dsnd-recommendation-systems-project
```

3. **Create the conda environment:**

The `environment.yml` file contains all the necessary packages. This single command will create a new environment named `recsys` with everything you need.

```bash
conda env create -f environment.yml
```

4. **Activate the recsys environment:**

The `conda` environment created by the above command is named *recsys* (short for RECommendation SYStem). You can activate the environment using the command:

```bash
conda activate recsys
```

5. **Launch Jupyter Notebook:**

This project is done in the Jupyter Notebook. To launch Jupyter Notebook within the project directory, you must ensure that you're already within the project directory. Then simply run:

```bash
jupyter notebook .
```

and Jupyter Notebook starts in your default browser.

## Testing

The project includes a suite of predefined tests in the `project_tests.py` file in the top directory to verify the correctness of the implemented functions. The main notebook `Recommendations_with_IBM.ipynb` contains cells that call these tests.

### Break Down Tests

**1. Part I: Exploratory Data Analysis Validation (t.sol_1_test)**

This initial test serves as a crucial sanity check to ensure the dataset has been loaded and analyzed correctly. It validates the results of the initial Exploratory Data Analysis (EDA) by checking a dictionary of key statistics against a known solution.

**2. Part II: Rank-Based Recommender Test (t.sol_2_test)**

This test directly evaluates the core logic of the Rank-Based (or popularity-based) recommendation engine.

**3. Part III: User-Item Matrix Integrity Check**

This is a set of `assert` statements that validate the structure and content of the user-item interaction matrix, which is the foundational data structure for both collaborative filtering and matrix factorization.

**4. Part III: Collaborative Filtering Helper Function Tests**

This is a comprehensive test suite that uses a series of `assert` statements to validate the individual building blocks of the user-user collaborative filtering system.

**5. Part III: Advanced Collaborative Filtering Test (t.sol_5_test)**

This test validates the improved user-user collaborative filtering logic from the `get_top_sorted_users` function.

**6. Part IV: Content-Based Recommender Validation**

This test evaluates the recommendations generated by the content-based model, which relies on K-Means clustering of article titles.

**7. Part V: Matrix Factorization (SVD) Recommender Test**

This is the final test, which validates the recommendations generated by the Singular Value Decomposition (SVD) model.

## Project Instructions

The main deliverables for this project are contained within the Jupyter Notebook `Recommendations_with_IBM.ipynb`. The notebook is structured into five main parts:

1.  **Part I: Exploratory Data Analysis:** Load, inspect, and clean the user-item interaction data.
2.  **Part II: Rank-Based Recommendations:** Implement a function to recommend the most popular articles based on interaction counts.
3.  **Part III: User-User Based Collaborative Filtering:** Build a system to find similar users based on their interaction history and recommend articles liked by those neighbors.
4.  **Part IV: Content-Based Recommendations:** Use TF-IDF and K-Means clustering on article titles to recommend articles with similar content.
5.  **Part V: Matrix Factorization:** Use Singular Value Decomposition (SVD) to uncover latent features and make personalized recommendations based on this lower-dimensional representation.

Each part involves filling in functions and answering questions to demonstrate a comprehensive understanding of different recommendation strategies.

## Built With

*   [Python](https://www.python.org/) - The core programming language used.
*   [Pandas](https://pandas.pydata.org/) - For data manipulation and analysis.
*   [NumPy](https://numpy.org/) - For numerical operations, especially with matrices.
*   [Scikit-learn](https://scikit-learn.org/stable/) - For implementing TF-IDF, K-Means Clustering, and SVD.
*   [Matplotlib](https://matplotlib.org/) - For data visualization.
*   [Jupyter Notebook](https://jupyter.org/) - As the interactive development environment.

## License

[License](LICENSE.txt)
