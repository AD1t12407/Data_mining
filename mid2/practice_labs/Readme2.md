# Desicion Tree Classifier
### Refer: https://medium.com/@enozeren/building-a-decision-tree-from-scratch-324b9a5ed836#:~:text=To%20create%20our%20tree%20from,develop%20a%20%E2%80%9Cpredict%E2%80%9D%20function.&text=In%20the%20Image%202%20above,we%20need%20for%20our%20class.

# Decide What is a Good Split
The main idea for training a decision tree is about how you will split your data. The best split is basically a split where after spliting each split has data points where every data point has the same class. We should define a numerical metric that gives this property. In this implementation we will use entropy metric
![Alt text](/image.png)
### Decision Trees in Regression and Classification:

#### 1. Information Gain with Graph:
   - **Information Gain:** Information gain is a measure of how much a particular attribute contributes to reducing uncertainty in the dataset. It helps in deciding which attribute to split on.
   - **Graphical Representation:** Visualizing information gain through a graph can aid in selecting attributes for node splitting.
   - **Example:** In a dataset of customers, information gain can help decide which feature (e.g., income, age) is most useful for splitting customers into groups.

#### 2. C5.0 Algorithm:
   - **C5.0 Algorithm:** An enhancement over ID3, C5.0 is versatile, handling both categorical and continuous data.
   - **Attributes:** Employs information gain to determine the best attributes for splitting.
   - **Application:** Widely used in data mining and machine learning for decision tree construction.
   
#### 3. Gini Index:
   - **Gini Index:** A measure of impurity in a set of data. It quantifies the likelihood of misclassifying an element chosen randomly.
   - **Usage:** Used in decision tree algorithms like CART for assessing node purity.
   - **Example:** In a binary classification task, Gini Index is used to evaluate how often a randomly chosen element would be incorrectly classified.

#### 4. CART Algorithm:
   - **CART Algorithm:** Stands for Classification and Regression Trees. Utilizes the Gini Index for classification tasks and the sum of squared residuals for regression.
   - **Applications:** Used in scenarios requiring both classification and regression, such as predicting customer satisfaction (regression) and classifying spam emails (classification).

#### 5. Sum of Squared Residuals:
   - **Low SSR:** Indicates a good fit of the model to the data, with smaller prediction errors.
   - **High SSR:** Suggests a poor model fit, as the predictions deviate significantly from the actual values.
   - **Example:** In a housing price prediction model, low SSR means the model accurately estimates house prices based on features like square footage and location.

#### 6. Recursive Portioning:
   - **Recursive Portioning:** The process of repeatedly dividing a dataset into subsets based on selected attributes.
   - **Application:** Recursive portioning is fundamental to decision tree construction, as it efficiently creates a hierarchical structure.
   - **Example:** In a medical diagnosis system, recursive portioning might split patient data based on symptoms to identify potential diseases.

#### 7. When to Stop Recursive Portioning:
   - **Criteria:** The decision to stop recursive portioning can be based on factors like maximum depth, minimum samples per leaf, or impurity measures.
   - **Example:** In fraud detection, stopping recursive portioning early may prevent overfitting and ensure a more generalized model.

#### 8. Pre-pruning and Post-pruning:
   - **Pre-pruning:** Halting the growth of the tree before it becomes overly complex.
   - **Post-pruning:** Trimming the fully grown tree to enhance simplicity and reduce overfitting.
   - **Example:** Pre-pruning may involve limiting the maximum depth of the tree, while post-pruning might prune branches with negligible contributions to accuracy.

#### 9. Tree Score:
   - **Larger Trees:** Larger trees may capture more details but are prone to overfitting.
   - **Balancing Act:** Achieving a balance between complexity and accuracy is crucial for optimal model performance.
   - **Example:** In a stock price prediction model, a too-complex tree might capture noise rather than the actual trends in the market.

#### 10. Constant Complexity Score:
   - **Constant Complexity Score:** Balances model complexity with predictive power, avoiding unnecessary intricacies.
   - **Example:** In a credit scoring model, maintaining a constant complexity score ensures that the model doesn't rely on irrelevant or overly specific features.

#### 11. Regression Tasks vs. Classification Tasks:
   - **Regression:** Minimizing the Sum of Squared Residuals (SSR) is crucial for accurate predictions.
   - **Classification:** Minimizing impurity, often measured by the Gini Index, is essential for creating pure class nodes.
   - **Example:** Predicting house prices (regression) vs. classifying emails as spam or not (classification).

#### 12. Pre-running and Post-running:
   - **Pre-running:** Tuning hyperparameters before tree construction to optimize model performance.
   - **Post-running:** Fine-tuning parameters after initial construction for further optimization.
   - **Example:** Pre-running might involve adjusting the maximum depth of the tree, while post-running could involve pruning or adjusting the minimum samples required for a split.

#### 13. Ideal Values for Hyperparameters:
   - **Max Depth:** Balancing model complexity and overfitting. Ideal values depend on the dataset and task.
   - **Min Samples Split:** Minimum samples required to split a node, preventing overfitting.
   - **Example:** In a spam classification model, an ideal max depth prevents overly complex decision rules, while an appropriate min samples split ensures meaningful splits.

#### 14. get_dummies():
   - **get_dummies():** A function to convert categorical variables into dummy or indicator variables.
   - **Application:** Essential for handling categorical data in decision tree models that require numerical input.
   - **Example:** Converting categorical variables like "gender" into dummy variables (0 or 1) for a decision tree predicting customer preferences.

#### 15. Random State:
   - **Random State:** A seed for random number generation ensures reproducibility in model training.
   - **Effect:** Changing the random state can lead to different data splits, affecting model outcomes.
   - **Example:** In a churn prediction model, setting a random state ensures consistent results when evaluating different hyperparameters.

#### 16. MAE (Mean Absolute Error) Effect:
   - **MAE:** Measures the average absolute errors between predicted and actual values.
   - **Effect:** Higher MAE indicates larger errors in predictions, impacting the overall accuracy of the model.
   - **Example:** In a weather forecasting model, a higher MAE implies a less accurate prediction of temperature.

#### 17. MSE (Mean Squared Error):
   - **MSE:** Ideal MSE is 0, indicating perfect predictions without any error.
   - **Evaluation:** Measures the average squared difference between predicted and actual values.
   - **Example:** In a stock price prediction model, a lower MSE signifies more accurate predictions, minimizing the squared differences between predicted and actual prices.