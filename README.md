# iGEM Modelling
Repository containing various iterations of the Spi-thon model designed to model spider silk protein expression in E. coli with differential gene expression of various helper proteins. This model is designed identify the effect on translation rate of alanine-rich spider silk MaSp proteins of co-expression of 3 key genes: alanine import channel protein CycA; alanine tRNA and the enzyme catalysing the binding of alanine to its corresponding tRNA alanyl-tRNA synthetase. The model identified that MaSp production is elevated by alanine tRNA overexpression, but is maximised by co-expression of all 3 genes. 

The various iterations of this model seek to identify the difference in MaSp production rate over time in E. coli with co-expression of 1 or more of the aforementioned genes. Later versions of the model account for protein and mRNA degradation, as well as tRNA degradation triggered by amino acid starvation. The model breaks down the relevant biological process into 4 steps: 
1) Alanine import - Alanine is taken up through CycA as well as through other already present porins and via passive processes)
2) Aminoacylation - Binding of alanine to the corresponding tRNA, catalysed by alanyl-tRNA synthetase; alanine/tRNA availability or synthetase activity can be rate-limiting for this step
3) Transcription + translation - Coupled transcription (and translation for proteins) using up all alanyl-tRNA (which is assumed to be maintained at a negligible concentration in highly metabolically active E. coli cells)
4) Degradation - First order degradation of mRNA and proteins (as well as tRNA in the case of alanine availability being rate-limiting for aminoacylation, amounting to amino acid starvation conditions)

The set of differential equations underpinning the model is given in a LaTeX pdf. All key parameters are lifted directly or estimated from the literature or calculated using pre-existing tools (such as DLKcat, an ML tool for estimation of Kcat values for a given enzyme-ligand pair). Full details of the model are available at https://2022.igem.wiki/exeter/model
