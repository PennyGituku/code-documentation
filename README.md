# Code Documentation Exercise – Mushroom Classifier

This project is submitted as part of the **Code Documentation Exercise** for the Generative AI learning module. It applies AI-powered strategies to document and explain a deep learning model for image classification using PyTorch Lightning.

---

## Exercise Goals

- Select a complex codebase with real-world logic
- Use **Prompt 1** to generate **comprehensive function/class documentation**
- Use **Prompt 2** to explain **intent and step-by-step logic**
- Combine both to produce a final documented version of the code

---

## Selected Code: Mushroom Image Classification

### Description:
A PyTorch Lightning project for classifying mushroom images using a ResNet152 model from `timm`. It includes:

- Data preprocessing using custom `Dataset` and Lightning `DataModule`
- Model definition using pretrained `ResNet152`
- Training, validation, and evaluation
- Visualization and classification report

---

## Files Included

| File | Description |
|------|-------------|
| `mushroom_classifier.py` | Final documented code with docstrings and inline logic |
| `requirements.txt` | Required dependencies for running the project |
| `README.md` | Summary of task and how documentation aligns with the exercise |
| `classification_report.txt` | (Optional) Output of model performance evaluation |

## Project Structure

```text
.
├── mushroom_classifier.py         # Main training script (documented)
├── requirements.txt               # Project dependencies
├── README.md                      # Project overview and instructions
└── /kaggle/input/mushroom1/       # Root directory of the dataset (ImageFolder format)
```
---

## Documented Function (Prompt 1) example

```python
class CustomDataset(Dataset):
    \"\"\"
    Custom PyTorch Dataset to load images from file paths and return transformed images.

    Args:
        path_label (List[Tuple[str, int]]): List of (image_path, label) tuples.
        transform (callable, optional): Optional transform to be applied on a sample.

    Returns:
        Tuple[Tensor, int]: Transformed image tensor and its label.
    \"\"\"
```

## Logic Breakdown (Prompt 2) example 
- Step 1: Image paths and labels are extracted using os.walk

- Step 2: A DataFrame is built for easier manipulation and mapping

- Step 3: A list of (path, label) is passed to a custom dataset

- Step 4: DataModule handles batching and train/val/test splits

- Step 5: ConvolutionalNetwork defines a pretrained ResNet152 classifier

- Step 6: Trainer from Lightning runs training and evaluation

## How to Run
pip install -r requirements.txt
python mushroom_classifier.py
Make sure your dataset is in the expected folder structure or update the path in dir0.

## License
This assignment is submitted for educational purposes under the GenAI curriculum.
