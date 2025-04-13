# M4M SQA Project

![Project Image](https://gitlab.utu.fi/yazhao/m4m_sqa/-/raw/main/finalflowchat.png?ref_type=heads "Project Image for M4M SQA")

**Figure 1.** Pipeline of the proposed framework for photoplethysmography (PPG) signal quality assessment (SQA) and heart rate (HR) estimation. The process is divided vertically into a training phase (top) and a testing phase (bottom), and horizontally into two functional modules: the SQA Module (enclosed by a pink dashed box) and the HR Estimation Module (enclosed by a blue dashed box). Dataset I (clinical recordings) and Dataset II (MIMIC-IV) are used in three train–test configurations (A–C). Raw PPG signals are preprocessed through filtering, normalization, segmentation, and peak detection. The SQA module involves feature extraction, feature selection, and machine learning (ML) model training using leave-one-subject-out (LOSO) cross-validation. During testing, predicted quality labels are used to guide downstream HR estimation using signal-based and label-based filtering strategies. HR is evaluated against ECG-derived HR, and performance is measured using mean absolute error (MAE).
<!-- ## Related Links

- [data](https://seafile.utu.fi/f/33741258c4064785b586/)
- [model, feature map and hr](https://seafile.utu.fi/f/81640b13fac64a258631/) -->

## Project Dependencies

This project requires the following packages with specified versions to ensure compatibility and proper functionality:

- **numpy**: `1.26.0`
- **matplotlib**: `3.8.1`
- **scipy**: `1.11.3`
- **neurokit2**: `0.2.7`
- **pandas**: `2.2.0`
- **seaborn**: `0.13.0`
- **sklearn**: `1.3.2`
- **fastdtw**: `0.3.4` - Dynamic Time Warping (DTW) algorithm with an O(N) time and memory complexity. [More Info](https://github.com/slaypni/fastdtw)
- **vitalwave**: `0.0.1` - [Vitalwave Official Page](https://github.com/Antonius-Markus/bio_library)
- **rlscore**: `0.8` - [RLScore Official Page](https://github.com/aatapa/RLScore)


## Notes

1. File New_M4M contain all raw data
2. train_SR = SR data used for train
3. test_SR = SR data used for test
4. Model_SR_AF contain the model trained by both SR and AF data.
5. Model_SR contain model trained by SR data
6. Model_AF contain model trained by AF data
data_60s contain the feature map and hr get from raw data. 
You can use these feature map directly.

### Start

```bash
cd path/to/your/project
git remote add origin https://gitlab.utu.fi/yazhao/m4m_sqa.git
git add .
git commit -m "Initial commit"
git branch -M main
git push -u origin main

