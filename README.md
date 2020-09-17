## README

This is a test to show if busco analysis results per chromosome when combined shows the same result as busco analysis results of the whole genome.

## Method

I took a genome containing chr1, chr2, chr3, chr4, chr5, chr6, chr7, scaf1, scaf2 and scaf3. These chromosomes were separated to individual file. Now I have one chromosome per file and one file containing all seven chromosomes.

Busco (v4.1.0) analysis of all files were done with exact same parameters. The results is shown below:

|Filename |  DB|       |    Mode  |  Completed |  SingleCopy | Duplicated | Fragmented | Missing |     Total|
|chr1.fasta |   fungi_odb10 | genome | 83(10.9%) |  83(10.9%) |  0(0.0%)  |   2(0.3%)  |   673(88.8%) |  758|
|chr2.fasta |  fungi_odb10 | genome | 208(27.4%) | 208(27.4%) | 0(0.0%) |    7(0.9%)  |   543(71.7%) |  758|
|chr3.fasta  |    fungi_odb10 | genome | 119(15.7%) | 119(15.7%) | 0(0.0%)  |   2(0.3%)  |   637(84.0%) |  758|
|chr4.fasta  |  fungi_odb10 | genome|  121(16.0%) | 121(16.0%) | 0(0.0%) |    5(0.7%)  |   632(83.3%) |  758|
|chr5.fasta  | fungi_odb10 | genome | 96(12.7%) |  96(12.7%) |  0(0.0%)  |   2(0.3%)  |   660(87.0%) |  758|
|chr6.fasta   |  fungi_odb10 | genome | 100(13.2%) | 100(13.2%) | 0(0.0%) |    5(0.7%)  |   653(86.1%) |  758|
|chr7.fasta   | fungi_odb10|  genome|  52(6.9%)  |  52(6.9%) |   0(0.0%) |    2(0.3%) |    704(92.8%) |  758|
|scaf1.fasta  |fungi_odb10 | genome|  0(0.0%) |    0(0.0%) |    0(0.0%) |    0(0.0%)  |   758(100.0%) | 758|
|scaf2.fasta  | fungi_odb10 | genome | 0(0.0%) |    0(0.0%) |    0(0.0%) |    0(0.0%) |    758(100.0%)|  758|
|scaf3.fasta  | fungi_odb10 | genome | 0(0.0%) |    0(0.0%) |    0(0.0%)|     0(0.0%)  |   758(100.0%) | 758|
|All_chromomes.fasta | fungi_odb10  genome  756(99.7%)  756(99.7%)  0(0.0%)     0(0.0%)  |   2(0.3%)  |    758|

The result above shows that the number of completed orthologous genes in each chromosome when combined shows the total of 779 (83+208+119+121+96+100+52). This is more than completed orthologous genes in all chromosomes analysed together showing just 756. The combined total of 779 is also greater than the total number 758 in the fungi_odb10.

## Result

The test is negative, meaning busco analysis per chromosome when combined is not same as in whole genome.
