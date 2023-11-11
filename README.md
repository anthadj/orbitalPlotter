# orbitalPlotter
This project consists of two parts. First, a bash script that takes information about atomic and molecular orbitals from .molden files and stores them in a .csv file format. 
Secondly, a mathematica script that inputs information from the .csv file to plot the orbital in question.

# Directory content:
src:
- moldenscriptAtom.sh 
- moldenscriptMolecule.sh
- ijkVals (directory)
- construct_wavefunction.nb

inputs:  
- h_1.molden
- c_222.molden
- ch4_22222.molden

The src folder: 
Contains the two bash scripts "moldenscriptAtom.sh" and "moldenscriptMolecule.sh".
These two scripts are responsible for reading .molden files and rewriting the data in .csv format.
The first one is for atomic data and the second for molecular. 
The ijkVals directory should be left alone. It contains data used from the two .sh scripts
The construct_wavefunction.nb is a mathematica script that reads the .csv files and prints 
the molecular orbitals.

The inputs folder:
Contains three example .molden files, two atomic cases (h_1 and c_222) and one molecular (ch4_22222).
The numbers represent electrons in orbitals. Hydrogen only has 1 electron, whule Carbon has 6 electrons
in 3 different orbitals. Methane (ch4) has 10 electrons in 10 orbitals. In here, place any .molden files 
you wish to analyse

# How to run the script:
For atoms:
Let's assume you wish to plot the first orbital of a carbon atom. Run the following command from withtin the src folder
"zsh moldenscriptAtom.sh ../inputs/h_1.molden"
This will create the file "h_1.molden.csv" in the inputs folder. 


For molecules:
Let's assume you wish to plot the first orbital of a methane molecule. Run the following command from withtin the src folder
"zsh moldenscriptMolecule.sh ../inputs/ch4_22222.molden"
This will create the file "ch4_22222.molden.csv" in the inputs folder. 


