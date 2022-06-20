## Input File
ViTA only uses multiple sequence alignment (protein sequences) in (aligned) FASTA (.afa or .fas) format. Any existing, published alignment tool can be used to produce the MSA, such as MAFFT or MUSCLE, as long as the aligned sequences are provided in (aligned) FASTA format. It is the user’s responsibility to manually check and fix for any misalignment. 
## Parameters 
### Sample Name
Name of the sequence to be analysed.
### Low support threshold	
The support is defined as the number of sequences at a given k-mer position that do not harbor a gap and/or an unknown/ ambiguous amino acid residue. Positions below a statistical support of 30 sequences (default) are defined as of low support. The user has the flexibility to set the threshold for low support.
### K-mer lenght
Select a *k-mer* window size that is appropriate for the analysis. While the minimum applicable size is 3, the maximum can equal to the alignment length of the uploaded input file. By default, a window size of nine (9; nonamer; 9-mer) is applied to evaluate the viral diversity with respect to cellular immune response. 

	
