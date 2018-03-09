# Book-Reviews-of-Practical-Statistics-for-Data-Science

In total, this is a very good book for statisticans who want to get into the area of data science. This book provides us a new point of view to look at most traditional data science problems: EDA, A/B testing, predictive modelling and unsupervised learning. I will list some important thoughts and methods I learned from this book below.

1. Data Visualization: This book recommended two very nice plots which are new to me: hexagon binning plot and violin plot. Hexagon binning plot groups the data points (records) into hexagonal grids with a color indicating the number of data points. When dealing with big data problems in which you have millions of data, the traditional scatter plot will be useless and you need to rely on hexagon plot to figure out the relationship between two numeric variables. When you want to visualize the categorical variables, the violin plot could help to show the distrbution of data within each categories and show the relationship among each categories simultaneously, which provided more information than traditional boxplot.

2. Thoughts of Permutation test: In our traditional A/B testing methods, we have to set assumptions first and make sure our data follows the assumptions. For example, t-test has a minimum sample size requirement and it needs data to follow normal distribution. However, with the thoughts of permutation test, we are no longer restricted. Permutation test could be regarded as using the defintion of the statistics. For example, the definition of 90% confidence interval is that if you do a great number of bootstarp, 90% of the result will be located within the area. In permutation test, we do repeat the same things to figure out the statistics (eg. t-statistics, p-value). For example, if you want to know whether or not the difference between two groups is significant. You first combine two groups into one data set and then shuffle it. After shuffling, you need to divided the dataset again into two groups whose sizes are equal to the initial groups. Then, calculate the difference and record it. repeat those steps thousands of times, you will get a distribution of the difference. Then, by looking at the location of your initial difference in this distribution, you could get the p-value. Thoughs of permutation test could be used in a very wide range. It is really a good tool.

3. Categorical vairables encoding: I used to use one-hot encoding only, but after reading this book, I find some new methods to encode categorical vairables. As we know one-hot has lots of disadvantages. For example, if the levls of categorical variable is too high (like zipcode), it will be reduce the degree of freedom greatly and make it unfeasible to build a reasonable model. Here, this book told me another way, you could first build a naive model without categorical variable and then use the mean or median residual of data in each level of categorical variables to encode it. But this method still has some problems. I think we may need to rely on deep learning in a more accurate encoding.

4. KNN and clustering in feature engineering and data generation: This is another new thought for me. I never used KNN and clustering algorithms in feature engineering before. I thought they may lead to multicollinearity! However, this book told me the KNN and clustering algorithms (like K-means) only consider the local information for each data points, thus it won't cause multicollinearity! I tried to use KNN to build a new feature in some data challenge and find it does increase the model performance! By the way, the same thought also helps in imbalanced data problems. We usually do upsampling to make the dataset balanced. We could also generate new data by using KNN according to this book! For example, the dataset has 10000 points with y = 0 and 100 with y = 1, we could find k nearest points whose y = 1 for each data points with y = 1 and calculate the weighted mean of those k points. This weighted mean could be added into our original dataset.

However, This book also has some drawbacks. It focus on the practice of concepts and hardly analyze the theory for diffcult concepts. For example, it introduced XGBoost to us and told us how to code in R to use XGBoost algorithm, but it never told us how XGBoost works. I have to google Tianqi Chen's paper and PPT to have a deep understanding of Gradient Boosting Tree, which is unfriendly to novice.

In conclusion, this is a very good book for those people with statistical background who want to step into the area of data science. You could review the foundamental statistics from the aspect of data scientist and learn the major algorithms step by step. If you already finished some relevant courses like Andrew Ng's Machine Learning, you could read this book and gain a deeper understanding of what you have learned.

Thanks to Peter Bruce and ANdrew Bruce for this excellent book!

Sheng
