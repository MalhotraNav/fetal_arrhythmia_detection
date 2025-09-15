# Classification of Fetal Arrhythmia using Electrocardiogram Signal Processing and Machine Learning

This project evaluates the efficacy of Non-Invasive Fetal Electrocardiogram (NI-fECG) in detecting fetal cardiac arrhythmia via ML tools as an alternative to conventional invasive, expensive, risky, and manual diagnostic methods.  

---

## System Architecture  

<img width="860" height="483" alt="image" src="https://github.com/user-attachments/assets/041bcdf4-21f6-40dc-ae66-ab24d4bced38" />  

---

## Signal Processing  

<img width="798" height="240" alt="image" src="https://github.com/user-attachments/assets/7d674c78-e372-42ef-ad80-d0bf268d0f6e" />  

---

## Feature Extraction  

Using the `NeuroKit2` package to isolate R-peaks and perform gradient detection for the remaining peaks:  

<br/>

<img width="810" height="128" alt="image" src="https://github.com/user-attachments/assets/3bc3300f-3211-4608-98ee-3ca8bbbf462f" />  

<br/>
<br/>  

<img width="591" height="456" alt="image" src="https://github.com/user-attachments/assets/7b1a4f12-a3cf-4427-aa72-fc57926ba686" />  

---

## Time Domain Features  

Time-domain features are calculated using the sampling frequency according to the `Nyquist Theorem`:  

$$
P_\text{seconds} = \frac{x_{\text{sample}}}{f_\text{sample}}
$$  

<p align="center"><em>Converts sample indices to time in seconds.</em></p>  

$$
\bar{P}_{\text{interval}} = \frac{1}{N} \sum_{i=0}^{N-1} (P_{i+1} - P_i)
$$  

<p align="center"><em>Finds average time between consecutive ECG peaks.</em></p>  

<br/>  

The features are also plotted by group (**arrhythmic & healthy**):  

<img width="895" height="535" alt="image" src="https://github.com/user-attachments/assets/372fe6f6-baa2-434a-975a-e104d476511b" />  

---

## Final Performance Metrics  

| **Model** | **Accuracy** | **Recall** | **Precision** | **F-score** | **Brier-Score** |
|-----------|--------------|------------|---------------|-------------|-----------------|
| LR        | 0.66         | 0.66       | 0.80          | 0.63        | 0.34            |
| **LDA**   | **0.83**     | **0.83**   | **0.88**      | **0.83**    | **0.17**        |
| KNN       | 0.66         | 0.66       | 0.80          | 0.63        | 0.34            |
| DT        | 0.50         | 0.50       | 0.50          | 0.49        | 0.50            |
| GNB       | 0.66         | 0.66       | 0.66          | 0.66        | 0.34            |
| **SVM**   | **0.83**     | **0.83**   | **0.88**      | **0.83**    | **0.17**        |

<p <em>Table: Performance comparison of classification models after hyperparameter tuning.</em></p>
