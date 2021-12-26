# 2.10-11 Naive Bayes

* Simple but powerful algo for predictive modeling
* Comprises of two types of probabilities:
    * The probability of each class
    * The conditional probability of each class based on the value of x
* Can be used to make predictions for new data
* Can easily estimate prob as bell curve 
* Is naive because it assumes every input variable is **independent**

* Eg: Email classification between spam and ham email

## Bayes Theorem:
### Prior Probability: 
* Prob based on previous experience  
Eg: green and red dots classification-
    * Prior Prob of Green Dots= # of green dots/ # total dots
    * Prior Prob of Red Dots= # of red dots/ # total dots
### Prior Probabilities of Class Membership
* Number of each class of dots in the vicinity of x

### Calculation
**Likelihood of X given Green** is directly proportional to

 `(Number of GREEN in the vicinity of X)/ Total Number of Greens`

**Likelihood of X given RED** is directly proportional to

 `(Number of REDS in the vicinity of X)/ Total Number of REDS`
## Final Classification
### CALCULATION: Posterior Probability
`Prior Prob * Likelihood of X` 
 
