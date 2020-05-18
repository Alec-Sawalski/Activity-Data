# Activity-Data

#### We used activity data variables "daily_activity" and "LELY_daily_rumination" as our outcome variables. We used different predictor variables from our hp9 dataset. Linear regression was used to determine significant vs. non-significant predictors of both. 

## Daily Activity Significant Predictors

#### Daily_Activity ~ BS.NEFA.0.7

    Call:
    glm(formula = log_daily_activity ~ BS.NEFA.0.7, data = Merged_new_dt_final2)

    Deviance Residuals: 
      Min        1Q    Median        3Q       Max  
    -0.74276  -0.17024  -0.04832   0.13649   1.13601  

    Coefficients:
               Estimate Std. Error t value Pr(>|t|)    
    (Intercept)   3.83380    0.03561 107.672   <2e-16 ***
    BS.NEFA.0.71 -0.17457    0.06941  -2.515   0.0136 *  
    ---
    Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

    (Dispersion parameter for gaussian family taken to be 0.08874708)

    Null deviance: 8.8148  on 94  degrees of freedom
    Residual deviance: 8.2535  on 93  degrees of freedom
    AIC: 43.49

    Number of Fisher Scoring iterations: 2

<img src=https://user-images.githubusercontent.com/61294969/82221643-e2e7db80-98e5-11ea-99b0-ff532759d117.png>

#### Daily_Activity ~ Milk.Yield

        Call:
        glm(formula = log_daily_activity ~ Milk.Yield, data = Merged_new_dt_final2)

        Deviance Residuals: 
            Min        1Q    Median        3Q       Max  
        -0.52136  -0.19065  -0.05304   0.15209   1.10686  

        Coefficients:
                  Estimate Std. Error t value Pr(>|t|)    
        (Intercept) 3.495616   0.125761  27.796   <2e-16 ***
        Milk.Yield  0.008181   0.003690   2.217   0.0294 *  
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 0.08523838)

            Null deviance: 7.4086  on 83  degrees of freedom
        Residual deviance: 6.9895  on 82  degrees of freedom
        (11 observations deleted due to missingness)
        AIC: 35.524

        Number of Fisher Scoring iterations: 2
 
 <img src=https://user-images.githubusercontent.com/61294969/82222466-f182c280-98e6-11ea-9186-8d0b605173a1.png>
 
#### Daily_Activity ~ MS.Milk.Yield

        Call:
        glm(formula = log_daily_activity ~ MS.Milk.Yield, data = Merged_new_dt_final2)

        Deviance Residuals: 
             Min        1Q    Median        3Q       Max  
        -0.67527  -0.16893  -0.03955   0.14537   1.19359  

        Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
        (Intercept)   3.618898   0.080772  44.804   <2e-16 ***
        MS.Milk.Yield 0.010559   0.004667   2.262    0.026 *  
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 0.08983916)

            Null deviance: 8.8148  on 94  degrees of freedom
        Residual deviance: 8.3550  on 93  degrees of freedom
        AIC: 44.652

        Number of Fisher Scoring iterations: 2

<img src=https://user-images.githubusercontent.com/61294969/82225341-b2567080-98ea-11ea-9b63-06c7104e9d57.png>

#### Daily_Activity ~ MS.Lactose

        Call:
        glm(formula = log_daily_activity ~ MS.Lactose, data = Merged_new_dt_final2)

        Deviance Residuals: 
            Min        1Q    Median        3Q       Max  
        -0.57652  -0.19658  -0.03712   0.15672   1.14854  

        Coefficients:
                    Estimate Std. Error t value Pr(>|t|)    
        (Intercept)   2.6520     0.5168   5.132 1.56e-06 ***
        MS.Lactose    0.2353     0.1068   2.202   0.0301 *  
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 0.09008632)

            Null deviance: 8.8148  on 94  degrees of freedom
        Residual deviance: 8.3780  on 93  degrees of freedom
        AIC: 44.913

        Number of Fisher Scoring iterations: 2

