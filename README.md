# GTDB2DIAMOND
Set of simple auxiliary python scripts to help create GTDB databases for annotation with DIAMOND

<br>
This collection of scripts is designed to facillitate DIAMOND annotations with GTDB representative protein sequences. 
It consists of 4 separate small scripts, that can be run in Spyder, or reused for other purposes.
Since DIAMOND varies in dependancies and requirements on different operating systems, automated diamond installation is not included,
and should be done following the descriptions in: https://github.com/bbuchfink/diamond/wiki 
<br><br>
Running a pipeline would consist of:<br>
-1. GTDB_protein_download.py: to download recent protein fasta files and taxonomy metadata<br>
-2. GTDB_protein_format.py: to include organism accession into headers of GTDB protein files <br>
-3. GTDB_protein_merge.py: merge renamed GTDB files into a single database<br>
-4. Construction of DIAMOND database from output of 3. (diamond --makedb, see: https://github.com/bbuchfink/diamond/wiki)<br>
-5. Annotation of proteins with DIAMOND database constructed in 4.  (diamond --blastp, see: https://github.com/bbuchfink/diamond/wiki)<br>
-6. GTDB_LCA.py: annotate taxonomy of query sequences based on lowest common ancestor, with top bitscore cutoff.<br>



#### Licensing

The pipeline is licensed with standard MIT-license. <br>
If you would like to use this pipeline in your research, please cite the following papers: 

[1] Kleikamp et al., 2022. Deep comparative metaproteomcis on the core AGS microbiome. (Mansucript in preparation, codes were developed and used within this project)
[2] Buchfink B, Reuter K, Drost HG, "Sensitive protein alignments at tree-of-life scale using DIAMOND", Nature Methods 18, 366–368 (2021). doi:10.1038/s41592-021-01101-x
<br>
[3] Parks, D.H., et al. 2020. A complete domain-to-species taxonomy for Bacteria and Archaea. Nature Biotechnology, https://doi.org/10.1038/s41587-020-0501-8.


#### Contact:
-Hugo Kleimamp (Developer): H.B.C.Kleikamp@tudelft.nl<br> 
-Martin Pabst: M.Pabst@tudelft.nl<br>


#### Recommended links to other repositories:
https://github.com/bbuchfink/diamond
https://gtdb.ecogenomic.org/downloads/
https://github.com/dutilh/CAT
