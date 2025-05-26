# CNN Improving Waste Management

> A TensorFlow/Keras image-classification pipeline for sorting common waste materials into seven categories: Cardboard, Food Waste, Glass, Metal, Other, Paper, and Plastic.

## Table of Contents

* [General Information](#general-information)  
* [Technologies Used](#technologies-used)  
* [Conclusions](#conclusions)  
* [Acknowledgements](#acknowledgements)  
* [Contact](#contact)  

## General Information

* **Objective:** Manual waste sorting is labor-intensive and error-prone. This project trains a CNN (from-scratch baseline and EfficientNetB0 transfer-learning) to automatically classify images of waste into seven categories, improving recycling rates and reducing landfill contamination.
* **Dataset:** - **Source:** Public “Waste Segregation” image data (≈7,000 samples in seven folders)  
- **Download:**  
  [Google Drive folder of raw images](https://drive.google.com/drive/folders/1sajIcvGxBemqK_YIHFoY28EyV1Su_b5M)   

## Technologies Used

* **Python 3.x**  
* **pandas** for data manipulation  
* **numpy** for numerical operations
* **tensorflow>=2.11** for model building, evaluation, and hyperparameter tuning  
* **imbalanced‑learn** for handling class imbalance (oversampling)  
* **matplotlib** & **seaborn** for plotting (ROC, precision‑recall, confusion matrices)  

## Conclusions

* **Results:**  
  * Baseline CNN: ~30% validation accuracy (from-scratch)
  * With Augmentation: marginal improvement on scratch model
  * EfficientNetB0 TL: 92–93% validation accuracy after two-stage fine-tuning
  * Per-class F1-scores: 0.86–0.96, with “Paper” slightly lower 

* **Key Takeaways:**  
  * Transfer learning with EfficientNetB0 dramatically outperforms a small scratch CNN on limited data.
  * Strong augmentation (MixUp/CutMix, random erasing) can further improve robustness.
  * Callbacks (EarlyStopping, ReduceLROnPlateau, ModelCheckpoint) are essential to prevent overfitting and capture the best model.

## Contact

Created by [@WolfeTyler](https://github.com/WolfeTyler) and [@uvarajthulasiram](https://github.com/uvarajthulasiram). Feel free to open an issue or reach out with questions or feedback!  
