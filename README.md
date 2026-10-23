# Brain Tumour Detection Using Deep Learning

A notebook-based project exploring four-class brain MRI image classification with transfer learning and image-processing / generative-AI experiments.

## Objective

Classify MRI images into four categories:

- Glioma
- Meningioma
- No tumour
- Pituitary tumour

## Methodology in the notebook

1. Load and inspect labelled MRI images.
2. Resize and normalize images and experiment with training-time augmentation.
3. Use MobileNetV2 transfer learning for image classification.
4. Explore denoising-related processing and GAN-based image generation.
5. Evaluate predictions using accuracy, precision, recall, F1-score, confusion matrix, and ROC/AUC plots.

The notebook includes Google Colab-specific steps and expects a dataset arranged into `Training/` and `Testing/` directories, each containing one subdirectory per class. See the notebook for the actual code and paths.

## Dataset

The notebook references a dataset hosted on Google Drive:

https://drive.google.com/drive/folders/1Cgavdzj3gntbrXDdhz9rgtw3b6cz4HuC?usp=sharing

Check the dataset's license and terms before redistributing any images. The dataset itself is not included in this repository.

Expected directory layout:

```text
data/
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── notumor/
│   └── pituitary/
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── notumor/
    └── pituitary/
```

## Run

Recommended: open `brain_tumor_detection.ipynb` in Google Colab or Jupyter. In Colab, upload/mount the dataset and update any paths to match your environment. Install dependencies as needed using `requirements.txt`.

## Results and limitations

The project notes a **reported test accuracy of 88.71%**. Treat this as a preliminary reported figure, not a verified benchmark: the notebook's evaluation output should be regenerated and reconciled with the reported accuracy before relying on it. Confirm test-generator ordering, class-index mapping, duplicate/near-duplicate images, and patient-level separation. Do not claim that denoising or GAN-based augmentation improved performance unless controlled ablation experiments support that conclusion.

This is an educational research project, not a clinically validated diagnostic tool. Predictions must not be used to make medical decisions.

## Repository contents

- `brain_tumor_detection.ipynb` — original project notebook.
- `requirements.txt` — core Python packages used by the notebook.

## License

No project license has been specified. Add a license only after deciding how you want others to use, modify, and distribute your work. Dataset licensing is separate.
