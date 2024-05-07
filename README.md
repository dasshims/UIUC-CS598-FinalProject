## Which Explanation Makes Sense? A Critical Evaluation of Local Explanations for Assessing Cervical Cancer Risk Factors


## Project Proposal submitted for CS598: Deep Learning For Healthcare, SP24



### Instructors:
Jimeng Sun
Siddhartha Laghuvarapu



### Prepared by:
Himangshu Das 				hdas4@illinois.edu
Jeremy Samuel 				sjeremy3@illinois.edu
Mahesh Matta 				maheshm3@illinois.edu


Original paper - [A-Critical-Evaluation-of-Local-Explanations-for-Assessing-Cervical-Cancer-Risk-Factors ](https://github.com/cwayad/Local-Explanations-for-Cervical-Cancer)- 

Citations: 
Mustafa WA, Ismail S, Mokhtar FS, Alquran H, Al-Issa Y. Cervical Cancer Detection Techniques: A Chronological Review. Diagnostics (Basel). 2023 May 17;13(10):1763. doi: 10.3390/diagnostics13101763. PMID: 37238248; PMCID: PMC10217496.

#### Steps to Reproduce:
Open DL4H_Team_84.ipynb Notebook:
In the Jupyter interface, navigate through the list of notebooks and click on the notebook you wish to run.
Run the Notebook:
Execute a single cell: Click on the cell and press Shift + Enter.
Run all cells: Go to the menu bar, select Kernel, then Restart & Run All.

#### Methodology
The methodology involves training various machine learning models on the preprocessed data to predict cervical cancer risk, applying local explainability techniques to interpret the predictions, and assessing the quality of different explanations.

#### Models and Local Explanations
Models Used: Logistic Regression, Random Forest, SVM, KNN, MLP
Explanation Techniques: LIME, SHAP, Integrated Gradients
Computational Requirements
Hardware: Recommended to use a machine with at least 16GB RAM and a modern multi-core CPU.
Software: Python 3.x, Jupyter Notebook.
Libraries: scikit-learn, numpy, pandas, matplotlib, lime, shap.

#### Project Overview
Cervical cancer is a critical global health issue, and early detection is crucial for effective treatment. Advanced machine learning models offer promising ways to predict and understand risk factors, but their "black-box" nature can limit their clinical utility. This project aims to address this gap by evaluating the effectiveness of local explanation methods like LIME, SHAP, and Integrated Gradients, among others.

#### Data
The data used in this project is the Cervical cancer risk factors dataset from the UCI repository, available here. The dataset includes demographic information, habits, and medical history of 858 patients.

Download Instructions
import gdown url = 'https://drive.google.com/file/d/1jH2A93bp2z86Avm08ev7Fz6khDDQia63/view?usp=sharing'
output = 'risk_factors_cervical_cancer.csv'
gdown.download(url=url, output=output, fuzzy=True)

#### Results

In this project, we compare the local feature attribution methods
in order to identify key risk factors causing cervical cancer for individual patients and
demonstrated on two patients having very similar characteristic but different predictions
(cancer and no cancer). Overall we observe that though the explainers may agree on the
importance of some features, there is no single explanation or technique that performs
optimally across all metrics of consistency, compactness, stability, faithfulness and accuracy.
Rather, a clinician may choose an explanation method based on the context or choose to
compute a weighted sum of these metrics.

Local explanations are also
not meant to replace insights from aggregation, but may be preferable to determine those
risk factors most likely to affect patients individually.
Regardless of the nature of the SHAP used, one obtains very similar feature importance.
However, SHAP values are all largely determined by one predominant driving risk factor
namely prior HPV infection and explanation quality significantly drops if this feature is
not available. Methods such as Local surrogates, LIME and Kernel SHAP learn local
interpretable models in the neighborhood of the instance we desire to explain, however can
be sensitive to the choice of neighbourhood for two instances with the same characteristics
and predictions. 

Our approach allows selecting the suitable explanations to reason about each patient’s
risk of developing cervical cancer, while satisfying several desired explanatory properties.
There are many potential avenues for future research, such as extending our framework
to other healthcare applications and areas where explanation is needed. 
