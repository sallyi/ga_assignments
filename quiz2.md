#Machine Learning / SKLearn Quiz (Quiz 2)

1. Given the following machine learning matrix, fit each of the following algorithms into their respective places. Some may have multiple.

    .               | continuous          | categorical
    ---------------:|:--------------------|:-----------
    supervised      | regression          | classification
    unsupervised    | dimension reduction | clustering

    Algorithms:
    * Ordinary Least Squares - regression
    * Logistic Regression - classification
    * Naive Bayes - classification
    * Decision Trees - classification, regression
    * Support Vector Machines - classification, regression
    * Nearest Neighbors - classification
    * K Means - clustering
    * Principal Component Analysis (Matrix Decomposition) - dimension reduction

2. Given the 4 entities in the matrix above, describe a problem / example we worked on in class for each, and provide one idea on your own.

-regression - predicting brain size based on animal height
            - predicting ceo salary based on company financials

-classifications-predicting tweet sentiment based on language of the tweet
                -predicting gender of author based on their language use

-dimension reduction - collapsing similar features that don't need to be distinct, such as feel temperature and real temperature in the bikeshare data, image compression, personality tests
-speech recognition (collapsing phonemes that are interchangeable)


-clustering - figuring out iris class based on similarities without looking at the actual class label
            - clustering songs into genres based on similar features without knowing what they are up front (for recommendation systems)
            - text clustering 
            - user segmentation


3. All sklearn prediction objects have functions akin to fit(), transform(), predict(), and fit_transform(). Explain each in their most general terms.

fit() - input the training data (x) and turn it into a matrix
transform() - map the input matrix onto the y (target data of interest)
predict() - use the transformed data to predict the value or class of a new not-yet-seen input
fit_transform() - fits the x and transforms it onto the y in one step

3. Two of the above algorithms can use kernels (in their sklearn context)
    a. Explain what a kernel does - allows nonlinear data to be transformed into multiple dimensions in order to make it linear
    b. Which are the two algorithms that use kernels? - SVM, PCA

4. One of the above algorithms is most obviously not a linear solution to classification (it does not draw straight decision lines). Which algorithm is it, and how does it decide on decision lines?

Knn - it looks for a certain number of clusters (k) and tries to find the most central point (the mean) of all the clusters with the minimum distance to the rest of the points in the cluster

5. You are working on microarray (DNA) samples where number of features (n) is 5 and number of observations (m) is > 10,000.
    1. Describe a supervised and unsupervised technique in order to reduce the number of features in the samples to those that are most significant.  
    - PCA (unsupervised), 
    - lasso regression (L1)
    2. Compare the two techniques in their solution.

    PCA - finds the features that are most similar to eachother and merges them into some hybrid feature (a component?)
    lasso regression (L1) - eliminates features methodically based on a p-value threshold


6. Below is a table of Gini Importance (Normalized to 1) in predicting rent in New York City.
    1. Which algorithm uses Gini Importance? Decision Trees
    2. Interpret the table.

    Feature           | GiniImportance
    :-----------------|:--------------
    bedrooms          | 0.211
    bathrooms         | 0.005
    sqft              | 0.532
    distance subway   | 0.198
    distance columbus | 0.017
    nearby pizza      | 0.042

    Square footage has the most variance (information gain) when it comes to predicting rent. It would be useful to classify rent based on square footage but not so useful to classify based on distance to columbus.

7. What is the Receiving Operator Characteristic Curve? What two metrics is it composed of?

It shows the performance of a classifier, calculating its recall (the number of classifications it got right of all possible classifications) when the model is tuned at different thresholds. Used for binary classifications.

9. How does a grid search work? Use an example algorithm from above to help explain it.

SVM uses grid search to tune the hyperplane (finding the optimal split between the classes) by looking for the best set of parameters.

10. Three parts:
    1. What's your strongest "takeaway" from machine learning and this segment of the course?  
    I _really_ need to take a linear algebra class and need to work on my pandas skills.

    2. Given a 2 dimensional figure where y=effort to learn and x=immediate usefulness, and slope = 1, what is one algorithm that felt above the slope (more effort to learn than usefulness) and one algorithm that felt below the slope (more usefulness than effort to learn)?

    Above the slope - PCA, head explode, not sure how to use
    Below the slope - Naive Bayes, want to use it for text stuff

    3. What's one question you still have about machine learning?
    I have a lot of questions about the measurements used to evaluate machine learning but not sure where to begin.

