## Desicion Tree Classifier
# Refer: https://medium.com/@enozeren/building-a-decision-tree-from-scratch-324b9a5ed836#:~:text=To%20create%20our%20tree%20from,develop%20a%20%E2%80%9Cpredict%E2%80%9D%20function.&text=In%20the%20Image%202%20above,we%20need%20for%20our%20class.

# Decide What is a Good Split
The main idea for training a decision tree is about how you will split your data. The best split is basically a split where after spliting each split has data points where every data point has the same class. We should define a numerical metric that gives this property. In this implementation we will use entropy metric
![Alt text](/image.png)