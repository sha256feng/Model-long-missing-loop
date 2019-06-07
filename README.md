# Model-long-missing-loop
This repository contains code and examples to model multiple missing loops in tetrameric protein.

Modeller script is mainly based on following link: https://salilab.org/modeller/wiki/Missing%20residues 

	- Execute the loop modeling for each chain. Mutate the "A" letters in `two-alignment.ali` to "B"/"C"/"D" letters. And run them in separate folder, because the output PDB files have the same names. Later I visually checked each chain's modeling result and `cat` them together.
	List of output files as example:


	- Loop modeling results: loops forming a knot -- need to fix 
  Two segments have knotted structure of peptides. In order to prepare a cleaner version where there is no such problem, I use CHARMM script to solve this bad penetration issues. The program requires feeding of PSF and CRD files. So I generated PSF and CRD file firstly by CHARMM-GUI's PDBReader. Later I used following script to rotate the loops and did some minimization to avoid clash and bad angles.
