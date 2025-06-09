# DeepLearningProject

## Group Members

|Name | Email |
| --- | --- |
| Tania Pazos | tania.pazos01@estudiant.upf.edu | 
| Yuyan Wang | yuyan.wang01@estudiant.upf.edu | 

## About the Project

This project was developed as part of the Deep Learning course at UPF. Our goal was to explore the trade-off between model size and performance for the task of **Facial Emotion Recognition** on the FER2013 dataset. In particular, we focused on designing lightweight architectures (under 500k parameters) suitable for low-resource environments, while achieving fair performance across all emotion classes — especially in the presence of significant class imbalance.

The experiments performed here provide valuable insights into the behavior of compact CNN architectures such as ResNet and MobileNetV2 on a challenging imbalanced dataset. While several limitations remain, including the difficulty of distinguishing subtle emotions and the tendency of some models to overfit, the project highlights promising directions for building efficient FER systems.

---

## How to run the notebooks

This project consists of several Jupyter notebooks that guide you through the full experimentation pipeline: from exploratory data analysis (EDA) to model training and result visualization.

### Environment Setup

We recommend running the project in a virtual environment. Install the dependencies using:

```bash
pip install -r requirements.txt
```

After having installed the dependencies, you should be able to run any notebook in this repository. You can now open and run the notebooks in your preferred Jupyter environment.

### Folder Structure

Please note that the `data` folder provided in this repository is empty due to size restrictions. To run the notebooks, you should place your dataset inside the `data` folder with the following structure:

```
data/
├── train/
│   ├── angry/
│   ├── disgust/
│   ├── fear/
│   ├── happy/
│   ├── neutral/
│   ├── sad/
│   ├── surprise/
├── test/
│   ├── angry/
│   ├── disgust/
│   ├── fear/
│   ├── happy/
│   ├── neutral/
│   ├── sad/
│   ├── surprise/
```

Each subfolder should contain the corresponding images for each emotion class.

### Notebooks Overview

- `EDA.ipynb`  
  Performs Exploratory Data Analysis on the dataset, including visualizations of class distributions and sample images.

- `KerasBaseline.ipynb`  
  Trains and evaluates the VGG16 baseline model.

- `ResNet.ipynb`  
  Defines, trains, and evaluates the custom ResNet variant.

- `MobileNetV2.ipynb`  
  Defines, trains, and evaluates the custom MobileNetV2 variant.

- `plots-resnet.ipynb` and `plots-mobv2.ipynb`  
  Generate plots for visualizing performance metrics and embedding spaces of the trained ResNet and MobileNetV2 models.

### Outputs

All experimental results (metrics, plots, intermediate model outputs) are saved in the `results/` folder.

