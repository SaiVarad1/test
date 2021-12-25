# 5.6  Numpy Array Basic Operations

## Mathematical Operations
`+, - ,* ,/ ,**`
## Logic Operations
`& | ~` And, Or, Not
* returns boolean array
    * can be used to generate array
        * Eg: test_scores=np.array([[83,71,57,63],[54,68,81,45]])  
passing_score=test_scores>60  
test_scores[passing_score]
* np.logical_and()
* np.logical_or()
* np.logical_xor()
* np.logical_not()
* Generate Boolean arrays
    * Eg:
## Comparison Operations
* `> >= < <= == !=`   
* Eg: `np_weekly_hrs[np_weekly_hrs>40]`  
returns `array([41,55,47])