<img src=https://user-images.githubusercontent.com/61294969/82225471-ddd95b00-98ea-11ea-8aec-799be9337fd0.png>

## LELY Daily Rumination Significant Predictors

#### LELY Daily Rumination ~ Hapto.0.35

        Call:
        glm(formula = LELY_DAILY_RUMINATION ~ Hapto0.35, data = Merged_new_dt_final2)

        Deviance Residuals: 
             Min        1Q    Median        3Q       Max  
        -180.258   -38.258     5.742    42.751   110.759  

        Coefficients:
                    Estimate Std. Error t value Pr(>|t|)    
        (Intercept)  448.258      7.158  62.626   <2e-16 ***
        Hapto0.351   -30.016     12.955  -2.317   0.0227 *  
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 3381.354)

            Null deviance: 332618  on 94  degrees of freedom
        Residual deviance: 314466  on 93  degrees of freedom
        AIC: 1045.5

        Number of Fisher Scoring iterations: 2
        
<img src=https://user-images.githubusercontent.com/61294969/82225657-18db8e80-98eb-11ea-87a6-f7b121198f7f.png>

#### LELY Daily Rumination ~ CE.Waste.Consistency (Thick)

        Call:
        glm(formula = LELY_DAILY_RUMINATION ~ CE.Waste.Consistency, data = Merged_new_dt_final2)

        Deviance Residuals: 
            Min       1Q   Median       3Q      Max  
        -188.64   -31.64     6.00    43.36   113.36  

        Coefficients:
                                 Estimate Std. Error t value Pr(>|t|)    
        (Intercept)                 499.00      40.77  12.240   <2e-16 ***
        CE.Waste.Consistencynorm    -55.36      41.28  -1.341   0.1831    
        CE.Waste.Consistencythick   -97.08      43.79  -2.217   0.0291 *  
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 3324.211)

            Null deviance: 332618  on 94  degrees of freedom
        Residual deviance: 305827  on 92  degrees of freedom
        AIC: 1044.9

        Number of Fisher Scoring iterations: 2

#### LELY Daily Rumination ~ CE.Stom.Layering

        Call:
        glm(formula = LELY_DAILY_RUMINATION ~ CE.Stom.Layering, data = Merged_new_dt_final2)

        Deviance Residuals: 
             Min        1Q    Median        3Q       Max  
        -185.725   -33.725     4.775    45.025   116.275  

        Coefficients:
                         Estimate Std. Error t value Pr(>|t|)    
        (Intercept)         371.67      33.83  10.987   <2e-16 ***
        CE.Stom.Layering1    69.06      34.38   2.009   0.0475 *  
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 3432.943)

            Null deviance: 329681  on 93  degrees of freedom
        Residual deviance: 315831  on 92  degrees of freedom
          (1 observation deleted due to missingness)
        AIC: 1036

        Number of Fisher Scoring iterations: 2

#### LELY Daily Rumination ~ MS.Urea

        Call:
        glm(formula = LELY_DAILY_RUMINATION ~ MS.Urea, data = Merged_new_dt_final2)

        Deviance Residuals: 
            Min        1Q    Median        3Q       Max  
        -190.070   -27.127     7.041    37.618   101.719  

        Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
        (Intercept) 390.5559    17.5817  22.214  < 2e-16 ***
        MS.Urea       1.8733     0.6396   2.929  0.00428 ** 
        ---
        Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

        (Dispersion parameter for gaussian family taken to be 3274.499)

            Null deviance: 332618  on 94  degrees of freedom
        Residual deviance: 304528  on 93  degrees of freedom
        AIC: 1042.5

        Number of Fisher Scoring iterations: 2

<img src=https://user-images.githubusercontent.com/61294969/82224062-08c2af80-98e9-11ea-86cb-6241fd3fa253.png>
