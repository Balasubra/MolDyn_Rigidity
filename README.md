# MolDyn_Rigidity: 
## **Quantification of protein rigidness**
#### - Background
Molecular dynamics (MD) is widely used to characterise the dynamic behaviour of proteins, allowing the time-evolved conformational changes associated with protein function to be described. In this context, the root mean square deviation (RMSD) is a routinely used measure of the structural variability of a protein with respect to a reference conformation (e.g. the initial snapshot). However, the `standard RMSD (sRMSD) does not provide sufficient information to distinguish or quantify the contributions of static/rigid and mobile regions within the protein`. For this purpose, various methods for estimating the weighted RMSD (wRMSD) have been reported. These methods vary slightly in their mathematical formulation, but the general idea remains the same. The methods assign weights to atoms involved in the alignment to drive the fit based on segments that are relatively rigid (atoms with higher weights) between the two superimposed conformations. This excludes contributions from mobile segments in the fitting process. 
#### - Implementation
`A drawback of wRMSD, however, is that it requires an iterative fit` to achieve convergence, which may limit its application to large MD trajectories. To our knowledge, there is no readily available tool for estimating wRMSD on trajectories. The current repository provides a Jupyter notebook implementation of wRMSD estimation based on the popular MDAnalysis library. Briefly, the method uses a Gaussian weighting factor to assign weights to atoms, which are updated in each iteration. Details of the Gaussian weighted fitting formulation can be found [elsewhere](https://pubmed.ncbi.nlm.nih.gov/16565070/) 
#### - Protein Rigidness
Hereby we demonstrate wRMSD estimation and corresponding analysis with a sample trajectory provided by the MDAnalysis package to ensure reproducibility and, reusability for any system. A more detailed application of wRMSD, demonstrating its use in the quantification of protein rigidness, can be found in our recent articles.

- Quantification of protein rigidity with wRMSD 
   - Distinct dynamical features of plasmodial and human HSP70-HSP110 highlight the divergence in 
     their chaperone-assisted protein folding (https://doi.org/10.1016/j.bbapap.2023.140942)
     
- Application of wRMSD 
   - Conformational response to ligand binding of TMPRSS2, a protease involved in SARS-CoV-2 
     infection: Insights through computational modeling (https://pubmed.ncbi.nlm.nih.gov/37409524/)

#### Packages & their Versions 
- matplotlib: 3.9.1
- nglview   : 3.1.1
- numpy     : 1.26.3
- pandas    : 2.1.4
- MDAnalysis: 2.7.0
- MDAnalysistests : 2.7.0
- seaborn   : 0.13.1
