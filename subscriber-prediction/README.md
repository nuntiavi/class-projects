# Music Streaming Premium Subscriber Prediction

**Task:** Create a model to predict which users on Website XYZ, a music-listening social networking website, will convert to a premium subscriber within the next 6 months.

**Measurement:** As it's a highly unbalanced dataset, F-1 score.

**Model used:** After testing multiple statistical and machine learning models, GBDT (gradient-boosted decision tree) performed best.

**Assignment Result:** Model predictions were uploaded to a class competition on Kaggle. Our group's project won first place.

#### Methodology:
**1. Feature Engineering**
- Added some features that were ratios between various variables
- As it's GDBT, I left all features in the model.

**2. Data Preparation**
- Split train/validation data
- Create another version of the train data where the classes are both over and under sampled, so that I have a balanced dataset.
- Train models on both the original and balanced dataset

**3. Parameter tuning**
- Use caret to choose the best parameter for each training set
- Use AUC on the training data to determine which model is best (the F score is wrong)

**4. Model creation**
- Plug in the parameters to create a model (sometimes this wasn't right because caret used AUC on training data, so I still played around with it)
- Create model with best AUC

**5. Determine decision boundary / threshold**
- Test different decision boundaries to work out which one gives the best F1 and accuracy

**6. Run on Test Data**
- With the model and decision boundary, plug it into the test data and create the file for submission.

- In the end the balanced over/under sampled model had better F1 so I only submitted that.
