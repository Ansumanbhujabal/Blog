---

Data Standardization in ML
Basic process for data standardization for ML

Data standardization is a crucial preprocessing step in machine learning. It involves transforming our dataset to have a consistent scale and distribution, which can improve the performance of many machine learning algorithms.
In simple term it means processing our data into a common format before feeding it to machine learning algorithm.

The two common techniques for data standardization are Min-Max scaling and z-score normalization.
Min-Max Scaling: Min-Max scaling transforms our data into a specific range, usually [0, 1]. It linearly scales the data, so the minimum value becomes 0, and the maximum value becomes 1, while all other values are scaled proportionally in between.
Z-Score Normalization (Standardization): Z-score normalization transforms our data so that it has a mean of 0 and a standard deviation of 1. This method is particularly useful when your data follows a normal distribution.
Here are the steps in brief for data standardization.
Finding Data Standard Deviation:

print(dataset.data.std()) // If o/p is 1 , then no devation

2. Standard Scaler:
from sklearn.preprocessing import StandardScaler// Import
scaler= StandardScaler()// Initialization

3.Data fitting and Standardization:
Fit the scaler to your training data, and then transform both the training and test data using the fitted scaler. This step calculates the mean and standard deviation from the training data and applies the same transformation to both sets.
scaler.fit(x_train)

4. Data Transformation:
x_train_standardized= scaler.transform(x_train)

5.Data Standardizing of test based on train :
Use the same scaler that you fitted on the training data to standardize the test data. This ensures that the scaling parameters (mean and standard deviation) are consistent between the training and test sets.
x_test_standardized= scaler.transform(x_test)

6.Checking Standard Deviation
print(x_train_standardized.std())
print(x_test_standardized.std())

By following these steps, you ensure that your data is standardized (mean-centered and scaled) for use in machine learning models, making it easier for algorithms to converge and perform effectively, especially when they are sensitive to feature scales.
from sklearn.preprocessing import StandardScaler

# Assuming you have your dataset loaded as x_train and x_test

# Step 1: Initialization
scaler = StandardScaler()

# Step 2: Data Fitting and Standardization for the training set
scaler.fit(x_train)
x_train_standardized = scaler.transform(x_train)

# Step 3: Data Standardization of the test set based on the training set
x_test_standardized = scaler.transform(x_test)

# Step 4: Checking Standard Deviation
print(x_train_standardized.std())
print(x_test_standardized.std())
Conclusion: Data Gets a Makeover

In the dazzling world of machine learning, even data deserves a makeover. Data standardization is like dressing up your dataset for a fancy soirée. It's all about giving your numbers a fresh coat of paint and ensuring they waltz into the world of algorithms looking their best.
Picture this: your data, once a wild jungle of numbers, now marches in wearing tuxedos and ball gowns, thanks to Min-Max scaling and Z-Score normalization. The rowdy outliers have been tamed, and everyone's dancing to the same beat, be it [0, 1] or the rhythmic heart of a mean 0 and standard deviation 1.
But don't just take my word for it; the data itself can vouch for its transformation. It boasts about its newfound uniformity, flashing a standard deviation of 1 like a badge of honor.
So, remember, before you let your algorithms loose on your dataset, treat it to a spa day of standardization. Your models will thank you for the harmonious dance they'll perform.
Stay Standardized, Data Enthusiasts!

---

Connect with Me on GitHub and LinkedIn
If you found this journey through data standardization as fascinating as I did, let's connect! You can explore the code and examples discussed in this blog on my GitHub repository. Also, if you're interested in more data-related insights and machine learning adventures, follow me on LinkedIn.
GitHub | LinkedIn
Let's dive deeper into the data-driven world together!
