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

## Genomic Feature Files
Genomic feature files for GRCh38, hg19, mm10, and mm9 can be found at [here](http://enhancer.sdsc.edu/yunjiang/resources/genomic_features/).

## Citation

If you use HiCNorm, please cite the following paper:

- Hu M, Deng K, Selvaraj S, Qin ZS, Ren B and Liu JS (2012) HiCNorm: removing biases in Hi-C data via Poisson regression. (2012) Bioinformatics 28 (23), 3131-3133.
