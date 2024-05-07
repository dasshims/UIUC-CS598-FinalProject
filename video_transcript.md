Hi,

This is our final project for CS 598, DL4H, where we have done a research study for a deep learning research paper.  

The original paper named - A Critical Evaluation of Local Explanations for Assessing Cervical Cancer Risk Factors

Intro :
Cervical cancer is a life-threatening disease and one of the most prevalent types of cancer affecting women worldwide, Being able to adequately identify and assess factors that
elevate risk of cervical cancer is crucial for early detection and treatment. The early stages of cervical cancer generally show no signs or symptoms. Hence it is very important to be able to detect it sooner. 

The original paper present a critical analysis of several existing local interpretability methods for explaining risk factors associated with cervical cancer. the main goal of the paper is to help clinicians who use AI to better understand which types of explanations to use for analyzing and predicting the risks of cervical cancer. Also, provide a method for analyzing and assessing the performances of various explanations for cervical cancer risk assessment provides a generalizable set of guidelines for clinicians to use to more easily audit a machine learning model’s predictions in high-stake settings, while maintaining predictive accuracy.

Specific approach : 
In the experiments done in this paper it tries to provide and empirical study analysing the performances of different methods for explaining cervical cancer risk factors. For each method, we contextualise how different formulations of these explanations might be appropriate for different patient contexts and when an explainability technique may not be suitable for use. Finally, we provide advice for practitioners as to how to use different types of explanations in practice for assessing and determining key factors driving cervical cancer risk.

This paper also introduces an Algorithm for comparing the performances of various interpretability tools, which could be used to assess how explanations may differ across patients, diseases or applications.

It uses different matrices to to compare how explanations may differ in terms of their accuracy, compactness, consistency and robustness. Moreover, These metrics may be applicable in other contexts, beyond our cervical cancer risk assessment task.
 


Scope of Reproducibility
The original paper focuses on evaluating different explanation methods for assessing cervical cancer risk. It offers a systematic framework for interpreting model predictions and assessing the performance of various explanation techniques. The scope of reproducibility in the project involves replicating the evaluation of explanation methods conducted in the original paper. This includes implementing the systematic approach for interpreting model predictions and comparing the performances of different explanation methods in the context of cervical cancer risk assessment.



Methodology: 

The paper proposes a systematic approach for interpreting the predictions of a black-box model using multiple interpretability methods, and compare the explanations based on desired criteria. The approach consists
of three key phases: 
a) first we train a series of models for cervical cancer risk assessment and choose the best among these models; 
b) next, we interpret the models from a) using a series of local explainability techniques; 
c) we compute a series of metrics to assess the plausibility and coherency of each of the explainability methods considered.

It is as described in the figure below - 


The methodology involves training multiple machine learning models (LR, RF, SVM, KNN, MLP) on preprocessed data to predict cervical cancer risk. The Random Forest model is selected as the best-performing model based on AUC performance. Local explainability techniques are then applied to interpret the predictions of the Random Forest model, including LIME and SHAP, to assess the quality of different explanations for cervical cancer risk assessment. Various metrics are computed to determine which explanation method makes the most sense for assessing cervical cancer risk.


