# Qiime2 Tutorial
##### If you have multiplex NGS amplicon sequencing data (e.g., 16S/18S/ITS/any functional genes) and you obtained all the sequencing files as two files (e.g., forward sequencing data as R1 and reverse sequence data as R2) from the sequencing facility. Then I hope this tutorial will help you to use qiime2 (version 2020.6).

 
### Step-1: Extract barcodes:
Note: This step is necessary for qiime2 for Demultiplexing. So far, the Qiime2 do not provide any command to extract barcode from the sequencing data. Therefore, we can still use Qiime1 (version 1.9.1) to generate a barcode file. To install qiime1 is a bit difficult process. But don't worry. You can follow this link: https://github.com/Sainur/qiime1 

> extract_barcodes.py \
-f /home/samad/Data/Christopher/P01-A01-SSO1_R1_clipped.fastq \
-r /home/samad/Data/Christopher/P01-A01-SSO1_R2_clipped.fastq \
-c barcode_paired_end \
--mapping_fp /home/samad/Data/Christopher/qiime1/mapping_SS01_202.txt \
--bc1_len 12 --bc2_len 12 \
-o /home/samad/Data/Christopher/qiime1/ 
