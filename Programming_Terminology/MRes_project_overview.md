[[MRI_Physics]]

[[convolutional_neural_network]]

**Methods and modelling approaches**
- Firstly collected MRI data ([[MRI_Physics]]). 
- Chose SAX orientation as this has the greatest variability in ventricular volume
- Synthetic data pre-processing steps: Linear resampling to reduce matrix size; cardiac gating (take 1 cardiac cycle); Fourier transform to cartesian; gridding k-space (from cartesian to radial); undersampling; Inverse fourier transform; cropping (around heart); temporal interpolation (to 20 frames); normalisation (0 to 1).
- SSIM as loss function. 90% data for training 10% for validation. t-test compares SSIM across models (to check for improvement)
- Recreation of the Hauptmann model - Trained [[convolutional_neural_network]] for 350 epochs. [[Overview_of_CNN_model]].
- Improvements to the model: parameter optimisation ([[ML_learning_rate]], [[ML_loss_function]] (MSE or SSIM), [[ML_scales]], [[ML_residual]]); cropping (centre of image or heart); increase Field Of View; Sorted Golden Angle k-space trajectory; more loss functions (DSSIM, RDSSIM, 3DSSIM, *2DSSIM with TVMAE and MSE [[regularisation]]*)
- Optimised with this new loss function
- Trained with multiple orientations
- In-vivo study - Can reconstruct in the hospital in real time
- Exercise model - Augmented data with raised heart rate and translation (mimic diaphragm movement)
- Compared ML model with [[compressed_sensing]] (ML much better).

**Discussion**
- Improvement from - Novel loss function; sorted golden angle trajectory; augmentation (exercise model)
**Contributions**
- Work was integrated into the Siemens workflow

**What was the modelling approach you did for your MRes project (did you make the model, or did you adapt another one??)**



