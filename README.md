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
