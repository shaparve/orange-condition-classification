# Orange Condition Classification — Green Pods Labs Assignment 2

## Objective
Classify orange images into the supplied labels: `blackspot`, `canker`, `fresh`, and `grenning`.

## Approaches
- Classical computer vision: CIELAB color histograms + LBP texture features, using SVM and Random Forest.
- Deep learning: MobileNetV2 transfer learning.

## Dataset layout
```text
orange_dataset/
├── train/
│   ├── blackspot/
│   ├── canker/
│   ├── fresh/
│   └── grenning/
└── test/
    ├── blackspot/
    ├── canker/
    ├── fresh/
    └── grenning/
```
The dataset is not included in this repository. Upload `Orange Dataset.zip` in Colab.

## Test results from the Colab run
| Model | Accuracy | Macro Precision | Macro Recall | Macro F1 |
|---|---:|---:|---:|---:|
| SVM | 96.97% | 96.64% | 96.59% | 96.59% |
| Random Forest | 96.97% | 96.64% | 96.59% | 96.59% |
| MobileNetV2 | 93.94% | 93.80% | 93.18% | 93.42% |

The test set contains 99 images. Treat these as split-specific results; use a larger independent dataset before production deployment.

## Prepared-input benchmark
- SVM: 1.013 ms/image
- Random Forest: 80.953 ms/image
- MobileNetV2: 11.161 ms/image

These exclude some loading/preprocessing costs and are not end-to-end latency.

## Reproducibility
1. Open the notebook you executed in Google Colab.
2. Enable GPU if available.
3. Upload the dataset ZIP.
4. Run cells from top to bottom and verify outputs.
5. Keep the original test set separate until final evaluation.

## Submission reminder
Add the actual Colab notebook and any approved model files before pushing to GitHub. Set Colab permissions to anyone-with-the-link can view. Do not claim a public repository or video exists until created.
