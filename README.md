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
 
ACS Code 2017
acs2017_ny[1:10,1:7]
   AGE female educ_nohs educ_hs educ_somecoll educ_college
1   72      1         0       0             0            0
2   72      0         0       0             0            0
3   31      0         0       0             0            1
4   28      1         0       0             0            1
5   54      0         0       0             0            0
6   45      1         0       1             0            0
7   84      1         0       0             1            0
8   71      0         0       0             0            1
9   68      1         0       0             1            0
10  37      1         1       0             0            0
   educ_advdeg
1            1
2            1
3            0
4            0
5            1
6            0
7            0
8            0
9            0
10           0
> attach(acs2017_ny)
> summary(acs2017_ny)
      AGE            female         educ_nohs    
 Min.   : 0.00   Min.   :0.0000   Min.   :0.000  
 1st Qu.:22.00   1st Qu.:0.0000   1st Qu.:0.000  
 Median :42.00   Median :1.0000   Median :0.000  
 Mean   :41.57   Mean   :0.5156   Mean   :0.271  
 3rd Qu.:60.00   3rd Qu.:1.0000   3rd Qu.:1.000  
 Max.   :95.00   Max.   :1.0000   Max.   :1.000  
                                                 
    educ_hs       educ_somecoll    educ_college   
 Min.   :0.0000   Min.   :0.000   Min.   :0.0000  
 1st Qu.:0.0000   1st Qu.:0.000   1st Qu.:0.0000  
 Median :0.0000   Median :0.000   Median :0.0000  
 Mean   :0.2804   Mean   :0.173   Mean   :0.1567  
 3rd Qu.:1.0000   3rd Qu.:0.000   3rd Qu.:0.0000  
 Max.   :1.0000   Max.   :1.000   Max.   :1.0000  
                                                  
  educ_advdeg                  SCHOOL      
 Min.   :0.000   N/A              :  5569  
 1st Qu.:0.000   No, not in school:144968  
 Median :0.000   Yes, in school   : 46048  
 Mean   :0.119   Missing          :     0  
 3rd Qu.:0.000                             
 Max.   :1.000                             
                                           
                        EDUC      
 Grade 12                 :55119  
 4 years of college       :30802  
 5+ years of college      :23385  
 1 year of college        :19947  
 Nursery school to grade 4:14240  
 2 years of college       :14065  
 (Other)                  :39027  
                                          EDUCD      
 Regular high school diploma                 :35689  
 Bachelor's degree                           :30802  
 1 or more years of college credit, no degree:19947  
 Master's degree                             :17010  
 Associate's degree, type not specified      :14065  
 Some college, but less than 1 year          : 9086  
 (Other)                                     :69986  
                                     DEGFIELD     
 N/A                                     :142398  
 Business                                :  9802  
 Education Administration and Teaching   :  6708  
 Social Sciences                         :  4836  
 Medical and Health Sciences and Services:  3919  
 Fine Arts                               :  3491  
 (Other)                                 : 25431  
                                  DEGFIELDD     
 N/A                                   :142398  
 Psychology                            :  2926  
 Business Management and Administration:  2501  
 Accounting                            :  2284  
 General Education                     :  2238  
 English Language and Literature       :  2202  
 (Other)                               : 42036  
                                 DEGFIELD2     
 N/A                                  :190425  
 Business                             :   972  
 Social Sciences                      :   853  
 Education Administration and Teaching:   611  
 Fine Arts                            :   465  
 Communications                       :   352  
 (Other)                              :  2907  
                                                           DEGFIELD2D    
 N/A                                                            :190425  
 Psychology                                                     :   284  
 Economics                                                      :   260  
 Political Science and Government                               :   243  
 Business Management and Administration                         :   217  
 French, German, Latin and Other Common Foreign Language Studies:   205  
 (Other)                                                        :  4951  
      PUMA            GQ           OWNERSHP    
 Min.   : 100   Min.   :1.000   Min.   :0.000  
 1st Qu.:1500   1st Qu.:1.000   1st Qu.:1.000  
 Median :3201   Median :1.000   Median :1.000  
 Mean   :2713   Mean   :1.148   Mean   :1.266  
 3rd Qu.:3902   3rd Qu.:1.000   3rd Qu.:2.000  
 Max.   :4114   Max.   :5.000   Max.   :2.000  
                                               
   OWNERSHPD        MORTGAGE        OWNCOST     
 Min.   : 0.00   Min.   :0.000   Min.   :    0  
 1st Qu.:12.00   1st Qu.:0.000   1st Qu.: 1208  
 Median :13.00   Median :1.000   Median : 2891  
 Mean   :14.95   Mean   :1.453   Mean   :38582  
 3rd Qu.:22.00   3rd Qu.:3.000   3rd Qu.:99999  
 Max.   :22.00   Max.   :4.000   Max.   :99999  
                                                
      RENT         COSTELEC       COSTGAS    
 Min.   :   0   Min.   :   0   Min.   :   0  
 1st Qu.:   0   1st Qu.: 960   1st Qu.: 840  
 Median :   0   Median :1560   Median :2400  
 Mean   : 393   Mean   :2311   Mean   :5032  
 3rd Qu.: 630   3rd Qu.:2520   3rd Qu.:9993  
 Max.   :3800   Max.   :9997   Max.   :9997  
                                             
    COSTWATR       COSTFUEL       HHINCOME      
 Min.   :   0   Min.   :   0   Min.   : -11800  
 1st Qu.: 320   1st Qu.:9993   1st Qu.:  41600  
 Median :1400   Median :9993   Median :  81700  
 Mean   :4836   Mean   :7935   Mean   : 114902  
 3rd Qu.:9993   3rd Qu.:9993   3rd Qu.: 140900  
 Max.   :9997   Max.   :9997   Max.   :2030000  
                               NA's   :10630    
    FOODSTMP        LINGISOL         ROOMS       
 Min.   :1.000   Min.   :0.000   Min.   : 0.000  
 1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 4.000  
 Median :1.000   Median :1.000   Median : 6.000  
 Mean   :1.147   Mean   :1.002   Mean   : 5.887  
 3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.: 8.000  
 Max.   :2.000   Max.   :2.000   Max.   :16.000  
                                                 
    BUILTYR2         UNITSSTR        FUELHEAT    
 Min.   : 0.000   Min.   : 0.00   Min.   :0.000  
 1st Qu.: 1.000   1st Qu.: 3.00   1st Qu.:2.000  
 Median : 3.000   Median : 3.00   Median :2.000  
 Mean   : 3.711   Mean   : 4.39   Mean   :2.959  
 3rd Qu.: 5.000   3rd Qu.: 6.00   3rd Qu.:4.000  
 Max.   :22.000   Max.   :10.00   Max.   :9.000  
                                                 
      SSMC            FAMSIZE           NCHILD      
 Min.   :0.00000   Min.   : 1.000   Min.   :0.0000  
 1st Qu.:0.00000   1st Qu.: 2.000   1st Qu.:0.0000  
 Median :0.00000   Median : 3.000   Median :0.0000  
 Mean   :0.01102   Mean   : 3.087   Mean   :0.5009  
 3rd Qu.:0.00000   3rd Qu.: 4.000   3rd Qu.:1.0000  
 Max.   :2.00000   Max.   :19.000   Max.   :9.0000  
                                                    
     NCHLT5            RELATE          RELATED      
 Min.   :0.00000   Min.   : 1.000   Min.   : 101.0  
 1st Qu.:0.00000   1st Qu.: 1.000   1st Qu.: 101.0  
 Median :0.00000   Median : 2.000   Median : 201.0  
 Mean   :0.08441   Mean   : 3.307   Mean   : 335.6  
 3rd Qu.:0.00000   3rd Qu.: 3.000   3rd Qu.: 301.0  
 Max.   :5.00000   Max.   :13.000   Max.   :1301.0  
                                                    
     MARST            RACE          RACED    
 Min.   :1.000   Min.   :1.00   Min.   :100  
 1st Qu.:1.000   1st Qu.:1.00   1st Qu.:100  
 Median :5.000   Median :1.00   Median :100  
 Mean   :3.742   Mean   :2.03   Mean   :205  
 3rd Qu.:6.000   3rd Qu.:2.00   3rd Qu.:200  
 Max.   :6.000   Max.   :9.00   Max.   :990  
                                             
     HISPAN          HISPAND                  BPL        
 Min.   :0.0000   Min.   :  0.00   New York     :128517  
 1st Qu.:0.0000   1st Qu.:  0.00   West Indies  :  8481  
 Median :0.0000   Median :  0.00   China        :  4964  
 Mean   :0.4153   Mean   : 44.75   SOUTH AMERICA:  4957  
 3rd Qu.:0.0000   3rd Qu.:  0.00   India        :  3476  
 Max.   :4.0000   Max.   :498.00   Pennsylvania :  3303  
                                   (Other)      : 42887  
                 BPLD       
 New York          :128517  
 China             :  4116  
 Dominican Republic:  3517  
 Pennsylvania      :  3303  
 New Jersey        :  3127  
 Puerto Rico       :  2272  
 (Other)           : 51733  
                     ANCESTR1    
 Not Reported            :32021  
 Italian                 :20577  
 Irish, various subheads,:16388  
 German                  :12781  
 African-American        : 9559  
 United States           : 8209  
 (Other)                 :97050  
                                   ANCESTR1D    
 Not Reported                           :32021  
 Italian (1990-2000, ACS, PRCS)         :20577  
 Irish                                  :15651  
 German (1990-2000, ACS/PRCS)           :12605  
 African-American (1990-2000, ACS, PRCS): 9559  
 United States                          : 8209  
 (Other)                                :97963  
         ANCESTR2     
 Not Reported:141487  
 German      :  9476  
 Irish       :  9238  
 English     :  4895  
 Italian     :  4531  
 Polish      :  3113  
 (Other)     : 23845  
                          ANCESTR2D         CITIZEN      
 Not Reported                  :141487   Min.   :0.0000  
 German (1990-2000, ACS, PRCS) :  9441   1st Qu.:0.0000  
 Irish                         :  8809   Median :0.0000  
 English                       :  4895   Mean   :0.4793  
 Italian (1990-2000, ACS, PRCS):  4531   3rd Qu.:0.0000  
 Polish                        :  3113   Max.   :3.0000  
 (Other)                       : 24309                   
    YRSUSA1          HCOVANY         HCOVPRIV    
 Min.   : 0.000   Min.   :1.000   Min.   :1.000  
 1st Qu.: 0.000   1st Qu.:2.000   1st Qu.:1.000  
 Median : 0.000   Median :2.000   Median :2.000  
 Mean   : 5.377   Mean   :1.951   Mean   :1.691  
 3rd Qu.: 0.000   3rd Qu.:2.000   3rd Qu.:2.000  
 Max.   :92.000   Max.   :2.000   Max.   :2.000  
                                                 
     SEX            EMPSTAT         EMPSTATD    
 Male  : 95222   Min.   :0.000   Min.   : 0.00  
 Female:101363   1st Qu.:1.000   1st Qu.:10.00  
                 Median :1.000   Median :10.00  
                 Mean   :1.514   Mean   :15.16  
                 3rd Qu.:3.000   3rd Qu.:30.00  
                 Max.   :3.000   Max.   :30.00  
                                                
    LABFORCE          OCC              IND       
 Min.   :0.000   0      : 79987   0      :79987  
 1st Qu.:1.000   2310   :  3494   7860   : 9025  
 Median :2.000   5700   :  3235   8680   : 6354  
 Mean   :1.331   430    :  3025   770    : 6279  
 3rd Qu.:2.000   4720   :  2666   8190   : 5873  
 Max.   :2.000   4760   :  2563   7870   : 4041  
                 (Other):101615   (Other):85026  
    CLASSWKR       CLASSWKRD        WKSWORK2    
 Min.   :0.000   Min.   : 0.00   Min.   :0.000  
 1st Qu.:0.000   1st Qu.: 0.00   1st Qu.:0.000  
 Median :2.000   Median :22.00   Median :1.000  
 Mean   :1.116   Mean   :13.03   Mean   :2.701  
 3rd Qu.:2.000   3rd Qu.:22.00   3rd Qu.:6.000  
 Max.   :2.000   Max.   :29.00   Max.   :6.000  
                                                
    UHRSWORK         INCTOT           FTOTINC       
 Min.   : 0.00   Min.   :  -7300   Min.   : -11800  
 1st Qu.: 0.00   1st Qu.:   8000   1st Qu.:  35550  
 Median :12.00   Median :  25000   Median :  74000  
 Mean   :19.77   Mean   :  45245   Mean   : 107110  
 3rd Qu.:40.00   3rd Qu.:  56500   3rd Qu.: 132438  
 Max.   :99.00   Max.   :1563000   Max.   :2030000  
                 NA's   :31129     NA's   :10817    
    INCWAGE          POVERTY         MIGRATE1    
 Min.   :     0   Min.   :  0.0   Min.   :0.000  
 1st Qu.:     0   1st Qu.:159.0   1st Qu.:1.000  
 Median : 10000   Median :351.0   Median :1.000  
 Mean   : 33796   Mean   :318.7   Mean   :1.122  
 3rd Qu.: 47000   3rd Qu.:501.0   3rd Qu.:1.000  
 Max.   :638000   Max.   :501.0   Max.   :4.000  
 NA's   :33427                                   
   MIGRATE1D        MIGPLAC1         MIGCOUNTY1     
 Min.   : 0.00   Min.   :  0.000   Min.   :  0.000  
 1st Qu.:10.00   1st Qu.:  0.000   1st Qu.:  0.000  
 Median :10.00   Median :  0.000   Median :  0.000  
 Mean   :11.51   Mean   :  6.184   Mean   :  4.117  
 3rd Qu.:10.00   3rd Qu.:  0.000   3rd Qu.:  0.000  
 Max.   :40.00   Max.   :900.000   Max.   :810.000  
                                                    
    MIGPUMA1        VETSTAT          VETSTATD     
 Min.   :    0   Min.   :0.0000   Min.   : 0.000  
 1st Qu.:    0   1st Qu.:1.0000   1st Qu.:11.000  
 Median :    0   Median :1.0000   Median :11.000  
 Mean   :  277   Mean   :0.8621   Mean   : 9.412  
 3rd Qu.:    0   3rd Qu.:1.0000   3rd Qu.:11.000  
 Max.   :70100   Max.   :2.0000   Max.   :20.000  
                                                  
    PWPUMA00        TRANWORK         TRANTIME     
 Min.   :    0   Min.   : 0.000   Min.   :  0.00  
 1st Qu.:    0   1st Qu.: 0.000   1st Qu.:  0.00  
 Median :    0   Median : 0.000   Median :  0.00  
 Mean   : 1255   Mean   : 9.725   Mean   : 14.75  
 3rd Qu.: 3100   3rd Qu.:10.000   3rd Qu.: 20.00  
 Max.   :59300   Max.   :70.000   Max.   :138.00  
                                                  
    DEPARTS           in_NYC          in_Bronx     
 Min.   :   0.0   Min.   :0.0000   Min.   :0.0000  
 1st Qu.:   0.0   1st Qu.:0.0000   1st Qu.:0.0000  
 Median :   0.0   Median :0.0000   Median :0.0000  
 Mean   : 373.3   Mean   :0.3615   Mean   :0.0538  
 3rd Qu.: 732.0   3rd Qu.:1.0000   3rd Qu.:0.0000  
 Max.   :2345.0   Max.   :1.0000   Max.   :1.0000  
                                                   
  in_Manhattan       in_StatenI       in_Brooklyn   
 Min.   :0.00000   Min.   :0.00000   Min.   :0.000  
 1st Qu.:0.00000   1st Qu.:0.00000   1st Qu.:0.000  
 Median :0.00000   Median :0.00000   Median :0.000  
 Mean   :0.04981   Mean   :0.02084   Mean   :0.126  
 3rd Qu.:0.00000   3rd Qu.:0.00000   3rd Qu.:0.000  
 Max.   :1.00000   Max.   :1.00000   Max.   :1.000  
                                                    
   in_Queens      in_Westchester      in_Nassau      
 Min.   :0.0000   Min.   :0.00000   Min.   :0.00000  
 1st Qu.:0.0000   1st Qu.:0.00000   1st Qu.:0.00000  
 Median :0.0000   Median :0.00000   Median :0.00000  
 Mean   :0.1111   Mean   :0.04413   Mean   :0.07032  
 3rd Qu.:0.0000   3rd Qu.:0.00000   3rd Qu.:0.00000  
 Max.   :1.0000   Max.   :1.00000   Max.   :1.00000  
                                                     
    Hispanic         Hisp_Mex          Hisp_PR      
 Min.   :0.0000   Min.   :0.00000   Min.   :0.0000  
 1st Qu.:0.0000   1st Qu.:0.00000   1st Qu.:0.0000  
 Median :0.0000   Median :0.00000   Median :0.0000  
 Mean   :0.1387   Mean   :0.01626   Mean   :0.0436  
 3rd Qu.:0.0000   3rd Qu.:0.00000   3rd Qu.:0.0000  
 Max.   :1.0000   Max.   :1.00000   Max.   :1.0000  
                                                    
   Hisp_Cuban         Hisp_DomR           white       
 Min.   :0.000000   Min.   :0.00000   Min.   :0.0000  
 1st Qu.:0.000000   1st Qu.:0.00000   1st Qu.:0.0000  
 Median :0.000000   Median :0.00000   Median :1.0000  
 Mean   :0.003403   Mean   :0.02827   Mean   :0.6997  
 3rd Qu.:0.000000   3rd Qu.:0.00000   3rd Qu.:1.0000  
 Max.   :1.000000   Max.   :1.00000   Max.   :1.0000  
                                                      
      AfAm          Amindian            Asian        
 Min.   :0.000   Min.   :0.000000   Min.   :0.00000  
 1st Qu.:0.000   1st Qu.:0.000000   1st Qu.:0.00000  
 Median :0.000   Median :0.000000   Median :0.00000  
 Mean   :0.125   Mean   :0.003779   Mean   :0.08656  
 3rd Qu.:0.000   3rd Qu.:0.000000   3rd Qu.:0.00000  
 Max.   :1.000   Max.   :1.000000   Max.   :1.00000  
                                                     
    race_oth        unmarried       veteran       
 Min.   :0.0000   Min.   :0.00   Min.   :0.00000  
 1st Qu.:0.0000   1st Qu.:0.00   1st Qu.:0.00000  
 Median :0.0000   Median :0.00   Median :0.00000  
 Mean   :0.1324   Mean   :0.45   Mean   :0.04443  
 3rd Qu.:0.0000   3rd Qu.:1.00   3rd Qu.:0.00000  
 Max.   :1.0000   Max.   :1.00   Max.   :1.00000  
                                                  
 has_AnyHealthIns has_PvtHealthIns  Commute_car    
 Min.   :0.0000   Min.   :0.0000   Min.   :0.0000  
 1st Qu.:1.0000   1st Qu.:0.0000   1st Qu.:0.0000  
 Median :1.0000   Median :1.0000   Median :0.0000  
 Mean   :0.9513   Mean   :0.6906   Mean   :0.2997  
 3rd Qu.:1.0000   3rd Qu.:1.0000   3rd Qu.:1.0000  
 Max.   :1.0000   Max.   :1.0000   Max.   :1.0000  
                                                   
  Commute_bus      Commute_subway     Commute_rail    
 Min.   :0.00000   Min.   :0.00000   Min.   :0.00000  
 1st Qu.:0.00000   1st Qu.:0.00000   1st Qu.:0.00000  
 Median :0.00000   Median :0.00000   Median :0.00000  
 Mean   :0.02162   Mean   :0.07468   Mean   :0.01332  
 3rd Qu.:0.00000   3rd Qu.:0.00000   3rd Qu.:0.00000  
 Max.   :1.00000   Max.   :1.00000   Max.   :1.00000  
                                                      
 Commute_other     below_povertyline below_150poverty
 Min.   :0.00000   Min.   :0.000     Min.   :0.0000  
 1st Qu.:0.00000   1st Qu.:0.000     1st Qu.:0.0000  
 Median :0.00000   Median :0.000     Median :0.0000  
 Mean   :0.05506   Mean   :0.122     Mean   :0.1965  
 3rd Qu.:0.00000   3rd Qu.:0.000     3rd Qu.:0.0000  
 Max.   :1.00000   Max.   :1.000     Max.   :1.0000  
                                                     
 below_200poverty   foodstamps    
 Min.   :0.0000   Min.   :0.0000  
 1st Qu.:0.0000   1st Qu.:0.0000  
 Median :0.0000   Median :0.0000  
 Mean   :0.2676   Mean   :0.1465  
 3rd Qu.:1.0000   3rd Qu.:0.0000  
 Max.   :1.0000   Max.   :1.0000  
                                  
