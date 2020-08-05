# 2020 Challenge Dataset Curation Tools

This repository provides the scripts written for use in preparing the multicenter contextual dermoscopic image database for the SIIM-ISIC Melanoma Classification competition. The competition was hosted on Kaggle during the Summer of 2020 https://www.kaggle.com/c/siim-isic-melanoma-classification). The dataset is available for download at the DOI https://doi.org/10.34970/2020-ds01.

## Standardize Metadata

Each image in this dataset is attributed to one patient who of which is associated to multiple other images. Because the images that make up this data come from multiple centers, and because the associated identification metadata in each centers' internal image databases often are considered PHI, it was necessary to assign new patient and lesion identification codes in standard format, free of PHI, for the dataset.

[2020 Challenge assign Id_200408.py](https://github.com/ISIC-Research/2020-Challenge-Curation/blob/master/2020%20Challenge%20assign%20Id_200408.py) reads a csv containing filenames associated with pre-existing lesion IDs and patient IDs, and outputs 3 mapping tables (patient, lesion, and image) between original identification codes and a standardized format absent of PHI. Additional items can be added to the dataset without redundancy or double coding by specifying the existence of any of the three output tables. Duplicate patients, lesions, and images already present in the existing mapping tables are not assigned extra identification codes.





