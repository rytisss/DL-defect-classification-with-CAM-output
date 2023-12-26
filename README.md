# Defects localization in images using deep learning-based classification with CAM output
This repository includes code models used in [IDAACS'2023](https://www.idaacs.net/2023) conference article [*'Defects localization in images using deep learning-based classification with CAM output'*](https://ieeexplore.ieee.org/abstract/document/10348813) by [**Rytis Augustauskas**](https://www.linkedin.com/in/rytis-augustauskas-4b99a791/), [**Lukas Zabulis**](linkedin.com/in/lukaszabulis), [**Arūnas Lipnickas**](linkedin.com/in/arunas-lipnickas-888037155), [**Simas Jokubauskas**](linkedin.com/in/simasjokubauskas)

Modified image classification architectures are used with multihead output to predict and roughly segment images without pixel-wise annotation. It is making predictions in a single iteration.

The model is trained as binary classified, then converted to a 2-output model in which one output is for classification score, the other for CAM explainability.

The following CAM explainability map (used for segmentation) can be generated using this approach:

| Dataset | CAM visualization |
| :---: | :---: |
| BSD | <img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/BSD_efficientNetB04down_716ms.gif" width="500"/> |
| Oliena| <img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/oliena_convext4down_716ms.gif" width="500"/> |
| PCB |<img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/PCB_efficientNetB04down_716ms.gif" width="500"/> |

Check the article for more details!

# Launch

1. Install requirements (**Tensorflow 2.12**, **OpenCV 4.7.0.72**, **Matplotlib 3.7.1**, **Albumentations 1.3.0**). Optionally, use the following command:  
```
pip install -r requirements.txt
```

2. Check the [provided Jupyter Notebook](https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/CAM%20classifiers.ipynb) for training, model conversion, inference and plotting routines. At the end of the training (overfit) on sample data [(Oliena)](https://doi.org/10.1016/j.eswa.2022.116710), some images will be rendered:

| Image | Image+defectCAM |
| :---: | :---: |
| <img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/example_results/4_anomaly_rgb.png" width="350"/> | <img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/example_results/4_anomaly_defectCAM_superpos.png" width="350"/> |
| <img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/example_results/6_anomaly_rgb.png" width="350"/>| <img src="https://github.com/rytisss/DL-defect-classification-with-CAM-output/blob/main/res/example_results/6_anomaly_defectCAM_superpos.png" width="350"/> |  
3. Use your data to get new results!

# Aknowledgement  
Research sponsored and conference expenses are covered by [Agmis](https://agmis.com/)

# Citing
```
@INPROCEEDINGS{10348813,
  author={Augustauskas, Rytis and Zabulis, Lukas and Lipnickas, Arūnas and Jokubauskas, Simas},
  booktitle={2023 IEEE 12th International Conference on Intelligent Data Acquisition and Advanced Computing Systems: Technology and Applications (IDAACS)}, 
  title={Defects Localization in Images Using Deep Learning-Based Classification with CAM Output}, 
  year={2023},
  volume={1},
  number={},
  pages={487-492},
  doi={10.1109/IDAACS58523.2023.10348813}}
```
The article ([*'Defects localization in images using deep learning-based classification with CAM output'*](https://ieeexplore.ieee.org/abstract/document/10348813) by [**Rytis Augustauskas**](https://www.linkedin.com/in/rytis-augustauskas-4b99a791/), [**Lukas Zabulis**](linkedin.com/in/lukaszabulis), [**Arūnas Lipnickas**](linkedin.com/in/arunas-lipnickas-888037155), [**Simas Jokubauskas**](linkedin.com/in/simasjokubauskas)) was presented at the [12th IEEE International Conference on Intelligent Data Acquisition and Advanced Computing Systems: Technology and Applications](https://www.idaacs.net/2023), in Dortmund, Germany on September 7-9th, 2023  

