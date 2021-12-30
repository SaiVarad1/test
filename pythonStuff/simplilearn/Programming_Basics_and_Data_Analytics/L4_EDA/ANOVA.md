# 4.2 Analysis of Variance (ANOVA)

To find correlation between different groups of a categorical variable

## F-test Score
Variation between sample group mean divided by variation within sample group
* small F - poor correlation between variable,categories and target variable
* large F - strong correlation
    * similar averages -> low F score
    * different averages -> higher F score
    

## P- value 
Confidence degree - whether result is statistically significant

## Python implementation
Anova between Honda and Subaru:  
df_anova=df[["make", "price"]]  
grouped_anova=df_anova.groupb([["make"]])

`anova_results_1=stats.f_oneway(grouped_anova.get_group("honda")["price"], grouped_anova.get_group("subaru")["price"])`

### **Strong correlation if large F test value & small P value (< 0.5)