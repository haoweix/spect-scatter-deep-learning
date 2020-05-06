README

-------------------------------------------------------------------------------
### Introduction:

This is Python code for (re)producing the results in the paper  
"A deep neural network for fast and accurate scatter estimation in quantitative SPECT/CT under challenging scatter conditions,"  
Haowei Xiang, Hongki Lim, Jeffrey A. Fessler, Yuni K. Dewaraja, 2020  
[<http://doi.org/10.1007/s00259-020-04840-9>]  
Published in
European Journal of Nuclear Medicine (EJNM)

The results show that using deep convolutional neural network (DCNN) can significantly accelerate the scatter estimation process of SPECT/CT while maintaining similar accuracy to previous Monte Carlo (MC) method.



If you use this code, please cite the EJNM paper linked above.

The code is distributed per the Creative Commons Attribution 4.0 license:
https://creativecommons.org/licenses/by/4.0/

```https://github.com/haoweix/spect-scatter-deep-learning```

If you have any questions or need help using this code, please contact haoweix@umich.edu

-------------------------------------------------------------------------------
### Contents:

* Example code for preprocessing, training and testing:
   * ```ipynb/Deep Learning for SPECT scatter estimation v9.ipynb```: Instructions included in the python notebook.
* Pre-trained model used in our paper:  
   * ```model/DCNN_SC_v9.hdf5.h5```: A DCNN model trained with 8 simulated phantom/virtual patient. This is the model we used to generate most of the results in our paper.



### Data:

* Data are separately stored to keep this repository lightweight:
  * Phantom data including training data and testing data are avialble on [https://github.com/haoweix/spect-scatter-deep-learning-data]:
    - ```training_data```: There are 8 simulations in training data and they are evenly seperated into 2 sets (s1 means set No.1 and s2 means set No.2). Each simluation consist of scatter, primary, total and also attenuation map (mu-map). 
    - ```test_data```: There are 6 instances of test data. 
      - ```cat_cali_measure_0822.mat```: measuement of 'calibration' phantom.
      - ```cat_liver_measure_w_noise_0826.mat```: measuement of 'liver' phantom.
      - ```cat_liver_w_noise_Apr2019.mat```: Monte Carlo simulation of 'liver' phantom.
      - ```cat_nema_w_noise_Apr2019.mat```: Monte Carlo simulation of 'NEMA' phantom.
      - ```cat_shell_measure_Aug2019.mat```: First measuement of 'shell' phantom (2 layers of activity).
      - ```cat_shell2_measure_08202019.mat```: Second measuement of 'shell' phantom (3 layers of activity).
  * According to rule of sharing patient data, real patient data is available on [<https://doi.org/10.7302/v07v-z854>].





-------------------------------------------------------------------------------
Copyright 2020-05-05, Haowei Xiang, Hongki Lim, Jeffrey A. Fessler, Yuni K. Dewaraja, University of Michigan