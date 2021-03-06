# Master_diploma
Code for ChIP-seq peak intersections and motif finding
#Intersections of 2 bed files (genome intervals)

Intersection_bed_files.py - find overlapping regions in 2 bed files 
Sample files: bed_file1.bed, bed_file2.bed, bed_file_result.bed

#Find motifs using PWMs

PFM_to_PWM.py - converts frequency matrix into position weight matrix
find_motifs_in_fasta.py - find motif coordinates using PWM
find_motifs_in_fasta_optimized.py - the same as find_motifs_in_fasta.py, but works faster
Sample files: PFM.txt, PWM.txt, fasta_file_for_motif_search.fasta, motif_coordinates_results.txt
motif_coordinates_results.txt - column names: 1) seq_ID 2)sequence 3) motif sequence 4) motif_start (from 1st position in the sequence) 5) motif_end 6) motif_score 7) motif strand (regarding to sequence)

#Find threshold for PWMs (false positive rate)

FalsePostivieRateCount.py - create a table
threshold_plot.py - plot and calculation of threshold
Sample files: Araport11_201606_prot_cod_gene_promoters_1500_longest_UTR.fasta - promoter sequenses of all protein-coding genes in Arabidopsis thaliana, PWM.txt, threshold_results.txt, threshold_plot.png


#De novo motif search

Homer.txt - commands for Homer tool for using genome and random background (for more information, read Homer manual)

#Make a list of promoter coordinates (-1500; +longest UTR) from gff genome annotation
promoters_1500_UTR.R 
Sample files: Araport11_GFF3_genes_transposons.201606.gff, Araport11_201606_prot_cod_gene_promoters_1500_longest_UTR.bed


#Intersections of peaks with promoters
intersections_peaks_promoters.py

#Make fasta from bed
get_fasta_from_bed.py 
Sample file TAIR10_chr_1.fasta - trancated file as example, Araport11_201606_prot_cod_gene_promoters_1500_longest_UTR.bed, Araport11_201606_prot_cod_gene_promoters_1500_longest_UTR.fasta
