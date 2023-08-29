# Breast Cancer Histopathological Images Grading Classification using Convolutional Neural Network Models: A Comparative Study

## Citation
If you find our code useful, please consider citing our work using the bibtex:
```
@article{
voon2022performance,
title={Performance analysis of seven Convolutional Neural Networks (CNNs) with transfer learning for Invasive Ductal Carcinoma (IDC) grading in breast histopathological images},
author={Voon, Wingates and Hum, Yan Chai and Tee, Yee Kai and Yap, Wun-She and Salim, Maheza Irna Mohamad and Tan, Tian Swee and Mokayed, Hamam and Lai, Khin Wee},
journal={Scientific Reports},
volume={12},
number={1},
pages={19200},
year={2022},
month=11,
day=10,
issn={2045-2322},
url={https://doi.org/10.1038/s41598-022-21848-3},
doi={10.1038/s41598-022-21848-3},
ID={Voon2022}
}
```

# Abstract
Computer-aided Invasive Ductal Carcinoma (IDC) grading classification systems based on deep learning have shown that deep learning may be used to achieve reliable accuracy in IDC grade classification using histopathology images. However, there is a dearth of comprehensive performance comparisons of Convolutional Neural Network (CNN) designs on IDC in the literature. As such, we would like to conduct a comparison analysis of the performance of seven selected CNN models: EfficientNetB0, EfficientNetV2B0-21k, ResNetV1-50, ResNetV2-50, MobileNetV1, and MobileNetV2. Our findings indicated that the EfficientNetV2B0-21k outperformed other CNN models, with a balanced accuracy score of 0.9666±0.0185 (5-fold stratified cross-validation) and 0.9524 (test result), as well as a recall score of 0.9666±0.0185 (5-fold stratified cross-validation) and 0.9524 (test result), while requiring only a small number of Floating-Point Operations (FLOPs) (0.72B) and parameters (7.1M). In conclusion, we discovered that practically all selected CNN models perform well in IDC grading applications, with an average balanced accuracy of 0.936±0.0189 on stratified 5-fold cross-validation and 0.9308±0.0211on the test set.

# Methodology
<img width="553" alt="image" src="https://user-images.githubusercontent.com/56868536/162567948-e5afa1d2-f1e4-454a-848c-90ac3a73d532.png">
This figure shows the overall flow of our methodology. First, a four-grade dataset (termed the "Four Breast Cancer Grades (FBCG) dataset") will be established using BreaKHis and BCG datasets. The selected 7 pretrained CNN architectures will then be used to model 80% of the FBCG using a 5-fold stratified cross validation approach on the preprocessed data. After confirming the stability of all the models via cross-validation, a final model was trained using all the training data. The final model will be evaluated using a test dataset (the 20% of FBCG). The receiver operating characteristics curves and training versus validation curves will be used to compare and analyse the performance of all the models that were chosen.

# Result
# Stratified five-fold cross validation results
<img width="620" alt="image" src="https://user-images.githubusercontent.com/56868536/162567012-a6c7dadf-28fd-4776-a75a-8a5b08324bb2.png">

<img width="627" alt="image" src="https://user-images.githubusercontent.com/56868536/162567127-9842e232-53ad-4e94-bb00-a14309e53fda.png">

<img width="580" alt="image" src="https://user-images.githubusercontent.com/56868536/162567138-421b6d9d-1714-4864-a097-397d2e00234c.png">

<img width="652" alt="image" src="https://user-images.githubusercontent.com/56868536/162567148-74e08620-0925-45dd-9f99-47c9a2a35cbc.png">

# Test results
<img width="620" alt="image" src="https://user-images.githubusercontent.com/56868536/162567102-4e056aad-050a-49ae-9b4a-af340d08141b.png">


# Conclusion 
In this paper, we compare the performance of seven CNN architectures in IDC grading applications. The Four-Breast-Cancer-Grades (FBCG) dataset was graded into four grades using transfer learning: Grade 0, Grade 1, Grade 2, and Grade 3. The results show that EfficientNetV2B0-21k outperformed all other CNN models in 5-fold stratified cross-validation (balanced accuracy score = 0.9666±0.0185, macro precision = 0.9646±0.0174, recall = 0.9666±0.0185, and F1-score = 0.9642±0.0184), despite having low FLOPs (0.72B), parameters (7.1M), inference time ((0.0758±0.0001s), and training time (0.5592±0.0162h). The EfficientNetV2B0-21k also had the highest balance accuracy (0.9524) and macro recall (0.9524) in the test. Similarly, the MobileNetV1 had the highest balanced accuracy (0.9524), macro precision (0.9545), and macro recall (0.9545) in the test results (0.9524). All CNN models, however, demonstrate significant capability in IDC grading applications, with an average balanced accuracy of 0.9361±0.0189 in the 5-fold stratified cross-validation and 0.9308±0.0211 in the test result. Choosing heavy-weight CNNs is not a problem because the IDC grading application highlights that accuracy and resources are not limiting factors. If future IDC grading applications require real-time settings, a smaller and faster CNN (MobileNetV2) would be preferable. We may expand our work for future development by comparing it to more recent state-of-the-art CNN architectures. In addition, to conduct our comparative performance analysis, we may consider a variety of breast cancer histopathological datasets.

# Data availability
The origin datasets combined for the current study are available in the Four Breast Cancer Grades (FBCG) Dataset, https://web.inf.ufpr.br/vri/databases/breast-cancerhistopathological-database-breakhis/, and breast carcinoma histological images from the Department of Pathology, https://zenodo.org/record/834910#.WXhxt4jrPcs.

FBCG Dataset downloadable link: https://drive.google.com/file/d/1G94HX6g5CC7IC3_m6TrqWFuwzRMoQQ0g/view?usp=share_link

# Pytorch Implementation
check this out for Pytorch Implementation: https://github.com/wingatesv/IDC_Grading_PyTorch.git


