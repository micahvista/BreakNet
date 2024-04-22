# BreakNet

A deep learning method to detect deletion from long reads alignment. It is
built with **Tensorflow** and **Python 3**.


## Installation

### Requirements
  * python 3.7, numpy, scipy, pandas, Matplotlib, TensorFlow 2.4, pysam

#### 1. Create a virtual environment

```bash
# create
conda create -n BreakNet python=3.6
# activate
conda activate BreakNet
# deactivate
conda deactivate
```

#### 2. clone BreakNet
- After creating and activating the BreakNet virtual environment, download BreakNet from github:
```bash
git clone https://github.com/micahvista/BreakNet.git
cd BreakNet
``` 
#### 3. Install

```bash
conda activate BreakNet
conda install numpy, scipy, pandas, Matplotlib, TensorFlow, pysam

``` 

## Tested data
The example data can be downloaded from 
#### HG002
https://ftp.ncbi.nih.gov/giab/ftp/data/AshkenazimTrio/HG002_NA24385_son/PacBio_MtSinai_NIST/Baylor_NGMLR_bam_GRCh37/HG002_PB_70x_RG_HP10XtrioRTG.bam
#### HG00514
http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/hgsv_sv_discovery/working/20160905_smithm_pacbio_aligns/HG00514_bwamem_GRCh38DH_CHS_20160905_pacbio.bam
#### HG00733
http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/hgsv_sv_discovery/working/20160905_smithm_pacbio_aligns/HG00733_bwamem_GRCh38DH_PUR_20160905_pacbio.bam
#### NA19240
http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/hgsv_sv_discovery/working/20160905_smithm_pacbio_aligns/NA19240_bwamem_GRCh38DH_YRI_20160905_pacbio.bam


## Usage



### Call deletion
In the folder "trained_weight", we give the trained weight files, which can directly used for calling deletions.

#### 1. Produce data for call sv
```bash
python breaknet.py data_mode bamfile_path data_folder

```

#### 2. Call deletion
```bash
python breaknet.py call_mode data_folder trained_weight_path bamfilepath
```

