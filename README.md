# 🏆 Humana - Mays 2024 Healthcare Analytics Case Competition
# 🏥 Bridging the Preventive Care Gap: Predicting Unengaged Medicare Advantage Members

## Project Overview
This project was developed as part of the Humana-Mays Healthcare Analytics Case Competition 2024. It focuses on identifying unengaged Medicare Advantage members and devising strategies to enhance preventive care engagement.                                                                                              

🚀 **Goal**: Develop a predictive model to identify unengaged Medicare Advantage members and improve preventive care outreach.                                  
🔍 **Impact**: Enhancing patient engagement can reduce healthcare costs and improve overall health outcomes.                                                                 

### 🎯 Achievement  
✅ **Qualified for the First Round** 
![First round qualifier](https://github.com/RakeshsarmaKarra/Humana-Mays-2024-Healthcare-Analytics-Case-Competition/blob/main/Humana%20%26%20Mays%20-%20Top%2050.jpg)

## Research Questions                                                                                                                                  
- What are the behaviors and underlying barriers among members in LPPO plans who are not engaging in preventive care with a PCP?                                     
- Which members are not likely to complete a preventive PCP visit in the current calendar year?                                                                 
- How can primary care physicians and specialists address low patient engagement in preventive care?                                                                 
- How are Humana’s competitors addressing this problem?                                                                                                                 
- What recommendations can Humana adopt to increase engagement through outreach, process improvements, and other initiatives?                                                 
  
## Brief Introduction About Data                                                                                                                                  
📊 Data Description:                                                                                                                                  
| Attribute         | Description                                            |
|------------------|--------------------------------------------------------|
| **Total Records** | 1.5M members (training dataset)                        |
| **Features**      | 300 variables across 14 datasets                       |
| **Key Variables** | Member demographics, claims history, social determinants, provider interactions, risk scores, etc. |
| **Target Variable** | `Preventive_Visit_Gap_Ind` (0 = Engaged, 1 = Unengaged) |

## ✔ Handling Missing Data:                                                                                                                                  
Rows/Columns with >50% missing values were removed.                                                                                              
Categorical missing values were labeled as "Unknown" where applicable.                                                                                    
Aggregated missing claims data for analysis.                                                                                                                                  

## ✔ Feature Engineering:                                                                                                                                  
One-hot encoding for categorical variables.                                                                                                                                  
Risk category aggregation (Downside, Upside, Global, Rewards).                                                                 
Behavioral indicators (e.g., engagement score, frequency of visits).                                                                                       
Health status clustering using risk scores and chronic conditions.                                                                                    

## Modeling Approach                                                                                                                                  
🔍 Models Evaluated:                                                                                                                                  
Logistic Regression (Baseline)                                                                                                                                  
Naïve Bayes                                                                                                                                  
LightGBM                                                                                                                                  
XGBoost (Final Model) ✅                                                                                                                                  

**🏆 Best Model: XGBoost**                                                                                                                                  
Accuracy: **68.7%**                                                                                                                                  
Precision: **65.7%**                                                                                                                                  
Recall: **63.5%**                                                                                                                                  
F1 Score: **64.5%**                                                                                                                                  
ROC-AUC: **0.76**                                                                                                                                  

## 🔧 Hyperparameter Optimization:                                                                                                                                  
Bayesian Optimization + GridSearchCV                                                                                                                                  
L1 & L2 Regularization                                                                                                                                  

## Model Evaluation Metrics                                                                                                                                  
📈 Key Insights from Model Performance:                                                                                                                                  
### Confusion Matrix:                                                                                                                                  
✅ True Positives (Engaged correctly identified): 122,689                                                                                               
✅ True Negatives (Unengaged correctly identified): 87,214                                                                                               
❌ False Positives: 45,480                                                                                                                                  
❌ False Negatives: 50,198                                                                                                                               
![Screenshot](https://github.com/RakeshsarmaKarra/Humana-Mays-2024-Healthcare-Analytics-Case-Competition/blob/main/Confusion%20Matrix.jpg)

### ROC Curve:                                                                                                                                                               
![Screenshot](https://github.com/RakeshsarmaKarra/Humana-Mays-2024-Healthcare-Analytics-Case-Competition/blob/main/ROC%20Curve.jpg)

### Feature Importance (SHAP Values)                                                                                          
### Top Influential Features:                                                                                                                                       
- Veteran Status                                                                                                                                       
- Total Net Paid Cost per Month                                                                                                                                       
- Total Risk Score                                                                                                                                       
- Disability Indicator                                                                                                                                       
- CMS Frailty Index                                                                                                                                       

## Recommendations                                                                                                                                       
✔ Targeted Outreach:                                                                                                                                       
Personalized communication for habitually unengaged members (e.g., veterans, low-income groups).                                             
Multilingual educational campaigns to address health literacy barriers.                                                                                          
✔ Process Improvements:                                                                                                                                       
Automated follow-ups for preventive visits using Electronic Health Records (EHRs).                                                                                          
Mobile health clinics & telehealth services for remote accessibility.                                                                                          
✔ Incentive Programs:                                                                                                                                       
"Bring a Buddy" Program – Encouraging members to bring a companion for preventive visits.                                                                       
Wellness vouchers for new enrollees who complete their first preventive checkup.                                                                                          
## Conclusion                                                                                                                                       
This project provides a data-driven approach to increasing Medicare Advantage member engagement in preventive care. By leveraging machine learning models, behavioral 
insights, and strategic outreach, healthcare providers can significantly improve STAR ratings and patient health outcomes.

🔗 Contact & Credits:                                                                                                                                       
Team Members: 
1. Rakeshsarma Karra (**rakeshsarmakarra@gmail.com**)
2. Chaitanya Krishna Kanth Vankadaru (**chaitanya.vankadaru@gmail.com**)
3. Nirupama Valluru
4. Anulekha Chegoni  
