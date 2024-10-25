Data and scripts required to generate the plots for:

**Active learning driven prioritisation of compounds from on-demand
libraries targeting the SARS-CoV-2 main protease**, by Ben Cree,
Mateusz Bieniek, Siddique Amin, Akane Kawamura and Daniel Cole.

Please see the [preprint](https://doi.org/10.26434/chemrxiv-2024-xczfb)
for further details.


### Reproducing plots in the paper:

Install the environment via:

```
mamba create --name fegrow_al_data python=3.11 jupyter rdkit numpy==1.24.4 scikit-learn umap-learn seaborn chemplot -c conda-forge -c anaconda
conda activate fegrow_al_data
pip install useful_rdkit_utils==0.2.7
```

To run the jupyter notebook:

```
python -m ipykernel install --user --name=fegrow_al_data
jupyter notebook
```

and open the notebook file `plots.ipynb`.

### Description of data:

The file `cs_49k.csv` contains the SMILES and predicted affinity of the oracle dataset. 

The folders `rep_*` contain five replicas of active learning hyperparameter tuning. For each experiment, folders contain SMILES and predicted affinity of compounds selected at each active learning cycle.

The same information is provided for the four prospective runs in the folders `mpro-*`, for the four different objective functions used.