> print(NN_obs <- length(AGE))
[1] 196585
> summary(AGE[female == 1])
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   0.00   23.00   44.00   42.72   61.00   95.00 
> mean(AGE[female == 1]
+ )
[1] 42.71629
> sd(AGE[female == 1])
[1] 23.72012
> mean(AGE[!female])
[1] 40.35398
> sd(AGE[!female])
[1] 23.1098
> 


4. The average for women in the sample was 42.72 and the average age for men in the sample was 40.35. I found interesting among Hispanics, Hisp_PR has the highest education attainment of 0.0436. This is particularly interesting to me because I was curious why this group of people had a larger education attainment relative to other Hispanics within the region. 
=======
4. The average for women in the sample was 42.72 and the average age for men in the sample was 40.35.



`````
5
For Question 5 instead of using the S&P 500 we used the SPY index which is an Exchange Traded Fund that is based off the S&P 500 and fluctuates according to price changes that occur on the S&P . We looked at the opening and closing price for SPY from 1993 until 2006. Based on the data we believe that an investment for SPY in 1993 of roughly 50 dollars in Jan 1993 would have yielded an investor a 166 percent increase if they had sold in October 2006 for 133 dollars. Relating to the Hot Hand Fallacy, the idea that a person can determine their luck by previous successsful outcomes is not true. Looking at the month to month rate of returns, the price changes for this stock and the S&P fluctuated immensely. The Max value of this stock occured in April 2000 at a price of 150 after the stock started to decrease reaching around 85 dollars. It's important to note that throughout this time period the value of this investment would be in positive. If we were to graph the price values for SPY we would see an upward sloping curve throughout this time period  when looking at price. However if we compared the price data to the results of the   dice expierement where we are analyzing outcomes of rolls,  we would see a relatively flat line where most numbers from 1-6 would appear evenly.
Please see below the data 
"citation: citation("quantmod")
To cite package ‘quantmod’ in publications use:
  Jeffrey A. Ryan and Joshua M. Ulrich (2020).
  quantmod: Quantitative Financial Modelling
  Framework. http://www.quantmod.com
  https://github.com/joshuaulrich/quantmod."
 SPY.Open  SPY.High   SPY.Low SPY.Close  SPY.Volume SPY.Adjusted
Jan 1993  43.96875  43.96875  43.75000  43.93750     1003200     26.18406
Feb 1993  43.96875  45.12500  42.81250  44.40625     5417600     26.46340
Mar 1993  44.56250  45.84375  44.21875  45.18750     3019200     27.05615
Apr 1993  45.25000  45.25000  43.28125  44.03125     2697200     26.36384
May 1993  44.09375  45.65625  43.84375  45.21875     1808000     27.07487
Jun 1993  45.37500  45.81250  44.21875  45.06250     3438000     27.17253
Jul 1993  45.12500  45.21875  44.15625  44.84375     6117600     27.04063
Aug 1993  44.90625  46.56250  44.84375  46.56250     5440100     28.07704
Sep 1993  46.40625  46.59375  44.81250  45.93750     4369900     27.87274
Oct 1993  45.87500  47.15625  45.71875  46.84375     6972900     28.42262
Nov 1993  46.78125  47.00000  45.53125  46.34375     5351100     28.11924
Dec 1993  46.59375  47.15625  46.37500  46.59375     6128000     28.46446
Jan 1994  46.59375  48.31250  46.40625  48.21875     6837100     29.45719
Feb 1994  48.15625  48.28125  46.56250  46.81250    10974400     28.59809
Mar 1994  46.81250  47.31250  43.53125  44.59375    14705500     27.39980
Apr 1994  43.34375  45.35938  43.34375  45.09375    11429000     27.70700
May 1994  45.09375  45.93750  44.17188  45.81250     8545100     28.14862
Jun 1994  45.70312  46.56250  44.00000  44.46875    10352700     27.50363
Jul 1994  44.68750  46.04688  44.37500  45.90625     5452100     28.39272
Aug 1994  45.93750  47.98438  45.65625  47.65625     7945800     29.47507
Sep 1994  47.50000  47.71875  45.73438  46.17188     6309300     28.73069
Oct 1994  46.20312  47.70312  45.00000  47.48438     5437600     29.54739
Nov 1994  47.28125  47.32812  44.60938  45.59375     4807300     28.37095
Dec 1994  45.64062  46.40625  44.68750  45.56250     8568500     28.57755
Jan 1995  45.70312  47.23438  45.68750  47.09375     2768000     29.53798
Feb 1995  47.15625  49.15625  47.00000  49.01562     5954800     30.74341
Mar 1995  48.96875  50.89062  48.21875  50.10938     4538000     31.59954
Apr 1995  50.09375  51.67188  50.06250  51.59375     4395200     32.53560
May 1995  51.54688  53.64062  51.39062  53.64062     6986200     33.82639
Jun 1995  53.40625  55.15625  52.75000  54.40625     5790900     34.51070
Jul 1995  54.46875  56.70312  54.20312  56.15625     5508200     35.62075
Aug 1995  56.23438  56.79688  55.42188  56.40625     8100100     35.77932
Sep 1995  56.39062  58.90625  56.34375  58.48438     7431600     37.29551
Oct 1995  58.48438  59.18750  57.26562  58.31250     8944800     37.18590
Nov 1995  58.28125  61.20312  58.23438  60.90625     8841700     38.83995
Dec 1995  60.98438  62.79688  60.57812  61.48438     9816800     39.45102
Jan 1996  61.40625  63.68750  59.64062  63.67188    10661800     40.85461
Feb 1996  63.60938  66.68750  63.43750  63.87500    14850400     40.98494
Mar 1996  64.64062  65.96875  62.00000  64.68750    19022700     41.69064
Apr 1996  65.00000  65.81250  62.12500  65.39062    14999300     42.14380
May 1996  65.37500  68.43750  63.07812  66.87500    17453200     43.10046
Jun 1996  66.89062  68.50000  66.15625  67.10938    16871800     43.48068
Jul 1996  67.28125  67.70312  60.37500  64.09375    28811500     41.52684
Aug 1996  64.15625  67.34375  64.06250  65.32812    15593100     42.32661
Sep 1996  64.46875  69.25000  64.37500  68.62500    17216100     44.69151
Oct 1996  68.70312  71.62500  68.43750  70.84375    14791800     46.13645
Nov 1996  70.98438  76.68750  70.26562  76.01562    24089700     49.50458
Dec 1996  75.92188  76.57812  71.87500  73.84375    34952800     48.32648
Jan 1997  74.37500  79.68750  72.75000  78.40625    43623700     51.31237
Feb 1997  78.71875  82.00000  77.12500  79.15625    30028800     51.80320
Mar 1997  78.75000  81.79688  75.25000  75.37500    37514300     49.51753
Apr 1997  75.25000  80.68750  73.31250  80.09375    57679300     52.61750
May 1997  80.21875  85.56250  79.31250  85.15625    37473400     55.94330
Jun 1997  85.34375  90.50000  84.07812  88.31250    47332500     58.24268
Jul 1997  88.50000  96.03125  88.39062  95.31250    65359700     62.85922
Aug 1997  95.50000  96.62500  89.34375  90.37500    99046800     59.60293
Sep 1997  90.68750  96.37500  90.25000  94.37500    78642200     62.46927
Oct 1997  95.25000  98.50000  84.37500  92.06250   137440500     60.93856
Nov 1997  93.18750  96.81250  90.09375  95.62500    93157400     63.29668
Dec 1997  96.21875  99.00000  92.37500  97.06250    79162300     64.50387
Jan 1998  97.31250  99.56250  90.90625  98.31250   104582300     65.33454
Feb 1998  99.90625 105.53125  99.71875 105.12500    69733700     69.86186
Mar 1998 105.25000 111.53125 103.15625 109.93750    87316900     73.26994
Apr 1998 110.31250 113.43750 107.62500 111.34375   118629400     74.20720
May 1998 111.75000 113.31250 107.57812 109.03125   116264800     72.66599
Jun 1998 108.96875 114.68750 107.50000 113.31250   141993600     75.75962
Jul 1998 114.06250 119.23438 111.31250 111.78125   155280200     74.73584
Aug 1998 111.78125 112.42188  95.00000  96.00000   268542800     64.18467
Sep 1998  96.06250 107.00000  93.62500 101.75000   269370500     68.26932
Oct 1998 100.03125 110.90625  92.21875 110.00000   249152700     73.80466
Nov 1998 110.81250 119.71875 110.18750 116.12500   136369000     77.91425
Dec 1998 116.12500 124.75000 113.75000 123.31250   156026700     83.01160
Jan 1999 123.37500 128.50000 120.37500 127.65625   141419000     85.93572
Feb 1999 128.68750 128.84375 121.32812 123.56250   164624900     83.17986
Mar 1999 123.65625 132.62500 121.78125 128.37500   148191100     86.62915
Apr 1999 129.68750 137.50000 128.12500 133.25000   156755700     89.91887
May 1999 133.43750 138.00000 128.00000 130.20312   182566900     87.86282
Jun 1999 130.12500 137.50000 128.01562 137.00000   160692200     92.72853
Jul 1999 137.00000 142.25000 132.56250 132.75000   115669100     89.85192
Aug 1999 132.75000 138.78125 127.00000 132.06250   142925900     89.38658
Sep 1999 132.93750 136.62500 125.56250 128.75000   167972700     87.38995
Oct 1999 127.93750 137.68750 123.43750 137.00000   196829400     92.98969
Nov 1999 136.50000 143.00000 134.59375 139.28125   125042200     94.53812
Dec 1999 139.31250 147.56250 139.00000 146.87500   121529300     99.93713
Jan 2000 148.25000 148.25000 135.00000 139.56250   156770800     94.96152
Feb 2000 139.75000 144.56250 132.71875 137.43750   186938300     93.51562
Mar 2000 137.62500 155.75000 135.03125 150.37500   247594900    102.57863
Apr 2000 150.12500 153.10938 133.50000 145.09375   229246200     98.97604
May 2000 146.56250 148.48438 136.50000 142.81250   161024000     97.41985
Jun 2000 143.68750 149.15625 143.00000 145.28125   127146000     99.33723
Jul 2000 145.43750 151.98438 141.51562 143.00000   106780100     97.77743
Aug 2000 143.62500 153.09375 142.62500 152.34375   102365500    104.16626
Sep 2000 153.25000 153.59375 142.12500 143.62500   113203000     98.45151
Oct 2000 144.28125 145.75000 130.15625 142.95312   178392400     97.99097
Nov 2000 142.25000 144.29688 129.75000 132.28125   156699900     90.67563
Dec 2000 133.18750 139.56250 125.53125 131.18750   165416700     90.20176
Jan 2001 132.00000 138.70000 127.56250 137.02000   181296400     94.21201
Feb 2001 137.10001 137.99000 121.80000 123.95000   178607000     85.22537
Mar 2001 124.05000 127.75000 108.04000 116.69000   318187200     80.44959
Apr 2001 116.30000 127.27000 109.30000 126.66000   251839700     87.32320
May 2001 125.07000 132.09000 123.44000 125.95000   208040000     86.83375
Jun 2001 126.20000 129.23000 120.40000 122.60000   203578200     84.76453
Jul 2001 122.80000 124.32000 116.75000 121.35000   196892900     83.90025
Aug 2001 121.97000 123.25000 112.04000 114.15000   269599600     78.92227
Sep 2001 113.85000 116.17000  93.80000 104.44000   419156100     72.47982
Oct 2001 103.90000 111.79000 102.83000 105.80000   512612000     73.42362
Nov 2001 106.60000 116.90000 105.70000 114.05000   372515000     79.14898
Dec 2001 113.65000 118.00000 112.00000 114.30000   308403900     79.59532
Jan 2002 115.11000 117.99000 108.40000 113.18000   349380000     78.81542
Feb 2002 113.09000 113.30000 107.82000 111.15000   424492600     77.40173
Mar 2002 111.72000 117.90000 111.51000 114.52000   385578100     79.97697
Apr 2002 114.23000 115.10000 106.63000 107.86000   404461000     75.32586
May 2002 107.97000 111.25000 104.90000 107.22000   452626500     74.87891
Jun 2002 107.09000 107.60000  95.19000  98.96000   534883500     69.35227
Jul 2002  99.18000  99.80000  77.68000  91.16000  1124248800     63.88598
Aug 2002  90.88000  97.15000  83.55000  91.78000   936191200     64.32047
Sep 2002  90.73000  93.33000  80.90000  81.79000  1013828600     57.57631
Oct 2002  82.43000  91.29000  77.07000  88.52000  1344248100     62.31389
Nov 2002  88.35000  94.95000  87.45000  93.98000   818243400     66.15749
Dec 2002  95.47000  96.05000  87.11000  88.23000   728285900     62.41492
Jan 2003  88.85000  93.86000  84.15000  86.06000   911319900     60.87987
Feb 2003  86.14000  86.81000  81.00000  84.90000   862248300     60.05928
Mar 2003  85.26000  89.88000  79.38000  84.74000  1156870200     60.18781
Apr 2003  85.25000  92.80000  84.91000  91.91000   996114200     65.28040
May 2003  91.92000  97.09000  90.50000  96.95000   881509900     68.86012
Jun 2003  97.53000 102.18000  96.67000  97.63000   867970200     69.59363
Jul 2003  97.25000 101.90000  96.43000  99.39000   895260500     70.84818
Aug 2003  99.19000 101.82000  96.34000 101.44000   772702000     72.30950
Sep 2003 101.64000 104.70000  99.25000  99.95000   818513400     71.52087
Oct 2003 100.24000 105.97000 100.20000 105.30000   831700900     75.34915
Nov 2003 105.75000 106.95000 103.62000 106.45000   630654200     76.17205
Dec 2003 106.85000 111.52000 105.96000 111.28000   678350400     80.00449
Jan 2004 111.74000 116.50000 110.73000 113.48000   737674000     81.58620
Feb 2004 113.70000 116.60000 112.78000 115.02000   676976900     82.69335
Mar 2004 115.43000 116.97000 108.85000 113.10000  1125003900     81.59803
Apr 2004 113.07000 115.41000 110.90000 110.96000   968620900     80.05411
May 2004 111.37000 113.26000 108.06000 112.86000   981083900     81.42487
Jun 2004 112.46000 114.94000 111.87000 114.53000   721880400     82.93137
Jul 2004 114.25000 114.40000 108.21000 110.84000   954619200     80.25943
Aug 2004 110.19000 111.63000 106.59000 111.11000   922892000     80.45492
Sep 2004 110.95000 113.74000 110.41000 111.76000   790891900     81.26246
Oct 2004 112.26000 114.68000 109.35000 113.20000  1044071300     82.30950
Nov 2004 113.56000 119.14000 113.20000 117.89000   961601700     85.97372
Dec 2004 118.16000 121.66000 117.73000 120.87000   909170200     88.56335
Jan 2005 121.56000 121.76000 116.37000 118.16000  1184211500     86.57769
Feb 2005 118.25000 121.67000 118.10000 120.63000  1025608400     88.38747
Mar 2005 120.82000 123.25000 116.25000 117.96000  1330548800     86.77064
Apr 2005 118.63000 119.26000 113.55000 115.75000  1633318500     85.14498
May 2005 116.07000 120.25000 114.80000 119.48000  1334647300     87.88872
Jun 2005 119.52000 121.94000 118.75000 119.18000  1089322900     88.02186
Jul 2005 119.45000 124.64000 118.26000 123.74000  1176306400     91.38970
Aug 2005 123.83000 124.74000 120.38000 122.58000  1306564800     90.53298
Sep 2005 122.52000 124.74000 120.44000 123.04000  1287005000     91.25951
Oct 2005 122.96000 123.34000 116.88000 120.13000  1784566400     89.10118
Nov 2005 120.58000 127.41000 120.13000 125.41000  1183732800     93.01740
Dec 2005 126.02000 128.09000 124.36000 124.51000  1073146800     92.83941
Jan 2006 125.19000 129.44000 124.39000 127.50000  1233910800     95.06889
Feb 2006 127.82000 130.03999 125.40000 128.23000  1145244400     95.61315
Mar 2006 128.60001 131.47000 127.18000 129.83000  1350777100     97.19117
Apr 2006 130.07001 131.86000 128.02000 131.47000  1300327900     98.41889
May 2006 131.47000 132.80000 124.76000 127.51000  1752747100     95.45443
Jun 2006 127.38000 129.42999 122.34000 127.28000  2163829300     95.70335
Jul 2006 127.43000 128.14000 122.39000 127.85000  1691301400     96.13197
Aug 2006 127.34000 131.03999 126.28000 130.64000  1420345400     98.22980
Sep 2006 131.14000 133.99000 129.35001 133.58000  1363687900    100.88213
Oct 2006 133.53999 139.00000 132.64999 137.78999  1443344100    104.06167
`````

