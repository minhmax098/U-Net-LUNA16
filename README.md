# U-Net LUNA16
Lung cancer is the most common form of cancer found worldwide with a high mortality rate. 

Early detection of pulmonary nodules by screening with a low-dose computed tomography (CT) scan is crucial for its effective clinical management. 

Nodules which are symptomatic of malignancy occupy about 0.0125 - 0.025% of volume in a CT scan of a patient. 

Manual screening of all slices is a tedious task and presents a high risk of human errors. 

To tackle this problem we propose a computationally efficient two-stage framework. 

In the first stage, a convolutional neural network (CNN) trained adversarially using Turing test loss segments the lung region. 

In the second stage, patches sampled from the segmented region are then classified to detect the presence of nodules. 

The proposed method is experimentally validated on the LUNA16 challenge dataset with a dice coefficient of 0.984 ± 0.0007 for 10-fold cross-validation.

DATASET USED

The proposed method is experimentally validated by performing 10-fold cross-validation on the LUNA16 challenge dataset.

Dataset download page: https://luna16.grand-challenge.org/

The dataset consists of CT volumes from 880 subjects, provided as ten subsets for 10-fold cross-validation. In each fold of the experiment, eight subsets from the dataset were used for training and one each for validation and testing. The annotations provided includes binary masks for lung segmentation and, coordinates and spherical diameter of nodules present in each slice. LIDC-IDRI dataset from which LUNA16 is derived has nodule annotations in the form of contours which preserves its actual shape. Therefore, we use annotations from LUNA dataset only in Stage 1. The annotations for the nodules from the LIDC dataset is used in Stage 2 (nodule detection) to determine the presence of nodules in image patches.

Dataset download page: https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI

The ground truth annotations were marked in a two-phase image annotation process performed by four experienced thoracic radiologists. Systematic sampling of slices from the CT volumes was performed to ensure equal distribution of slices with and without the presence of nodules.
