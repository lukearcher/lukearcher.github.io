# Naive Bayes

* grab some data
* put aside some for testing
* split into two worksheets... one per class
* preprocess and tokenize the text
* create a tokens sheet:
  * copy the token text for as many times as the maximum number of tokens
  * space position... start with 0 for the first token and then the formula:
    * =IFERROR(FIND(" ",A152, B2+1),LEN(A152)+1)
  * token column:
    * =IFERROR(MID(A2,B2+1,B152-B2-1),".")
  * length column... calculate the length
* create two pivot table sheets... probability
  * filter on the length... remove small words e.g. 3 characters or less
  * count per token
  * add one to the count
  * sum the total of the add one column
  * get the probability of the add one i.e. count / total
  * get the natural log of the probability
* preprocess the testing data... get the tokens
* for testing and prediction:
  * create a test predictions sheet
  * copy out the tokens beside each text
  * at the bottom of the sheet... and for each token:
    * =IF(LEN(D2)<=3,0,IF(ISNA(VLOOKUP(D2,pos_tokens_probability!$A$5:$E$1260,5,FALSE)),LN(1/pos_tokens_probability!$C$1260),VLOOKUP(D2,pos_tokens_probability!$A$5:$E$1260,5,FALSE)))
    * then sum them
  * repeat this also for the negative probabilities... below all the positive ones
  * create a prediction... whichever sum is higher
