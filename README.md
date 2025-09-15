# Classification of Fetal Arrythmia using Electrocardiogram Signal Processing and Machine Learning

This project evaluates the efficacy of Non-Invasive Fetal Electrocardiogram (NI-fECG) in detecting fetal cardiac arrhythmia via ML tools as an alternative to conventional invasive, expensive, risky, and manual diagnostic methods



**System Architecture:**

<img width="860" height="483" alt="image" src="https://github.com/user-attachments/assets/041bcdf4-21f6-40dc-ae66-ab24d4bced38" />


**Signal Processing:**

[INSERT IMAGES OF BEFORE AND AFTER PROCESSING]



**Feature Extraction:**

Using the `NeuroKit2` package to isolate R-peaks and perform gradient detection for the remaning peaks:

<img width="394" height="304" alt="image" src="https://github.com/user-attachments/assets/7b1a4f12-a3cf-4427-aa72-fc57926ba686" />

Finally, time domain features are calculated using the sampling frequency according to `Nyquist Theorem.` <br/>
The features are also plotted by group (arrythmiac & healthy). 

[INSERT MATH OF FREQUENCY DOMAIN] [INSERT BOXPLOTS]



**FINAL PERFORMANCE METRICS**

<img width="442" height="205" alt="image" src="https://github.com/user-attachments/assets/f7236262-56a8-489b-a1fd-9612186e0370" />





