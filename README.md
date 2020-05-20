# Activity-Data

We used activity data variables "daily_activity" and "LELY_daily_rumination" as our outcome variables. We used different predictor variables from our hp9 dataset. Linear regression was used to determine significant vs. non-significant predictors of both. In addition, boxplots were used to visualize our factor variables and scatterplots were used to visualize our numeric variables. In total, we found four significantly associated predictors with Daily_Activity and four significantly associated predictors with LELY_daily_rumination.

## Defining Non-Significant Factor Predictors

BS.BHBA.1.2 - States whether the cow had a high or low blood BHBA level

CE.Lame - Is the cow lame

Hfr.or.Cow - Type of cow, is it a heifer or a cow

CE.Locomotion Score - Locomotion Score, 1 & 2 = okay, 3, 4, & 5 = lame

FPR.1.4 - States wheter the cow had high or low Fat/Protein ratio

CE.Stom.Tension - Measurement of abdominal tension aka stomach aches

CE.Stom.Fluid.Movement - Movement of fluids in the stomach

CE.Stom.Ping - Ping of the stomach

CE.Waste.Digestion - How well food has been digested by the cow

CE.Stom.Noise.Frequency - Frequency of Rumen Rumbles

CE.Stom.Fullness - Measure of how full the stomach is

Cow.Breed - Breed of the cow; CE.Skin.Dehydration - Elasticity of the skin of the cow to measure the dehydration: Received error message and could not be complete in R

## Defining Non-Significant Numeric Predictors

BS.DIM - number of days after calving that the blood sample took place

MS.DIM - How many days after calving was the milk sampled

MS.Acetone.Log - Acetone in milk

MS.S.Cell.Count.Log - amount of somatic cells in the milk (1000 cells/mL)

MS.pH - pH measurement of the milk

MS.SFA - Amount of short fatty acids in the milk (Micro mole/L)

MS.PFA - Amount of polyunsaturated fatty acids in the milk (Micro Mole/L)

MS.MFA - Amount of monounsaturated fatty acids in the milk (Micro mole/L)

MS.NSFA - Amount of non-saturated fatty acids in the milk (Micro mole/L)

MS.Palmeic - Amount of palmeic fatty acid in the milk (Micro mole/L)

MS.Stearine - Amount of stearine fatty acid in the milk (Micro mole/L)

MS.Oleic - Amount of oleic acid in the milk (Micro mole/L)

CE.Fat.Level - Fat level on the back of the cow (mm)

CE.Temp - Inner body temperature of the cow (celsius)

## Daily Activity Significant Predictors

#### Daily_Activity ~ BS.NEFA.0.7 - NEFA levels above or below 0.7 (above 0.7=high)

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

<img src = https://user-images.githubusercontent.com/61294969/82485760-87fae380-9aa1-11ea-8e25-c654287089d8.png>

#### Daily_Activity ~ Milk.Yield - Milk Yield each day (kg)

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
 
#### Daily_Activity ~ MS.Milk.Yield - Amount of milk from a certain milk sample (kg)

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

#### Daily_Activity ~ MS.Lactose - % lactose in the milk (%)

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

#### LELY Daily Rumination ~ Hapto.0.35 - Hapto levels above or below 0.35 (0=Below 0.35, 1=Above 0.35)

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

#### LELY Daily Rumination ~ CE.Waste.Consistency - Consistency of Waste (Thick, Normal, Thin)

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

<img src=https://user-images.githubusercontent.com/61294969/82225832-50e2d180-98eb-11ea-8c78-29e3410be2e0.png>

#### LELY Daily Rumination ~ CE.Stom.Layering - Layering of the Rumen (1=Normal layering)

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

<img src=https://user-images.githubusercontent.com/61294969/82226285-ef6f3280-98eb-11ea-887b-559d119a2bd8.png>

#### LELY Daily Rumination ~ MS.Urea - % Urea Measurement

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

#### LELY Daily Rumination ~ BS.Month - Month Blood Sample was taken

       Call:
       glm(formula = LELY_DAILY_RUMINATION ~ BS.Month, data = Merged_new_dt_final2)

    Deviance Residuals: 
        Min       1Q   Median       3Q      Max  
    -163.67   -32.30     3.00    39.67   103.92  

    Coefficients:
                    Estimate Std. Error t value Pr(>|t|)    
    (Intercept)      462.769     16.264  28.453   <2e-16 ***
    BS.Month07-2018  -14.603     21.344  -0.684   0.4957    
    BS.Month08-2018  -44.103     23.475  -1.879   0.0636 .  
    BS.Month09-2018  -62.325     25.429  -2.451   0.0162 *  
    BS.Month10-2018  -29.769     24.024  -1.239   0.2186    
    BS.Month11-2018  -22.619     20.892  -1.083   0.2819    
    BS.Month12-2018   -9.686     23.475  -0.413   0.6809    
    ---
    Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

    (Dispersion parameter for gaussian family taken to be 3438.854)

     Null deviance: 332618  on 94  degrees of freedom
    Residual deviance: 302619  on 88  degrees of freedom
    AIC: 1051.9

    Number of Fisher Scoring iterations: 2

<img src = https://user-images.githubusercontent.com/61294969/82472223-77d90900-9a8d-11ea-8da5-d43e71378acd.png>

## Multiple Regression final output - Daily Activity

    Call:
    glm(formula = log_daily_activity ~ BS.NEFA.0.7 + MS.Lactose, 
    data = Merged_new_dt_final2)

    Deviance Residuals: 
         Min        1Q    Median        3Q       Max  
    -0.49940  -0.18103  -0.05424   0.16491   1.10325  

    Coefficients:
                 Estimate Std. Error t value Pr(>|t|)    
    (Intercept)   2.70818    0.50260   5.388 5.44e-07 ***
    BS.NEFA.0.71 -0.17330    0.06795  -2.550   0.0124 *  
    MS.Lactose    0.23308    0.10382   2.245   0.0272 *  
    ---
    Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

    (Dispersion parameter for gaussian family taken to be 0.08505233)

        Null deviance: 8.8148  on 94  degrees of freedom
    Residual deviance: 7.8248  on 92  degrees of freedom
    AIC: 40.424

    Number of Fisher Scoring iterations: 2

After arriving to our final Multiple Regression model, we see that BS.NEFA.0.7 and MS.Lactose are significant predictors of daily activity level in dairy cows.

## Multiple Regression final output - LELY Daily Rumination

    Call:
    glm(formula = LELY_DAILY_RUMINATION ~ Hapto0.35 + MS.Urea, data = Merged_new_dt_final2)

    Deviance Residuals: 
         Min        1Q    Median        3Q       Max  
    -179.338   -32.103     5.664    36.026   125.974  

    Coefficients:
                Estimate Std. Error t value Pr(>|t|)    
    (Intercept) 397.4486    17.2294  23.068  < 2e-16 ***
    Hapto0.351  -32.9575    12.3851  -2.661  0.00919 ** 
    MS.Urea       1.9956     0.6214   3.212  0.00182 ** 
    ---
    Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

    (Dispersion parameter for gaussian family taken to be 3073.523)

        Null deviance: 332618  on 94  degrees of freedom
    Residual deviance: 282764  on 92  degrees of freedom
    AIC: 1037.5

    Number of Fisher Scoring iterations: 2
    
After arriving to our final Multiple Regression model, we see that Hapto0.35 and MS.Urea are significant predictors of LELY Daily Rumination levels in dairy cows.
