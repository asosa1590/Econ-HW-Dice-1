# Econ-HW-Dice-1
> set.seed (42)
> throws <- 20
> dice <- replicate (2,
+     sample(1:6, throws, replace= TRUE)
+ )
> table(rowSum(dice))
Error in rowSum(dice) : could not find function "rowSum"
> table(rowSums(dice))

 3  4  5  6  7  8  9 10 11 
 3  1  3  6  2  1  1  2  1 
 view(dice)
 
