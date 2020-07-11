# VGG16-Kaggle-Histopathology
This repository contains an implementation of the VGG16 network with Batch Normalization for Invasive Ductal Carcinoma (IDC) image classification

# Dependencies
All the dependencies can be installed using pip/pip3
```
pip install -r requirements.txt
```

# Code
In this repository there are 2 files containing the network.<br/>

The first file is the jupyter notebook VGG_Histopathology.ipynb. This notebook details the network configuration and also contains the training loop and test statistics generation. This file has been developed for the sake of training and testing the network. For the purpose of deployment, the python file in mentioned below can be used.<br/>

The second file is the VGG16_BN.py. This file has the code for the VGG-16 network. It can be used for deploying applications once the model is trained and the saved. The saved model state dictionary and this file are sufficient for deployment. The model can be instantiated through after importing and the model state dictionary can be loaded. The notebook is essential only for training.<br/>
```
# Import Network
from VGG16_BN import VGG16
# Model Instantiation
model = VGG16()
# Model loading Statement
...
```
The above snippet can be used to import and load the model parameters. Please place the python file in the same folder as the file with the above snippet for the import to be successfully executed.

# Dataset
Breast cancer is the most common form of cancer in women. Among them the most common subtype is the invasive ductal carcinoma (IDC). Hence, it is crucial to develop accurate and robust algorithms for identifying and categorizing breast cancer subtypes. Developing automated methods are most beneficial due to their ability to process large amounts of data in a shorter span of time with minimum user involvement.<br/>

To assign an aggressiveness grade to a whole mount sample, pathologists typically focus on the regions which contain the IDC. As a result, one of the common pre-processing steps for automatic aggressiveness grading is to delineate the exact regions of IDC inside of a whole mount slide. This step is already pre-implemented in the context of this dataset. The patches are 50x50 size. For more details please refer to the Kaggle page hosting the [dataset](https://www.kaggle.com/paultimothymooney/breast-histopathology-images)<br/>

The Original dataset is located [here](http://gleason.case.edu/webdata/jpi-dl-tutorial/IDC_regular_ps50_idx5.zip)<br/>

# Citation
1) Janowczyk A, Madabhushi A. Deep learning for digital pathology image analysis: A comprehensive tutorial with selected use cases. J Pathol Inform. 2016;7:29. Published 2016 Jul 26. [doi:10.4103/2153-3539.186902](https://pubmed.ncbi.nlm.nih.gov/27563488/)<br/>
2) Cruz-Roa, Angel & Basavanhally, Ajay & González, Fabio & Gilmore, Hannah & Feldman, Michael & Ganesan, Shridar & Shih, Natalie & Tomaszewski, John & Madabhushi, Anant. (2014). Automatic detection of invasive ductal carcinoma in whole slide images with Convolutional Neural Networks. Progress in Biomedical Optics and Imaging - Proceedings of SPIE. 9041. [10.1117/12.2043872.](https://spie.org/Publications/Proceedings/Paper/10.1117/12.2043872)