We also attached the Month to Month rate of return for the SPY ETF from January 1st 1993 until October 31st 2006

> monthlyReturn(SPY)
           monthly.returns
1993-01-29   -0.0007107321
1993-02-26    0.0106685633
1993-03-31    0.0175932442
1993-04-30   -0.0255878285
1993-05-28    0.0269694819
1993-06-30   -0.0034554250
1993-07-30   -0.0048543689
1993-08-31    0.0383275261
1993-09-30   -0.0134228188
1993-10-29    0.0197278912
1993-11-30   -0.0106737825
1993-12-31    0.0053944707
1994-01-31    0.0348759222
1994-02-28   -0.0291639663
1994-03-31   -0.0473965287
1994-04-29    0.0112123336
1994-05-31    0.0159390159
1994-06-30   -0.0293315143
1994-07-29    0.0323260717
1994-08-31    0.0381211709
1994-09-30   -0.0311475410
1994-10-31    0.0284263959
1994-11-30   -0.0398157289
1994-12-30   -0.0006854010
1995-01-31    0.0336076818
1995-02-28    0.0408095554
1995-03-31    0.0223143130
1995-04-28    0.0296227003
1995-05-31    0.0396729255
1995-06-30    0.0142732304
1995-07-31    0.0321654222
1995-08-31    0.0044518642
1995-09-29    0.0368421053
1995-10-31   -0.0029388191
1995-11-30    0.0444801715
1995-12-29    0.0094920472
1996-01-31    0.0355781449
1996-02-29    0.0031901840
1996-03-29    0.0127201566
1996-04-30    0.0108695652
1996-05-31    0.0227001195
1996-06-28    0.0035046729
1996-07-31   -0.0449359721
1996-08-30    0.0192588981
1996-09-30    0.0504663956
1996-10-31    0.0323315118
1996-11-29    0.0730039700
1996-12-31   -0.0285714286
1997-01-31    0.0617858654
1997-02-28    0.0095655640
1997-03-31   -0.0477694433
1997-04-30    0.0626036484
1997-05-30    0.0632071791
1997-06-30    0.0370642202
1997-07-31    0.0792639774
1997-08-29   -0.0518032787
1997-09-30    0.0442600277
1997-10-31   -0.0245033113
1997-11-28    0.0386965377
1997-12-31    0.0150326797
1998-01-30    0.0128783001
1998-02-27    0.0692943420
1998-03-31    0.0457788347
1998-04-30    0.0127913587
1998-05-29   -0.0207690149
1998-06-30    0.0392662654
1998-07-31   -0.0135135135
1998-08-31   -0.1411797596
1998-09-30    0.0598958333
1998-10-30    0.0810810811
1998-11-30    0.0556818182
1998-12-31    0.0618945102
1999-01-29    0.0352255449
1999-02-26   -0.0320685435
1999-03-31    0.0389479009
1999-04-30    0.0379746835
1999-05-28   -0.0228658537
1999-06-30    0.0522020881
1999-07-30   -0.0310218978
1999-08-31   -0.0051789077
1999-09-30   -0.0250828206
1999-10-29    0.0640776699
1999-11-30    0.0166514599
1999-12-31    0.0545209782
2000-01-31   -0.0497872340
2000-02-29   -0.0152261532
2000-03-31    0.0941336971
2000-04-28   -0.0351205320
2000-05-31   -0.0157225932
2000-06-30    0.0172866521
2000-07-31   -0.0157023016
2000-08-31    0.0653409091
2000-09-29   -0.0572307692
2000-10-31   -0.0046779809
2000-11-30   -0.0746529675
2000-12-29   -0.0082683676
2001-01-31    0.0444592968
2001-02-28   -0.0953875830
2001-03-30   -0.0585719659
2001-04-30    0.0854400705
2001-05-31   -0.0056056133
2001-06-29   -0.0265978490
2001-07-31   -0.0101957587
2001-08-31   -0.0593324773
2001-09-28   -0.0850635114
2001-10-31    0.0130218400
2001-11-30    0.0779773135
2001-12-31    0.0021920210
2002-01-31   -0.0097988011
2002-02-28   -0.0179360134
2002-03-28    0.0303193427
2002-04-30   -0.0581557472
2002-05-31   -0.0059336176
2002-06-28   -0.0770378840
2002-07-31   -0.0788196754
2002-08-30    0.0068011735
2002-09-30   -0.1088472228
2002-10-31    0.0822838479
2002-11-29    0.0616810459
2002-12-31   -0.0611832285
2003-01-31   -0.0245948649
2003-02-28   -0.0134789220
2003-03-31   -0.0018846172
2003-04-30    0.0846118264
2003-05-30    0.0548361743
2003-06-30    0.0070139249
2003-07-31    0.0180272668
2003-08-29    0.0206258479
2003-09-30   -0.0146885348
2003-10-31    0.0535268250
2003-11-28    0.0109211203
2003-12-31    0.0453734348
2004-01-30    0.0197699858
2004-02-27    0.0135706200
2004-03-31   -0.0166927408
2004-04-30   -0.0189213001
2004-05-28    0.0171233059
2004-06-30    0.0147970759
2004-07-30   -0.0322186591
2004-08-31    0.0024359889
2004-09-30    0.0058500674
2004-10-29    0.0128847081
2004-11-30    0.0414311142
2004-12-31    0.0252778355
2005-01-31   -0.0224207738
2005-02-28    0.0209037992
2005-03-31   -0.0221337815
2005-04-29   -0.0187351561
2005-05-31    0.0322246479
2005-06-30   -0.0025109055
2005-07-29    0.0382614365
2005-08-31   -0.0093744627
2005-09-30    0.0037526431
2005-10-31   -0.0236508776
2005-11-30    0.0439524443
2005-12-30   -0.0071764769
2006-01-31    0.0240141190
2006-02-28    0.0057254588
2006-03-31    0.0124776265
2006-04-28    0.0126318954
2006-05-31   -0.0301209323
2006-06-30   -0.0018038036
2006-07-31    0.0044783077
2006-08-31    0.0218224563
2006-09-29    0.0225046159
2006-10-31    0.0315166263

