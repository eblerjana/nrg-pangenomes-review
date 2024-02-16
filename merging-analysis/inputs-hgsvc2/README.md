# HGSVC2 input data


## Merged VCF

merged PAV (freeze 4) calls downloaded from: http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/HGSVC2/release/v2.0/integrated_callset/    
There are separate files for SNVs, indels and SVs:
* variants_freeze4_indel_insdel_alt.vcf.gz
* variants_freeze4_snv_snv_alt.vcf.gz
* variants_freeze4_sv_insdel_alt.vcf.gz

They were combined into a single VCF using `` bcftools concat ``:   

```bat
bcftools concat -a variants_freeze4_snv_snv_alt.vcf.gz variants_freeze4_indel_insdel_alt.vcf.gz variants_freeze4_sv_insdel_alt.vcf.gz | bgzip > variants_freeze4.vcf.gz
```

## Single sample VCFs

single sample VCFs downloaded from: http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/HGSVC2/working/20210806_PAV_VCF/


## Callable regions BEDs

callable region BED files are obtained from Globus endpoint: JAX HGSVC2, path: /sv/pav/hg38/results/<SAMPLE>/callable/


## Reference genome

GRCh38 reference genome downloaded from: http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/HGSVC2/technical/reference/20200513_hg38_NoALT/hg38.no_alt.fa.gz

