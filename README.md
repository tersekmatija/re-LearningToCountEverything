# Reproducibility Challenge 2021: Learning to count everything
For the reproducibility challenge we tried to reproduce the paper from Ranjan et al. **Learning to count everything**. This is the repository, where you can find our final report (not yet available), authors code, and also our own scripts.

The structure of the repository is as follows: in folder **src** there is authors original code, together with two other folders -- **notebooks** and **data**. Notebooks folder includes 11 notebooks, which are self explanatory. In the data folder, you have to put density maps provided by the authors in gt_density_map_adaptive_384_VarV2. Density maps that are provided separately (not together with the images) must be put in gt_density_map_special. Images must be put in images_384_VarV2. These are the setting for FSC-147 data set provided by the authors of the original paper and can be accessed here: https://github.com/cvlab-stonybrook/LearningToCountEverything.

Please put instances_val_2014.json and instances_val_2017.json which can be found on [COCO data set website](https://cocodataset.org/#home) into **src/notebooks/misc** directory (only required for running COCO related notebook).

For this challenge we were running test_extended.py and notebooks. We also changed utils.py.