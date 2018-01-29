# CMC_DLPFC_prediXcan
CommonMind Dorso-lateral pre-frontal cortex prediXcan models

These models were created by Laura M. Huckins from CommonMind Consoritum (CMC) post-mortem Dorso-lateral pre-frontal cortex (DLPFC) data

PrediXcan codes used to build these models are available through https://github.com/hakyimlab/PrediXcan

Our manuscript describing creation of these models may be found on biorxiv: https://www.biorxiv.org/content/early/2017/11/21/222596
Please cite the latest version of this manuscript when using these models. 

These models may be used on raw genotype or summary-statistic data. 
For more information on the extension to summary statistics ("S-PrediXcan"), please see our manuscript:

-------

Files are as follows:
DLPFC.cov.txt.gz  Covariances between rsids in each gene model. File required for MetaXcan

DLPFC_newMetax.db  DLPFC weight file. Compatible with PrediXcan and NEW MetaXcan code

DLPFC_oldMetax.db  DLPFC weight file. Compatible with PrediXcan and OLD MetaXcan code

Suggested command line to run MetaXcan:

./MetaXcan.py --beta_folder /betas/$name.$Tissue --weight_db_path DLPFC_newMetax.db --covariance DLPFC.cov.txt.gz  --gwas_folder /sc/orga/projects/psychgen/pgc/Transcriptome/SCZ --gwas_file_pattern INPUTFILENAME --compressed --or_column OR 
	--pvalue_column P --snp_column SNP --a1_column A1 --a2_column A2 --se_column SE  --output_file OUTPUTFILENAME

Suggested code to run prediXcan:

./PrediXcan.py --predict --dosages path_to_dosages/ --dosages_prefix INPUTFILENAME --dosages_suffix dosage.gz --samples FAMFILE --weights DLPFC_newMetax.db --output_dir path_to_output --output_prefix OUTPUTFILENAME


Please contact laura.huckins@mssm.edu for more information if required.
