# Principal Component Analysis of Educational Institutions

# Project Overview
This project involves analyzing a dataset containing information about various colleges and universities. The primary focus is to apply Principal Component Analysis (PCA) to uncover significant patterns and reduce the dimensionality of the dataset. The dataset is titled Education-Post 12th Grade.csv, and the data dictionary for this dataset can be found in the Data Dictionary.xlsx file.

# Table of Contents
* Exploratory Data Analysis (EDA)
* Scaling of Variables
* Covariance vs. Correlation Matrix
* Outlier Detection and Treatment
* PCA Components and Calculations
* Business Implications of PCA

# 1. Exploratory Data Analysis 
# Univariate Analysis

* Distribution Analysis: Charts depicting the distribution of various features such as the number of faculties with PhDs, number of applications accepted, number of applications received, graduation rate, and new student enrollments.

* Key Insights:
High acceptance rate inferred from comparing the number of applications received and accepted.
Graduation rates and new enrollments provide insights into the performance and popularity of institutions.

* Example Plots

Distribution of the dataset

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/b0023ef4-726b-4f30-b061-6623f1e2163d)

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/bfec56f2-04ce-4054-a8c4-b18221917bd4)

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/3382b6b0-1374-4e37-85e6-9aa7d75f8f07)

Number of faculties in the universitites with PhDs

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/1f67b1b4-e58a-4a3b-8926-9ab52697c1da)

Number of applications accepted

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/0a025f3a-c96b-48cf-a679-3e5d046b7b1c)

Number of applications received - Inferred with the previous chart, it is noted that almost all applications are accepted.

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/7394462f-d77d-4790-84a0-3983f54e0c16)

Graduation Rate

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/596eda7e-b8af-48d8-96fb-8007b03f93ed)

Number of new students enrolled

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/c5ae9d6c-77ee-4355-a3b3-fa4d20273960)

# Multivariate Analysis

* Pair Plots: Joint scatter plots for multiple features to visualize relationships between them.
* Key Insights:
Number of new students enrolled across various universities.
Number of applications accepted relative to applications received.
Number of faculties with PhDs and the graduation rate across universities.

* Example Plots

Number of new students enrolled across various universities

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/500f80c9-7294-47d9-a9b0-c564aec6e203)

Number of applications accepted across applications received

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/d195e33a-5a4c-4cec-a34e-6dad580aed8c)

Number of faculties with PhDs in various universities

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/7c2595b4-799e-4b77-92aa-4e42a49bd30d)

Graduation rate across various universities

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/9396a911-39a4-4254-b128-ca0fa8d3142c)

# 2. Scaling of Variables

Method Used: Standard Scaling

Rationale:
Standard scaling was chosen to ensure features are on a similar scale, aiding in the performance and convergence speed of machine learning algorithms.
Ensures the data approximates a normal distribution, which benefits many statistical methods and machine learning algorithms.

# 3. Covariance vs. Correlation Matrix
Covariance: Indicates the direction of the linear relationship between variables.

Correlation: Measures both the strength and direction of the linear relationship.

Observation:
Comparison between the original and scaled data showed minimal differences in covariance and correlation, likely due to prior outlier treatment.

# 4. Outlier Detection and Treatment
Outlier Treatment: Conducted during data cleaning before EDA.

Analysis:
Boxplot comparisons before and after outlier treatment.
Post-treatment observations showed a significant reduction in outliers and better scaling of the dataset.

Boxplot before outlier treatment

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/ba6acc2e-c40d-47e4-9559-8754a24f9620)

Boxplot after outlier treatment

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/dc54a698-3452-406d-8a10-5b189fa7cae9)

# 5. PCA Components and Calculations
Covariance Matrix: Constructed from the scaled data.

Eigenvalues and Eigenvectors:
Eigenvalues indicate the amount of variance captured by each principal component.
Eigenvectors represent the direction of maximum variance in the dataset.

First Principal Component:
Linear combination of original features weighted by the eigenvector values.

Cumulative Variance:
Steep drop in variance explained observed after the 15th component.
Decision to proceed with 25 components based on variance retention.

Heatmap: Visual representation of feature correlations with principal components.

Covariance Matrix

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/01e34f73-4df5-4490-8120-c6270c4f3a07)

Eigen Vectors and Eigen Values

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/ab00e472-fafe-4649-870a-905a7d0c410c)

First Principal Component

Equation of 𝐏𝐂1: -0.2487656Apps+0.33159823Accept+0.0630921Enroll-0.28131053Top10perc+0.00574141Top25perc+ 0.01623744F.Undergrad+0.04248635P.Undergrad+0.1030904Outstate+0.09022708Room.Board-0.0525098Books+0.3589704Personal0.4591395PhD+0.04304621Terminal-0.13340581S.F.Ratio+0.0806328 perc.alumni-0.59583097 * Expend + 0.02407091Grad.Rate

Graphical form of the Linear Equation of PC1

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/031ba977-61c0-404c-8b7c-115718aad82d)

From the below image, visually we can observe that there is steep drop in variance explained with increase in number of PC's. Since there is a steep drop after 15, we proceed with 25 components here.

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/330b4229-bfed-4782-ba86-8421c8786245)

The eigenvectors (Principal components) determine the directions of a new feature space. A Heatmap (shown below) is generated to observe the correlation between various feature and the Principal component itself.

![image](https://github.com/nit-stack/Principal-Component-Analysis-of-Educational-Institutions/assets/174468592/f14aa05b-1f79-44d0-bd17-9b1b75275867)

# 6. Business Implications of PCA

Interpretations:

PC0: Captures the majority of the variance in faculties with PhDs and instructional expenditure per student.
PC2: Significant for estimated book costs and personal spending.
PC3: Majorly captures room and board costs.
PC8: Focuses on part-time undergraduate numbers.
PC11: Relates to instructional expenditure.
PC13: Pertains to full-time undergraduates.

Value of PCA:

Reduces dataset dimensionality while preserving critical information.
Facilitates easier visualization and understanding of data trends.
Enhances the interpretability of the dataset, allowing for better-informed business decisions.
