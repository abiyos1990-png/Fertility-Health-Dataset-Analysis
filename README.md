# Fertility Health Dataset Analysis

This project examines a fertility health dataset to assess the impact of female and male factors for reproductive success. In this project, various couple variables were assessed and their impact for fertility outcome was expressed using tables and charts. It is an exploratory SQL analysis of various predictors for pregnancy success.

# Team

Yosief Weldesemaeti Habtemariam

# Dataset

The dataset contains fertility-related health and lifestyle indicators for predicting pregnancy outcomes (Success / Failure) in couples. It includes female and male age, BMI, menstrual regularity, PCOS status, sperm count, sperm motility, stress levels, sleep quality, smoking habits, alcohol intake, and exercise levels. 

# Dataset Size & Structure

•	Rows: 2,000

•	Columns: 19

# Objectives of the Analysis

Infertility remains a widespread global health challenge, and it affects millions of couples. Male and female factors have equal contribution to the infertility problem. This dataset provides a synthetic but realistic representation of couples' fertility health indicators, including age, BMI, hormonal conditions (PCOS, menstrual regularity), lifestyle habits (smoking, alcohol, exercise, sleep), and male fertility metrics (sperm count and motility).  This project emphasises mainly on;

1.	Identify the physiological factors (such as chronological age and BMI of male and female couples and analyse their impact for successful conception. Besides, it evaluates which factors mainly determine to exponential decrease in pregnancy success.
 
2.	How presence of polycystic ovarian syndrome influence reproduction success during female fertility period. In addition, it evaluates whether BMI has positive or negative impact on fertility outcomes.

3.	Comparison of sperm count (millions per millilitre-quantity) vs. sperm motility(quality) in male fertilization capability. It also evaluates which variable is more reliable predictor of pregnancy success.
   
# Analysis Methodology

The Fertility Health Dataset was extracted from Kaggle and was uploaded to DBeaver interface. Then using DuckDB data engine the Dataset is analysed using several exploratory SQL analyses. After data cleaning and type casting, representative charts were visualized using Google Sheets. Finally, the results of the assessment were uploaded into GitHUb.

# Final Results

## 1.	Female Age vs. Pregnancy Success

This analysis shows a significant correlation between maternal age and conception success. By isolating female age as an independent variable, the data reveals a consistent linear decline. Especially beyond the age 36, the pregnancy success rate drops by approximately 48.61% (i.e. it drops from 26.52 % to 12.89 %).

Conclusion: This trend demonstrates the critical impact of maternal age (biological clock) on reproductive outcomes within the dataset. Furthermore, this finding serves as a baseline for evaluating other health factors, such as BMI and PCOS.

<img width="600" height="371" alt="Impact of female age on pregnancy success" src="https://github.com/user-attachments/assets/f421ae9b-ebb9-4847-9b90-46e9a9dad012" />
 

## 2.	Female Age and BMI on Pregnancy Success

The evaluation reveals a complex interaction between maternal age, BMI and pregnancy success. The most significant finding is the drastic decline in pregnancy success rate (3.8%) for the obese females once they cross the age of 35. It also shows a sharp decline of more than half (11.8 %) in older healthy females. 

Conclusion: The dataset confirms that while BMI influences baseline fertility, the biological age (mainly after 35) remains the dominant influencer for pregnancy success. The negative impact of old age is even worse if it is combined with obesity.

<img width="600" height="371" alt="Impact of Female Age and BMI on Pregnancy Success" src="https://github.com/user-attachments/assets/884aa523-ebc9-4cdb-be00-b9e0694c449b" />


## 3.	Female Age, Female average BMI and Pregnancy Success

This result shows how female age plays a significant role in fertility success irrespective of body mass. The trend shows that even when females in the sample have average BMI (23.17 – 24.81) it cannot compensate the biological impact of aging.

Conclusion: As female age increases, the pregnancy success rate exhibits a steady, linear decline. This indicates that while a healthy average BMI is an important factor in fertility, it cannot prevent the age-related infertility.

<img width="600" height="371" alt="Female age, Female average BMI vs Pregnancy Success" src="https://github.com/user-attachments/assets/a22540e1-e505-4681-8171-81c101d23887" />


## 4.	Correlation between PCOS and Pregnancy Success

This evaluation reveals that the presence of Polycystic Ovary Syndrome in females results in a nearly 60.1 % relative reduction in pregnancy success rates. In the No PCOS cohort, the bar graph shows a baseline pregnancy success rate of 21.36 %. However, this success rate drops significantly to 12.84 % in females with PCOS.

Conclusion: While successful pregnancy remains possible with the presence of Polycystic Ovary Syndrome, it is a major physiological barrier to conception. As a result, pregnancy failure rate climbs from a baseline of 78.64 % to 87.16 % in the PCOS group.

<img width="600" height="371" alt="Correlation between PCOS and Pregnancy Success " src="https://github.com/user-attachments/assets/e0474c9f-ac1e-49d9-ace9-e7e591da8603" />


## 5.	Male Age vs. Pregnancy Success

The assessment indicates that male age is relatively weak predictor of pregnancy success within this dataset. The regression analysis of 0.006 signify that only 6 % of the variance in pregnancy success rates can be attributed to the male partner’s age. While there is a slight downward trend, the slope is remarkably gradual compared to females. 

Conclusion: These findings suggest that, while paternal age may contribute to a marginal decrease in fertility, it is a minor factor compared to the female age or metabolic health markers such as PCOS and BMI.

<img width="600" height="371" alt="Male Age vs Pregnancy Success" src="https://github.com/user-attachments/assets/c369b671-e921-4c8d-b03b-7538959dafbd" />


## 6.	Sperm Count vs. Pregnancy Success

Similar to male age, the analysis of sperm count in millions per millilitre appears to have a limited impact on pregnancy success. The data shows a linear increment in success rates- moving from just below 20 % to slightly above 20%. In addition, there is low correlation coefficient (0.006 %) suggests that, once a minimum threshold of sperm concentration is met, increasing the count has little effect in pregnancy success.

Conclusion: This result broadens the finding that male side numerical metrics (sperm count) has less predictive of pregnancy success than female biological and metabolic factors within this specific dataset.

<img width="600" height="371" alt="Sperm Count vs Pregnancy Success" src="https://github.com/user-attachments/assets/cbedd09d-81c8-4ac3-b19e-bbd603253c58" />


## 7.	Sperm Motility vs. Pregnancy Success

While the data shows nominal linear increase in pregnancy success as sperm motility improves, having Coefficient of Determination 0.008 indicates sperm motility stands as ‘strong’ male fertility indicator compared to the of 0.006 found for both male age and sperm count. 

Conclusion: Sperm motility has a slight upward trend. Though it is a relative male fertility indicator, it shows that once a baseline is met, further improvement in motility do not significantly increase the probability of pregnancy success.

<img width="600" height="371" alt="_Sperm Motility vs Pregnancy Success" src="https://github.com/user-attachments/assets/ab4c8d7d-7261-4d9d-97e7-9406bac8ca50" />


# Overall conclusion

The comprehensive analysis of this fertility health dataset displays a significant disparity between the impact of female and male physiological factors on pregnancy outcomes. Utilizing DuckDB for data processing and Google Sheets for visualization, the results consistently highlight those female variables mainly maternal age, BMI and the presence of PCOS are the most determinants of pregnancy success.
In contrast, male factors demonstrated little statistical relationship once baseline health thresholds were met. In conclusion, these findings emphasize that while reproductive health is shared between female and male couples, the biological factors analysed in this dataset indicate that female health profiles are dominant influencers of pregnancy success. 





