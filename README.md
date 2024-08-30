# Little City Foundation Practicum 


## Background Introduction

Little City Foundation (LCF) was founded in 1959 by a group of parents who dreamed of a revolutionary environment for their children who “experts” often said should be institutionalized. Today, through the support of families, individuals, corporate partners, and more, Little City is a vibrant community based throughout the greater Chicago area offering a comprehensive scope of services to individuals with intellectual and developmental disabilities.
For over 60 years, it has been our mission to serve children and adults with intellectual and developmental disabilities by providing the best options and opportunities to live safely, learn continuously, explore creatively, and work productively throughout their lifetime.


## Project description

LCF is requesting a comprehensive analysis of its donor file with an output of a responsive major & mid-level donor prospecting model to elevate and grow the top tier of its donor file – ultimately advancing the mission to support more individuals with disabilities.

Our goal is to have a responsive prospecting model where we can filter our donors – active & future – and be able to seamlessly identify major and mid-level donors based on their giving behaviors, modeled against past and current LCF major and mid-level donors.
The final deliverable will include the responsive prospecting model, and as well as a comprehensive summary of the findings.


## Data & Analysis Brief

- 25 years of donor giving data will be provided; (1) data update will be provided in late January 2024.
- Constituent data will be provided; only including constituent ID, zip code, first gift data, and solicit code data.
- Analysis is expected to include a responsive understanding of what a major (gifts of $10,000 or more) and mid-level (gifts of $1,000 – $9,999) donor profile looks like at LCF.
- The prospecting model will consider a number of data points based on historical and current LCF donor data to formulate the model


## Code Use Instruction

Platform: VS Code (free) 

*New users please see the attached VS_Code_Download.md for reference.*

Input: 

**donor_file**

**gift_file**

*For the privacy, data is not attached here.*


### Step 1. Cleaning & Exploratory Data Analysis
Codes:
- [1.1_donor_eda_and_cleaning.ipynb](model-pipeline/1-Cleaning/1.1_donor_eda_and_cleaning.ipynb)
- [1.2_gift_eda_and_cleaning.ipynb](model-pipeline/1-Cleaning/1.2_gift_eda_and_cleaning.ipynb)

Sample Output: 
- For Tableau Use (Visualization): [countdict.csv](model-pipeline/1-Cleaning/countdict.csv), [sumdict.csv](model-pipeline/1-Cleaning/sumdict.csv)
- For Next Steps of Modeling: giftandzipdata.csv


### Step 2. Merging
Codes: 
- [2-MergeData.ipynb](model-pipeline/2-Merging+3-Feature_Engineering/2-MergeData.ipynb)

Sample Output: 
- merge_file.csv


### Step 3. Feature Engineering
Codes:
- [3-FeatureEngineering.ipynb](model-pipeline/2-Merging+3-Feature_Engineering/3-FeatureEngineering.ipynb)

Sample Output: 
- data_new.csv

which is generated after runnning all cells in [3-FeatureEngineering.ipynb](model-pipeline/2-Merging+3-Feature_Engineering/3-FeatureEngineering.ipynb). 


### Step 4. Models
Codes: 
- [4.1_Random Forest.ipynb](<model-pipeline/4-Models/4.1_Random Forest.ipynb>)
- [4.2_Modeling(logistic regression).ipynb](<model-pipeline/4-Models/4.2_Modeling(logistic regression).ipynb>)
- [4.3_prediction.ipynb](model-pipeline/4-Models/4.3_prediction.ipynb)

Sample Output: 
- prediction 


### Conclusion

Following the order of each step as marked, kindly replace the input at the beginning in every code file:
- Use raw data about donor_file and gift_file only in the very first step about cleaning
- Then for the following steps 2-4, replace the name of output from the previous step at the beginning of code file too
- The final output is about using the best model saved during the traning process to make a prediction

