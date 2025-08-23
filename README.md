## CS:GO Round Winner Classification Using ML

### Project Overview

This project aims to predict the **winner of a round in the game Counter-Strike: Global Offensive (CS:GO)** using a dataset of in-game snapshots. By analyzing a wide range of features such as player health, armor, money, weapon counts, and grenade inventory for both Counter-Terrorist (CT) and Terrorist (T) teams, the goal is to develop a machine learning model that can forecast the round's outcome. This is a valuable tool for e-sports analysis and game strategy.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - CS:GO Round Winner Classification](https://www.kaggle.com/datasets/christianlillelund/csgo-round-winner-classification)
  * **Size**: 122,410 entries, 97 columns. After data cleaning (dropping duplicates), the dataset size is 117,448.
  * **Key Features**:
      * A large number of features representing the state of the game at a specific moment in a round, including `ct_health`, `t_health`, `ct_armor`, `t_armor`, `ct_money`, `t_money`, and the number of various weapons and grenades for each team.
  * **Approach**:
      * **Data Cleaning**: Dropped duplicate rows.
      * **Exploratory Data Analysis**: Histograms, boxplots, and a heatmap were used for visualization to understand data distributions and correlations. The heatmap was used to identify and drop highly correlated features.
      * **Feature Selection**: Dropped three highly correlated columns (`t_helmets`, `ct_players_alive`, `t_players_alive`) to reduce multicollinearity.
      * **Label Encoding**: Applied to all columns, including categorical features like `map` and the target `round_winner`.
      * **Binary Classification**: The target variable `round_winner` indicates whether the Terrorist team (`T`) or Counter-Terrorist team (`CT`) wins the round.
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **87.2%** with Random Forest Classifier.
      * **84.3%** with Bagging Classifier.
      * **81.5%** with Decision Tree Classifier.

-----

### Purpose and Applications

  * **Predict the winner of CS:GO rounds** for e-sports analytics and broadcasting.
  * Provide strategic insights to professional teams by identifying key factors that lead to round wins.
  * Develop an in-game assistant for players to make more informed decisions about resource management and play styles.
  * Serve as a foundational model for analyzing and understanding complex team-based game dynamics.

-----

### Installation

Clone the repository:

```bash
git clone hhttps://github.com/BhaveshBhakta/CS-GO-Round-Winner-Classification-Using-ML.git
cd CS-GO-Round-Winner-Classification-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for all models to achieve optimal performance.
  * Exploring more robust strategies for handling the large number of features, such as advanced feature selection or dimensionality reduction techniques.
  * Investigating the impact of different preprocessing methods, especially given the continuous and discrete nature of the features.
  * Adding explainability (e.g., SHAP or LIME) to understand which game factors are the most critical predictors of a round's outcome.
