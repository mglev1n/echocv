# echocv

Our echo computer vision pipelines has a several dependencies including:

1. opencv
2. tensorflow-gpu
3. trackpy
4. PIMS
5. numpy/scipy/pandas/scikit-learn
6. gdcm (Grassroots DICOM library)

We recommend using Anaconda, which has many of these installed, and allows ready installation of the remaining packages through conda or pip.

Our workflow takes as input a folder of DICOM format videos and performs the following

1. View classification:  using predict_viewclass.py
2. Segmentation: using segment_a4c_a2c_plax_psax.py
3. Phasing and assessment of disease probabilities (currently HCM and amyloid): using output_disease_prob_phased.py
4. Common 2D measurements including mass, volumes and ejection fraction using analyze_segmentations_unet_a4c_a2c_psax_plax.py
5. Global longitudinal strain: using compute_strain.py

Models are currently stored separately on Dropbox:  

https://www.dropbox.com/sh/0tkcf7e0ljgs0b8/AACBnNiXZ7PetYeCcvb-Z9MSa?dl=0

License details are provided in license.txt - and basically allow academic and non-profit use.