# CNN galaxy morphology classifier
Galaxy morphology classifier (E, S, SB) trained on a reduced dataset from Galaxy Zoo 2 from this kaggle dataset: https://www.kaggle.com/datasets/robertmifsud/resized-reduced-gz2-images

## Description
This Jupyter Notebook project trains a convolutional neural network (CNN) to classify 69x69 galaxy pictures from the Galaxy Zoo 2 dataset into the three Hubble sequence classes, Elliptical (E), Spiral (S) and Barred spiral (SB). Class balancing and data augmentation have been implemented to prevent overfitting and enhance data utility. 5-fold cross-validation is used to better estimate model performance, and the best model from the entire training is chosen for reevaluation and saving.
The data can be filtered through two parameters (0 - 1): DATA_FRACTION which controls the fraction of the data that will be used for training and MIN_AGREEMENT that determines the human's classifiers minimum agreement of the data used for training.

## Features
- **Class Balancing**: To ensure equitable training and reduce bias.
- **Data Augmentation**: To enrich the dataset and improve model generalization.
- **Cross-Validation**: For robust model performance evaluation.
- **Best Model Selection**: Based on accuracy and cross-validation results.

## Performance
The performance stats are in the "Stats.xlsx" file. The best models are achieved with a minimum agreement of 0.5 to 0.8 with an accuracy around 0.85, as this interval has sufficient data that is mostly well-labeled. The accuracies for E class and SB class galaxies are > 0.9 but well < 0.76 for class S galaxies. This issue remains unresolved and affects the overall model accuracy.

## Use
The model has been trained in a 12 GB GPU RTX 3060 with GeForce Game Ready Driver version 537.13, Tensorflow 4.10.1 and Python 3.7.16.

## License
This project is under the MIT License. This means that you can use, copy, modify, and distribute this project. However, you must provide attribution back to the original author of the project.
