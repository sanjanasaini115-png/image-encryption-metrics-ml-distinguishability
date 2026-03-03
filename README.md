# Image Encryption Metrics vs ML Distinguishability

This project tests whether standard image-encryption evaluation metrics are sufficient to compare encryption schemes.
We compute commonly reported metrics (Entropy, Corr-H/V/D, NPCR, UACI) on encrypted images and train ML models to
distinguish AES from Chaos/XOR encryption using only these metrics.

## Metrics Used
- Entropy
- Correlation: Horizontal, Vertical, Diagonal
- NPCR (%)
- UACI (%)

## Models
- Random Forest Classifier
- Support Vector Machine (SVM)

## Results (Classification Accuracy)
| Resolution | Random Forest | SVM |
|-----------:|--------------:|----:|
| 512×512    | 43.33%        | 36.66% |
| 1024×1024  | 59.09%        | 59.09% |

## Data Files
- `Book512_512.xlsx` : metrics for 512×512 encrypted images
- `Book1024_1024.xlsx` : metrics for 1024×1024 encrypted images

## Conclusion
If a model can separate encryption families using only these standard metrics, the metrics may retain method-specific
patterns and may not be fully sufficient as stand-alone evidence of security.
