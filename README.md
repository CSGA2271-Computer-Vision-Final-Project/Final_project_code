#  Final Project of Computer Vision：A Comparative Study of Deep Learning Models for Brain Tumor Segmentation

Brain ICV segmentation from multi-modal MRI is a complicated task in medical
image analysis that enables accurate diagnosis and treatment planning for patients
with brain disease. Manual segmentation of brain regions (grey matter, white
matter, CSF) is time-consuming even with expert knowledge and skills. In this
project, we evaluate and compare multiple deep learning architectures for automatic
brain tumor segmentation using the BraTS 2024 dataset, which contains four MRI
modalities (T1, T1CE, T2, and FLAIR) with expert-annotated tumor masks. This
research assesses the performance of several models including UNet, ResUNet,
NNUnet, SwinUNetR, Transformer-based Segmentation Models, SegFormer, NonSegmentation-Oriented Architectures, and conditional diffusion models (CMDiff)
under constrained computational resources. Our experiment’s results demonstrate
that UNet with skull stripping preprocessing, z-score normalization within the
brain mask, and a combined loss function of Cross Entropy and Dice Loss achieves
the best performance with a Dice coefficient of 0.7505, precision of 0.9306, and
sensitivity of 0.8708. We identify that distinguishing background from brain tissue
and penalizing models from trivially predicting all pixels as background are critical
factors for achieving robust segmentation. Our findings provide practical insights
for researchers working with limited data and computational resources in medical
image segmentation tasks.

## Files
The best model file contains two notebooks corresponding to the best model trained from scratch and best model with pretrain weight. Other models we experimented are included in the file of other model

## Downloading BraTS 2024 Data (Synapse)

BraTS 2024 challenge data is hosted on **Synapse** under the BraTS 2024 Challenge project.

### 0) Prerequisites (Synapse access)
1. Create a Synapse account and make sure your account has a valid email attached.
2. Register for the BraTS challenge (registration is required before some access steps).
3. Request/obtain data access:
   - If the data is released post-challenge, you may need to **agree to post-challenge Terms & Conditions** and click **Request Access** on the data page.
   - If you are instructed to use the **BraTS Data Access form**, fill it out and accept the email invitation to the data-access team. :contentReference

If you still cannot download after those steps, check the Synapse discussion “Data Access” thread for common fixes (email spam folder, username mismatch, etc.).

### 1) Where the BraTS 2024 files live on Synapse

- BraTS 2024 Challenge (main project): `syn53708249`
- Data hub page (contains links to datasets/tasks): `syn64952546`
- Example task (Adult Glioma / GLI container): `syn59059776`

#### BraTS 2024 GLI (example) direct file IDs
- **Training zip:** `syn60086071` (BraTS2024-BraTS-GLI-TrainingData.zip)
- **Validation zip:** `syn61455507` (BraTS2024-BraTS-GLI-ValidationData.zip)
- **Citations file:** `syn59808905` (CITATIONS.bib)

### 2) Download option A: Synapse web UI
1. Log into Synapse.
2. Open each Synapse ID page (e.g., `syn60086071`) and use the **Download** button (or add to your download cart, if applicable).
3. Unzip the downloaded archives into your local data directory.

### 3) Download option B: Command line

#### Install tools
```bash
python -m pip install --upgrade synapseclient
