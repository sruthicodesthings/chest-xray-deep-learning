# Chest X-ray Deep Learning: Classification and Detection

Research notebook exploring **Vision Transformer (ViT) classification** of normal versus pneumonia chest X-rays and **Faster R-CNN detection** of radiographic abnormalities.

> **Research prototype, not a clinical diagnostic tool.** Results below come from saved notebook outputs and accompanying analysis; experiments were not rerun for this GitHub cleanup.

## Experiments

| Track | Approach | Comparison |
| --- | --- | --- |
| Classification | Custom ViT with patch embeddings and multi-head self-attention | Standard sampling vs. class-balanced sampling |
| Detection | Faster R-CNN with ResNet-50-FPN | Standard vs. smaller region-proposal anchors |

### Classification

The notebook implements image preprocessing, a Vision Transformer, training and evaluation routines, and a controlled class-balanced sampling experiment. Its written analysis reports **77.88% accuracy** for an initial baseline evaluation; the controlled sampling comparison uses a separate validation protocol and should **not** be treated as directly comparable to that baseline.

### Detection

The detection experiment uses Faster R-CNN, bounding-box annotations, intersection-over-union (IoU) evaluation, visual inspection, and a controlled anchor-size comparison. See the notebook for recorded outputs and limitations.

## Repository

```text
notebooks/chest_xray_experiments.ipynb   # Main research notebook, saved outputs retained
requirements.txt                        # Approximate dependencies; not a lockfile
.gitignore                              # Excludes datasets, checkpoints and local outputs
```

## Getting started

1. Obtain the chest X-ray datasets from their original providers and follow their terms.
2. Create a Python environment and install dependencies: `pip install -r requirements.txt`.
3. Open `notebooks/chest_xray_experiments.ipynb` in Jupyter or Colab.
4. Update dataset paths and environment-specific setup cells before running.

**No GPU rerun is necessary to inspect the code and saved results.** Reproducing training does require the original data, suitable compute, and compatible package versions. The notebook may include Colab-specific commands and has not been end-to-end tested in this reorganized form.

## Limitations

- Dataset access and preprocessing must be verified before reproduction.
- Experimental comparisons use their stated evaluation splits; metrics from different protocols should not be compared directly.
- The notebook's saved outputs are historical artifacts, not independently verified results.
- Model checkpoints and datasets are not included.
- No external clinical validation has been established.

## Development history

The first five commits are **reconstructed from successive notebook versions** in an archive, using the archive's modification timestamps as estimated author dates (October 20–21, 2026). Their actual committer dates record when this Git history was generated. Assignment-specific presentation was removed from each public-facing snapshot; the historical commits do not represent original Git commits.

## Attribution

This project was adapted from coursework into a standalone research portfolio repository. The notebook contains the implemented experiments and analysis; source datasets, libraries, and model components retain their respective licenses and attribution requirements.


## Data and publication safety

The dataset, patient-level radiographs, detection visualizations, and model checkpoints are **not distributed** in this repository. Embedded notebook images were removed for safer public sharing; previously recorded text-only training logs and metrics are retained where available. Obtain source data separately under the dataset provider’s terms. The notebook has not been rerun after this packaging change.
