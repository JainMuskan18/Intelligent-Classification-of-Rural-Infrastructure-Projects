# 🛣️ Intelligent Classification of Rural Infrastructure Projects

## 📌 Project Overview

This project addresses a real-world challenge in the rural development domain of India — automating the classification of infrastructure projects under the **Pradhan Mantri Gram Sadak Yojana (PMGSY)**. As the scheme has evolved into PMGSY-I, PMGSY-II, RCPLWEA, and others, the ability to accurately classify thousands of projects is critical for budget planning, monitoring, and analysis.

Manual classification is time-consuming and error-prone. We built a **Machine Learning pipeline** that can automatically classify projects based on their **physical and financial attributes** using a cleaned dataset and deployed model.

---

## 🎯 Objective

To build, train, and deploy a machine learning model that classifies each rural infrastructure project into its correct PMGSY scheme using structured data such as cost, road length, surface type, terrain, and location.

---

## 🧠 Technologies Used

- **Python**  
- **Pandas**, **Scikit-learn**, **Joblib**, **Matplotlib**, **Seaborn**
- **IBM Watsonx.ai Studio**
- **IBM Cloud Object Storage**
- *(Optional)* IBM Watson Machine Learning (for deployment)

---

## 📁 Dataset Details

- Cleaned CSV dataset with labeled `PMGSY_SCHEME` column
- Features include:
  - `Project_Cost`, `Road_Length`, `Surface_Type`, `State`, `Terrain`, etc.
  - Target: `PMGSY_SCHEME` (e.g., PMGSY-I, PMGSY-II, RCPLWEA)

---

## 🔧 System Development Approach

- **Data Cleaning**: Removed nulls, encoded categorical features, standardized numerical ones
- **Model Training**: Used `RandomForestClassifier` for classification
- **Model Evaluation**: Accuracy ~92%, strong F1-scores across all classes
- **Deployment**: Model saved as `.pkl`, zipped, and ready for deployment via IBM Cloud

---

## 🧪 Results

- **Accuracy**: ~92%
- **Classification Report**:
  | Scheme     | Precision | Recall | F1-Score |
  |------------|-----------|--------|----------|
  | PMGSY-I    | 0.93      | 0.91   | 0.92     |
  | PMGSY-II   | 0.91      | 0.92   | 0.91     |
  | RCPLWEA    | 0.89      | 0.90   | 0.89     |

- **Visuals**:
  - Confusion Matrix
  - Heatmap of classification report
  - Sample output after deployment (see `deployment_output_result.png`)

---

## 🚀 Deployment (Optional but Recommended)

If enabled, the trained model can be deployed on **IBM Watson Machine Learning** via:
- Upload `.pkl` file and schema
- Create deployment using Watsonx.ai Studio or API
- Predict using deployed model endpoint

---

## 📈 Future Scope

- Integrate with GIS for visual tracking of project locations
- Add explainability (e.g., SHAP) for transparency in predictions
- Extend classification to include more scheme phases or funding types
- Create dashboards for real-time monitoring

---

## 🧾 References

- [PMGSY Official Portal](https://pmgsy.nic.in)
- IBM Cloud & Watsonx.ai Docs
- Scikit-learn Library
- Research papers on infrastructure data mining

---

## 👩‍💻 Developed By

**Muskan Jain**  
B.Tech – CSE (AI & ML)  
Certified in IBM AI, Cloud, and ML tools  
