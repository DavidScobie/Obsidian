[[MRI_Physics]]

Objective - Develop a model to simulate the BOLD haemodynamic response function:
Novelties - Our model was an expansion of the Balloon model which allowed for different field strengths (1.5T, 3T, 7T, 9.4T) and noise. We also expanded on the literature to include an arterial compartment in the BOLD HRF signal.

![[Pasted image 20250715152430.png]]
![[Pasted image 20250715152812.png]]
CMRO2 - cerebral metabolic rate of oxygen
Origin of T2* - T2* is a combined measure of T2 relaxation (transverse relaxation) and the effects of magnetic field inhomogeneities.

What did we measure and how?
- CBF - Using Arterial Spin Labelling (ASL)
- CBV - Vascular Space Occupancy (VASO)
- BOLD - BOLD fMRI
We estimated the r0 value at 9.4T and used this to simulate the model. 

We simulated noise in order to see how this effected the experimental data.
![[Pasted image 20250715155533.png]] std is the standard deviation in the noise as a percentage of signal change. At 1.5 T, 3 T and 7 T, the tSNR is roughly 20:1, 40:1 and 90:1
respectively. We extrapolated to find tSNR of 120:1 for 9.4T.

Data analysis steps of our MATLAB code:
![[Pasted image 20250715160116.png]]
- Drift? We pushed the MRI coils to their limit which heated them up. This led to a temporal drift downwards in the BOLD signal in some of the data. We corrected for this using the fourier transform over a large time window. This removed the drift harmonic.
- Discard outlying active voxels - This was done by clustering. We only deemed a voxel to be 'active' if at least one of its neighbours was also active.
- We used a venous mask (from the FLASH data, another MRI scan type) to deduce if an active pixel was of a vein or from tissue. - ![[Pasted image 20250715163618.png]]
here a) is the flash image and c) is the venous mask taken from a).

What data did we collect and how did we use it?
- We used the BOLD scanner data to identify active voxels (99.99th %ile). We used the FLASH scan to identify venous or tissue voxels. We then considered the 99.9th %ile to find active voxels in terms of CBF and CBV data (collected in the scanner).

**3D simulation??**
- We computed the correlation coefficient between each voxel of the scan data and the model
- Next we created a histogram of all the correlation coefficients for every voxel
- The 99.99th percentile was the cut-off threshold for identifying voxels that were ’active’ (only the 'active' voxels undergo the BOLD HRF).

![[Pasted image 20250715165452.png]]Different slices through the brain. The yellow crosses are the active voxels (correlating strongly with model, (undergoing a BOLD HRF)).

![[Pasted image 20250715165745.png]]
a) is the model BOLD HRF. c) is the experimental data.

Validation - We collected CBF and CBV experimental data, we plugged these into our model to see the predicted BOLD response. And we compared this to our BOLD HRF data.
![[Pasted image 20250715170043.png]]
