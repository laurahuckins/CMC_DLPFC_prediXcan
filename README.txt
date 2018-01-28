In this folder are PrediXcan dbs for the CommonMindConsortium DLPFC samples.

Files are as follows:
DLPFC.cov.txt.gz  Covariances between rsids in each gene model. File required for MetaXcan
DLPFC_newMetax.db  DLPFC weight file. Compatible with PrediXcan and NEW MetaXcan code
DLPFC_oldMetax.db  DLPFC weight file. Compatible with PrediXcan and OLD MetaXcan code
DLPFC_update_corr  Correlations between snps in gene models
old	Previous incarnations of these models.

Suggested command line to run MetaXcan:

./MetaXcan.py --beta_folder /betas/$name.$Tissue --weight_db_path DLPFC_newMetax.db --covariance DLPFC.cov.txt.gz  --gwas_folder /sc/orga/projects/psychgen/pgc/Transcriptome/SCZ --gwas_file_pattern INPUTFILENAME --compressed --or_column OR 
	--pvalue_column P --snp_column SNP --a1_column A1 --a2_column A2 --se_column SE  --output_file OUTPUTFILENAME

Suggested code to run prediXcan:

./PrediXcan.py --predict --dosages path_to_dosages/ --dosages_prefix INPUTFILENAME --dosages_suffix dosage.gz --samples FAMFILE --weights DLPFC_newMetax.db --output_dir path_to_output --output_prefix OUTPUTFILENAME


Please contact laura.huckins@mssm.edu for more information if required.
