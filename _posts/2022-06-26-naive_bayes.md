# Naive Bayes

##### model prep - do this for both classes
tokenize the text<br>
get a count of the total tokens<br>
add one to the token totals<br>
sum this total<br>
divide each of the token counts by the sum to get the probability<br>
take the natural log<br>

##### predictions
apply the same tokenization rules and split out the tokens<br>
sum up all the probabilities per token<br>
whichever is higher is the predicted class<br>
