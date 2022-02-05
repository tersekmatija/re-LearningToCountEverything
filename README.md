# Reproducibility Challenge 2021: Learning to count everything
For the reproducibility challenge we tried to reproduce the paper from Ranjan et al. **Learning to count everything**. This is the repository, where you can find our final report (not yet available), authors code, and also our own scripts.

The structure of the repository is as follows: in folder **src** there is authors original code, together with two other folders -- **notebooks** and **data**. Notebooks folder includes 11 notebooks, which are self explanatory. In the data folder, you have to put density maps provided by the authors in gt_density_map_adaptive_384_VarV2. Density maps that are provided separately (not together with the images) must be put in gt_density_map_special. Images must be put in images_384_VarV2. These are the setting for FSC-147 data set provided by the authors of the original paper and can be accessed here: https://github.com/cvlab-stonybrook/LearningToCountEverything.

Please put instances_val_2014.json and instances_val_2017.json which can be found on [COCO data set website](https://cocodataset.org/#home) into **src/notebooks/misc** directory (only required for running COCO related notebook).

For this challenge we were running test_extended.py and notebooks. We also changed utils.py.

The majority of our experiments can be ran using script test_extended.py, which is only an extension of script test.py, produced by the authors of original paper. The instructions for running their script are described on their [repository](https://github.com/cvlab-stonybrook/LearningToCountEverything/blob/master/README.md). We added some command line parameters in order to evaluate FamNet in different test scenarios. The added parameteres are:
- o: the path to the output file, in which the results are written,
- al: if specified, the absolute loss is used in MinCountLoss instead of squared loss,
- ne: the number of exemplars that is used (for number of exemplars ablation study), set to -1 by default, meaning that all exemplars are used,
- c: if specified, FamNet is evaluated on CarPK test set,
- cc: if specified, FamNet is evaluated on JHU-CROWD++ test set.

To evaluate different values for $ \sigma_G $ in perturbation loss, we ran script choose_sigma.py and to find the instances, where adaptation brings biggest/worst improvements we ran script check_adapt.py. Both of these scripts are ran in the same way as original test.py and have the same command line parameters (except for parameter -a, which is removed in both scripts and -sp, which is removed in choose_sigma.py).
