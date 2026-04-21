# Breast-Cancer-Study
A repository for expanding on a previous project I did for my DS2001 class (Fall 2023) on breast density and cancer risk in my MATH6243 class (Spring 2026). 
## How Does Breast Density Relate to Cancer Risk?

**MATH 6243 - Spring 2026**

**Data**
Data Source: The data used in this project is from the Breast Cancer Surveilance Consortium and was accessed on 9th March 2026 from <https://www.bcsc-research.org/datasets/rf> and <https://www.bcsc-research.org/datasets/mammography_dataset>.

We are using a dataset found through the BCSC Organization that organizes risk factor data for breast cancer for 1,522,340 records. This data ranges in collection date from January 2005 to December 2017 and was originally collected to describe the distribution of breast cancer risk in the general population or to explore relationships among breast cancer risk factors. This dataset will help us explore how our focus risk factors inpact breast density.

We are also using a dataset found through the same organization which includes 40,000 records of mammogram assessment, subsequent breast cancer diagnosis within one year, and associated risk factors. The data ranges in collection date from January 2005 to December 2008 and was originally collected for teaching data analysis, epidemiological study design, or statistical methods for binary outcomes or correlated data. This dataset will help us explore the correlation between breast density and cancer risk as well as assessment-effectiveness.

**Background**
Breast cancer will impact one in eight American women at some point in their life. In 2020, there were 2.3 million women diagnosed with breast cancer and 685,000 deaths globally caused by it. In the current day and age, we have a lot of advancements that make breast cancer less deadly than ever before, and detection methods which allow us to spot the risk before it becomes dangerous. Most notably, mammograms are used. This is a method widely known and accepted, and yet one factor can impact the effectiveness: breast density. There are four categories of breast density: fatty, scattered, heterogeneously dense, and extremely dense. Women who have been told they have dense breasts should be aware that it can make it difficult for screening mammography to detect tumors.
Women who have dense breasts can also be at increased risk for breast cancer. With conventional mammography, while we can be as accurate as 98% in a fatty breast, our sensitivity can drop to as low as 30% in women with extremely dense breasts. Having extremely dense breasts can make you 2 times more likely to develop breast cancer in comparison with those who have scattered breast density, and 1.5 times more likely for heterogeneously dense breasts. Since the only way to test for breast density currently is a mammogram, not being aware of the chance of having high breast density may delay diagnosis of breast cancer when it is potentially more likely to occur. This may make treatment options more limited and complicated to administer.

This project aims to focus on predicting breast cancer risk with a highlighted focus on breast density as a less discussed risk factor compared to some others like age and BMI. It builds off of a previous study I performed on this data, in which I examined how breast density was correlated with other risk factors (age, BMI, and HRT) and how breast cancer and false negative mammogram results were correlated with breast density using simple bar charts. I am using a risk factor dataset obtained through the BCSC Organization which organizes risk factor data for approximately 2 million records. With this data, I aim to use more sophisticated ML techniques to expand on these relationships in a more interpretable way, namely by creating predictive models that estimate breast cancer risk off of a variety of factors. 

I implemented regularization in logistic regression to perform model selection on a wide range of available risk factors: age, race/ethnicity, family history, age at menarche, age at first birth, HRT usage, menopausal status, BMI. I evaluated my resulting model with a binary cross-entropy approach, with a goal of creating a model that accurately estimates cancer risk. This model was built from scratch and compared to a Sklearn-built model. I used a similar method with a random forest approach to allow for ranking feature importance, which I evaluated on specificity and sensitivity results.

For validation, I employed stratified sampling for 10-fold cross validation, stratified in order to account for class imbalance in cancer diagnosis as well as various categoricals such as race and breast density. The regularization in my logistic model also aims to address any issues of multicollinearity between risk factors. 

In terms of data preprocessing, this data is very organized and having worked with it before I have a good background in it. In my past work with this data, as I was studying false negatives by breast density but the nature of how screenings were done didn’t specify false negative results, I instead considered a datapoint a false negative if the mammogram assessment was negative and cancer was diagnosed within a year of the mammogram, and may employ similar logic in the models I create here. For risk factor analysis here, I used past incidence of breast cancer as the variable of interest to get a sense of aggregate risk over an individual’s lifespan.

**Reproduction Instructions**

## Repository Structure

```
├── README.md
├── data/
│   └── raw/
│       └── bcsc_risk_factors_summarized1_092020.csv
│       └── bcsc_risk_factors_summarized2_092020.csv
│       └── bcsc_risk_factors_summarized3_092020.csv
│   └── processed/
│       └── rf_df_bc.csv                        # Processed data used in analysis
├── notebooks/
│   ├── 01_DataProcessing.ipynb                  # Preliminary data cleaning code
│   └── 02_ModelBuilding.ipynb                  # Modeling and Results replication
├── docs/
│    └── Proposal
│    └── Final Report
└── requirements.txt                            # Required python libraries
```

## How to Run

```bash
# Clone the repository
git clone https://github.com/belokonr/Breast-Cancer-Study
cd Breast-Cancer-Study

# Run the data processing (or open in Google Colab / Jupyter)
jupyter notebook notebooks/01_DataProcessing.ipynb

# Run the replication (or open in Google Colab / Jupyter)
jupyter notebook notebooks/02_ModelBuilding.ipynb

```



