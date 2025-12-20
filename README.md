#  Final Project of Computer Vision：A Comparative Study of Deep Learning Models for Brain Tumor Segmentation

## Downloading BraTS 2024 Data (Synapse)

BraTS 2024 challenge data is hosted on **Synapse** under the BraTS 2024 Challenge project (**syn53708249**). :contentReference[oaicite:0]{index=0}

### 0) Prerequisites (Synapse access)
1. Create a Synapse account and make sure your account has a valid email attached.
2. Register for the BraTS challenge (registration is required before some access steps).
3. Request/obtain data access:
   - If the data is released post-challenge, you may need to **agree to post-challenge Terms & Conditions** and click **Request Access** on the data page. :contentReference[oaicite:1]{index=1}
   - If you are instructed to use the **BraTS Data Access form**, fill it out and accept the email invitation to the data-access team. :contentReference[oaicite:2]{index=2}

If you still cannot download after those steps, check the Synapse discussion “Data Access” thread for common fixes (email spam folder, username mismatch, etc.). :contentReference[oaicite:3]{index=3}

### 1) Where the BraTS 2024 files live on Synapse

- BraTS 2024 Challenge (main project): `syn53708249` :contentReference[oaicite:4]{index=4}
- Data hub page (contains links to datasets/tasks): `syn64952546` :contentReference[oaicite:5]{index=5}
- Example task (Adult Glioma / GLI container): `syn59059776` :contentReference[oaicite:6]{index=6}

#### BraTS 2024 GLI (example) direct file IDs
- **Training zip:** `syn60086071` (BraTS2024-BraTS-GLI-TrainingData.zip) :contentReference[oaicite:7]{index=7}
- **Validation zip:** `syn61455507` (BraTS2024-BraTS-GLI-ValidationData.zip) :contentReference[oaicite:8]{index=8}
- **Citations file:** `syn59808905` (CITATIONS.bib) :contentReference[oaicite:9]{index=9}

> Note: In BraTS, ground-truth labels are provided for training, while validation typically comes without GT labels; test data is hidden/not publicly downloadable. :contentReference[oaicite:10]{index=10}

### 2) Download option A: Synapse web UI
1. Log into Synapse.
2. Open each Synapse ID page (e.g., `syn60086071`) and use the **Download** button (or add to your download cart, if applicable).
3. Unzip the downloaded archives into your local data directory.

### 3) Download option B: Command line (recommended)

#### Install tools
```bash
python -m pip install --upgrade synapseclient
