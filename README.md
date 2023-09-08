# Defects localization in images using deep learning-based classification with CAM output
This repository includes code models used in IDAACS'2023 conference article *'Defects localization in images using deep learning-based classification with CAM output'* by **Rytis Augustauskas**, **Lukas Zabulis**, **Arūnas Lipnickas**, **Simas Jokubauskas**.

Modified image classification architectures are used with multihead output to predict and roughly segment images without pixel-wise annotation. It is making predictions in a single iteration.

The model is being trained as binary classified, then converted to a 2-output model in which one output is for classification score, the other for CAM explainability.

Check the article for more details. 

# Launch

1. Install requirements (**Tensorflow 2.12**, **OpenCV 4.7.0.72**, **Matplotlib 3.7.1**, **Albumentations 1.3.0**). Optionally, use the following command:  
```
pip install -r requirements.txt
```

2. Check the [provided Jupyter Notebook](https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/CAM%20classifiers.ipynb) for training, model conversion and inference routines. *Better description upcoming after conference*
