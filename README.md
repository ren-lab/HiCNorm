# HiCNorm
Scripts to run HiCNorm  

## Usage

Rscript HiCNorm.R [options]

Options:
	
	-i INPUT, --input=INPUT
		raw HiC matrix

	-o OUTPUT, --output=OUTPUT
		normalized HiC matrix

	-f GENOMIC_FEATURE, --genomic_feature=GENOMIC_FEATURE
		genomic feature file

	-c COV, --cov=COV
		minimun coverage [default 1]

	-l LEN, --len=LEN
		minimun fragment length [default 0.1]

	-s GC, --gc=GC
		minimum gc content [default 0.3]

	-m MAP, --map=MAP
		minimum mappability [default 0.8]

	-n, --negative_binomial
		use negative binomial regression

	-h, --help
		Show this help message and exit

## Input and Output Format

Input matrix file contains four columns: chromosome, first bin, second bin, and raw counts. 
Input genomic feature files contain six columns: chromosome, bin start position, bin end position, fragment length, GC content, and mappbility.
Output matrix file cotains four columns: chromosome, first bin, second bin, and normalized counts. 

## Example

A demo data of chrmosome 19 form mESC HindIII HiC data is in the data folder. The data is from Fraser, J. et al. Molecular Systems Biology (2015).

```
Rscript HiCNorm.R -i data/mESC.HindIII.raw.chr19.txt -o data/mESC.HindIII.HiCNorm.chr19.txt -f data/F_GC_M_Hind3_50Kb_el.chr19.txt
```

## Genomic Feature Files
Genomic feature files for GRCh38, hg19, mm10, and mm9 can be found at [here](http://enhancer.sdsc.edu/yunjiang/resources/genomic_features/).

## Citation

If you use HiCNorm, please cite the following paper:

- Hu M, Deng K, Selvaraj S, Qin ZS, Ren B and Liu JS (2012) HiCNorm: removing biases in Hi-C data via Poisson regression. (2012) Bioinformatics 28 (23), 3131-3133.

## Contact

For any questions or comments, please contact Ming Hu(afhuming@gmail.com) or Yunjiang Qiu(yuq003@ucsd.edu).
