# Breast-Cancer-Study
A repository for expanding on a previous project I did for my DS2001 class (Fall 2023) on breast density and cancer risk in my MATH6243 class (Spring 2026). 
## How Does Breast Density Relate to Cancer Risk?

**MATH 6243 - Spring 2026**

** Data **
Data Source: The data used in this project is from the Breast Cancer Surveilance Consortium and was accessed on 9th March 2026 from <https://www.bcsc-research.org/datasets/rf> and <https://www.bcsc-research.org/datasets/mammography_dataset>.

We are using a dataset found through the BCSC Organization that organizes risk factor data for breast cancer for 1,522,340 records. This data ranges in collection date from January 2005 to December 2017 and was originally collected to describe the distribution of breast cancer risk in the general population or to explore relationships among breast cancer risk factors. This dataset will help us explore how our focus risk factors inpact breast density.

We are also using a dataset found through the same organization which includes 40,000 records of mammogram assessment, subsequent breast cancer diagnosis within one year, and associated risk factors. The data ranges in collection date from January 2005 to December 2008 and was originally collected for teaching data analysis, epidemiological study design, or statistical methods for binary outcomes or correlated data. This dataset will help us explore the correlation between breast density and cancer risk as well as assessment-effectiveness.

**Background**

We are looking at how different factors can affect breast densitity and then subsuquently affect cancer diagnoses. In 2020, there were 2.3 million women diagnosed with breast cancer and 685,000 deaths globally caused by it. Mammography is a technique that is extremely important in diagnosing breast cancer, but breast density can significantly impact its effectiveness, making it harder to detect tumors. There are four categories of breast density: fatty, scattered, heterogeneously dense, and extremely dense.

Women who have dense breasts can also be at increased risk for breast cancer. According to Yale Medicine, having extremely dense breasts can make you 2 times more likely to develop breast cancer in comparison with those who have scattered breast density, and 1.5 times more likely for heterogeneously dense breasts. Some studies point to an even higher correlation.

According to the CDC, one is more likely to have dense breasts if they are: younger, pregnant/breastfeeding, taking HRT, or have a lower body weight. Our proposal is to study how breast density changes with these factors and others so that anyone at risk of breast cancer can be more aware of the associated risk factors as time goes on.

**Questions**

1. How do age, BMI, and HRT impact breast density?
For these first three questions, we will plot bar graphs with age, BMI, and HRT usage on the x axis and count on the y axis. Either each breast density will be represented with different colored bars, or we will plot four separate graphs for each breast density group. We will ignore instances with unknown values.


2. How does breast density impact cancer diagnosis?
For this question, we will plot bar graphs with breast density on the x axis and count on the y axis, noting different cancer assessments either with different colors of bars or by making separate graphs for each cancer assessment. The cancer types in our model are: needs additional imaging, negative, benign, probably benign, suspicious abnormality, and highly suggestive of malignancy.

3. How does breast density impact false negatives?
For this question, we will plot scatter plots with false negatives on the y axis against risk factors on the x axis, making points of different colors for each breast density. Risk factors will consist of age, BMI, and HRT usage in our study, and how we interpret this graph will depend on our findings for earlier questions regarding the correlation between each risk factor and breast density.





