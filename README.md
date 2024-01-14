## Breast cancer
Breast cancer is the most common cancer in the world, ranking 1 among women.
According to WHO experts, from 800,000 to 1 million new cases of breast cancer are registered annually in the world. This type of cancer ranks second in the number of deaths from cancer in women.


This dataset of breast cancer patients was obtained from the 2017 November update of the SEER Program of the NCI, which provides information on population-based cancer statistics. 
The dataset involved female patients with infiltrating duct and lobular carcinoma breast cancer (SEER primary cites recode NOS histology codes 8522/3) diagnosed in 2006-2010. 
Patients with unknown tumour size, examined regional LNs, positive regional LNs, and patients whose survival months were less than 1 month were excluded; thus, 4024 patients were ultimately included.


## Conclusion:
1. This dataset consists of 4024 rows × 16 columns.
2. 15% died of breast cancer, 85% are alive. Unbalanced dataset 
3. Breast cancer occurs at a young age from the age of 30. The old age is 69 years. 
4. In the white race, 13% died of breast cancer, 72% are alive.
    Among the black race, 2% died, 5% are alive. For others, 1% died, 7% are alive.
5. Grade 2 is more common in all races. 
   Grade 4 is only 3% common in the black race. None of the others
6. Initial forms of cancer and stage IIIA are more common at all ages 
   Advanced forms IIIС occurs from 31 years of age, IIIB from 33 years of age. 
7. Positive hormone receptor status is found in every race. Negative statuses are rare in blacks and others 
8.  Patients diagnosed with breast cancer live an average of 40 to 110 months. 
9. Breast cancer mortality: They die after an average of 40 months (3 years 4 months), regardless of the stage of the disease. In stage IIIB, they die after 35 months.
10. In this dataset :  1. the white race die of breast cancer after living up to 40 months.
                       2. Black race die after living up to 50 months. 
                       3. Others die before 30 months. 
    Why so few? Because this dataset represents many whites than others and blacks.
11. from 30 to 70 years of age day of breast cancer after living the first 40 months. 
     Why do they live so little? Because at a young age there is an aggressive form of breast cancer, the survival rate is minimal. Older age has many others diagnosis

12. In tree-based algorithms, an important variable is 'Survival Months' 
13. For this unbalanced dataset, the AdaBoostClassifier models predict better: Train 0.90, Test 0.89
                                                                        recall score: 0.50
                                                                        f1 score: 0.602
                                                                        precision score: 0.74

    GradientBoostingClassifier is also good, even better than AdaBoostClassifier Train: 0.92, Test: 0.90 but  
                                                                         recall score: 0.47, 
                                                                         f1 score: 0.59
                                                                         precision score: 0.80 lower than                                                                                              AdaBoostClassifier, but not so critical. 

    RandomForestClassifier, DecisionTreeClassifier is very much overfitting. 

   LogisticRegression', 'SVC' predicts very weakly. 
