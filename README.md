# omicR_linux
omicR creates fasta files, downloads genomes from NCBI using the refseq number, creates databases to run BLAST+, runs BLAST+ and filters these results to obtain the best match per sequence.  These scripts can be used to run BLAST alignment of short-read (DArTseq data) and long-read sequences (Illumina, PacBio… etc). You can use reference genomes from NCBI, or any other genetic sequence that you would like to use as reference. 

Introduction

omicR creates fasta files, downloads genomes from NCBI using the refseq number, creates databases to run BLAST+, runs BLAST+ and filters these results to obtain the best match per sequence. 

These scripts can be used to run BLAST alignment of short-read (DArTseq data) and long-read sequences (Illumina, PacBio… etc). You can use reference genomes from NCBI, genomes from your private collection, contigs, scaffolds or any other genetic sequence that you would like to use as reference. 

Requirements

•	NCBI BLAST+ V4 or latest. (https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/)

•	Python V3 or latest (https://www.python.org/downloads/) 

•	Biopython (https://biopython.org/) 

•	omicR 

Add these programs to your environment path variables.

Introduction
If you are running omicR with an HPC computer, it likely that you know how to use a command line. For this purpose, I suggest that you only use 2 scripts to “create fasta files” and “filter”. As the steps of downloading, creating a database and running BLAST can take longer than running BLAST+ directly. 
The required input BLAST command line to run this filtering script is:

blastn -db [ ] -query [ ] -out [ ] -word_size [ ] -perc_identity [ ] -num_threads [ ] -outfmt ' 6 qseqid sacc stitle qseq sseq nident mismatch pident length evalue bitscore qstart qend sstart send gapopen gaps qlen slen’
