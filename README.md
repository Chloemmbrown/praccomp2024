Praccomp README
Chloe Brown
Reduced Sexual Dimorphism in Threespine Stickleback

first observe the raw data using FastQC
determine where/what needs to be trimmed
use trimmomatic-0.39 to remove sequences that are unsuitable 
all sequences after reads below 20 are removed

Script for trimmomatic 
 nohup java -jar ~/praccomp2024/Trimmomatic-0.39/trimmomatic-0.39.jar PE ../00_raw_reads_fastq/BALAKRISHNAN_5270_181121A6/5270-S10_S10_L001_R1_001.fastq.gz ../00_raw_reads_fastq/BALAKRISHNAN_5270_181121A6/5270-S10_S10_L001_R2_001.fastq.gz CB2output_forward_paired.fastq.gz CB2output_forward_unpaired.fastq.gz CB2output_reverse_paired.fastq.gz CB2output_reverse_unpaired.fastq.gz ILLUMINACLIP:../02_adapter_files/S10_adapters.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:20 MINLEN:36
##note for above line nohup allows for continued processing when computer turns off and back on 

Use FastQC to analyze new trimmed reads to ensure they are now valid sequnces all above 20


