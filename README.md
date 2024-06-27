# TFCRs
find TFCRs

1.Peak to fasta (.fa)
 bedtools getfasta -fi ./hg19/hg19.fa -bed ./peaks.bed -fo ./2_peak.fa/peaks.bed.fa

2.Fimo scans the genome sequence to obtain the sequence position corresponding to motif
./meme-5.1.1/src/fimo --oc ./3_scan --thresh 1e-5 --no-qvalue ./cisbp.human.motif.txt 
./2_peak.fa/peaks.bed.fa

3.tsv To txt
 R run tsv_to_txt.R

4.Run perl d-motif_combine-TFfamily.pl

5.Run perl e-tfpos_combine.pl
 
6.Run perl f1-tf_bed-new-c.pl
 
7.Run perl f2-delete-overlap.pl
 
