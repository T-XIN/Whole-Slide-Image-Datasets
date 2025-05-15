
# Whole Slide Image Datasets

This repository aims to guide you through the process of finding, downloading, and using public medical images for your projects. Whether you're a researcher, developer, or enthusiast, this guide will help you get started with medical image datasets.

## Introduction

Medical images are crucial for various applications, including research, diagnostics, and machine learning. Publicly available medical image datasets provide a valuable resource for developing and testing algorithms. In this guide, we'll explore where to find these datasets, how to download them, and how to use them in your projects.

## NO.1 TCGA (The Cancer Genome Atlas)

1. **Where to Find**: Visit [National Cancer Institute GDC Data Portal Homepage](https://portal.gdc.cancer.gov/).

2. **Download Command**: `gdc-client download -m manifest name.txt`. Make sure data selected are diagnostic WSIs (saved in .svs format).

3. **Understand the Label**:
	- **Patient ID** is the first 12 characters of the slide name, e.g. TCGA-50-5066
	- **Case ID** is the first 15 characters of the slide name, e.g. TCGA-50-5066-01 or TCGA-50-5066-02
	- **Slide name**, e.g. TCGA-50-5066-01Z-00-DX1.e161df31-84a4-40a4-a6a2-748b60820f77 contains the slide name TCGA-50-5066-01Z-00-DX1 and some uid e161df31-84a4-40a4-a6a2-748b60820f77; all slide names in the downloaded dataset are unique and so are the uid’s so that there is a one-to-one mapping between the slide names and the uid’s.
	- **UUID** Extract UUID from folder name (assuming folder name is the UUID).

4. **TCGA-NSCLC (lung)**
	- **TCGA-LUAD** (lung adenocarcinoma): 541 diagnostic slides
	- **TCGA-LUSC** (lung squamous cell carcinoma): 512 diagnostic slides
5. **TCGA-RCC  (Rental Cell carcinoma)**
	- **TCGA-KIRC** (Kidney Renal Clear Cell Carcinoma): 519 diagnostic slides
	- **TCGA-KIRP** (Kidney Renal Papillary Cell Carcinoma): 300 diagnostic slides
	- **TCGA-KICH** (Kidney Chromophobe): 121 diagnostic slides
