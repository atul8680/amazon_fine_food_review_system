# amazon_fine_food_review_system

 This project is about study of amazon food reviews given by customers, and to predict whether a given review is positive or negative.
 Dataset for this project contains 500k reviews along with star rating(0-5), upvote and downvote.
 for training and testing purpose we have teken star rating as truth value of dataset, thus reviews with star rating > 3 considered as positive review while reviews with star rating < 3 are considered as negative review. reviews with star rating = 3 are discarded to avoid ambiguity.
 
## dataset
  dataset is freely available on
  https://www.kaggle.com/snap/amazon-fine-food-reviews

## preprocessing
  
First dataset was loaded as dataframe in jupiter notebook.
Then duplicate row with userId,productId, time,text as candidate keys were deleted.
All columns except text and star rating were deleted.
Delete rows having rating=3.
In rating column replace rating<3 by 0 and rating >3 by 1.
devide dataset into part training and testset.

## document_to_vector_conversion
 
"glove model" is a standered word to vec model provided by stanford.text reviews were converted to vctor using this model.

## Model_training
 
 different -different model applied on dataset and each gave different accuracy. logistic regression resulted highest accuracy with 92.5%.
 after applying stacking algorithm on three model adaboost, random forest and adagrad classifier it results an accuracy of 93.5%.
