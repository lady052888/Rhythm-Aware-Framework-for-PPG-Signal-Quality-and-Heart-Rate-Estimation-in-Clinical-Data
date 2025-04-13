# Rhythm-Aware PPG Signal Quality and Heart Rate Estimation

This repository contains the implementation of our proposed framework for assessing PPG signal quality and estimating heart rate across varying cardiac rhythms using clinical data.

🔒 **Note:** The full source code and pretrained models will be made publicly available upon acceptance of the manuscript.

For early access or collaboration inquiries, please contact yazhao@utu.fi.


![Project Image](https://github.com/lady052888/Rhythm-Aware-Framework-for-PPG-Signal-Quality-and-Heart-Rate-Estimation-in-Clinical-Data/blob/main/finalflowchat.png?raw=true)


**Figure 1.** Pipeline of the proposed framework for photoplethysmography (PPG) signal quality assessment (SQA) and heart rate (HR) estimation. The process is divided vertically into a training phase (top) and a testing phase (bottom), and horizontally into two functional modules: the SQA Module (enclosed by a pink dashed box) and the HR Estimation Module (enclosed by a blue dashed box). Dataset I (clinical recordings) and Dataset II (MIMIC-IV) are used in three train–test configurations (A–C). Raw PPG signals are preprocessed through filtering, normalization, segmentation, and peak detection. The SQA module involves feature extraction, feature selection, and machine learning (ML) model training using leave-one-subject-out (LOSO) cross-validation. During testing, predicted quality labels are used to guide downstream HR estimation using signal-based and label-based filtering strategies. HR is evaluated against ECG-derived HR, and performance is measured using mean absolute error (MAE).

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



