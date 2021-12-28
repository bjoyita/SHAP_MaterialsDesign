# SHAP_MaterialsDesign
The code "SHAP_PF_kappa_Github(1).ipynb" uses Pymatgen, Matminer, Scikit-learn, and SHAP libraries to highlight the contribution of features (descriptors) on the targets, namely power factor (PF) and thermal conductivity (kappa) measured at room temperature, of 204 inorganic thermoelectric materials listed in the csv file Pf_kappa_RT_1.csv. This dataset is a subset of the dataset used in https://github.com/ngs00/DopNet/tree/main/dataset derived from http://www.mrl.ucsb.edu:8080/datamine/thermoelectric.jsp.

To run the code, one needs to install two open-source python-based materials packages - Pymatgen and Matminer along with the SHAP library. 

To install Pymatgen and Matminer, you will require python > 3.7 and pip. Run the following to install Pymatgen and Matminer: pip install Pymatgen; pip install matminer (follow the sequence).

The code uses "composition" featurizers from Pymatgen and Matminer to extract elements and their atomic fractions from the compound formula given in the dataset. To learn more about the libraries, visit https://hackingmaterials.lbl.gov/matminer, https://pymatgen.org.

I have chosen  random forest algorithm to train the dataset. Please note that this dataset consists of two targets – PF and kappa which are trained individually. These are the parameters that have a direct influence on the performance of thermoelectric materials. 

To find out the contribution of each element on the targets, SHAP has been employed. Refer to https://shap-lrjball.readthedocs.io/en/latest/ for details about SHAP. Shapley value originated from the concept of game theory and was first introduced by L.S Shapley (Shapley, Lloyd S. “A value for n-person games.” Contributions to the Theory of Games 2.28 (1953): 307-317).
