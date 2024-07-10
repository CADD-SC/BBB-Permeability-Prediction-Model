# Blood-Brain-Barrier-Permeability-Prediction-Model
Machine Learning-based prediction model for blood-brain barrier Permeability prediction of early stage drug screening

## Introduction: ## 

Welcome to our repository, here we provide machine learning model to efficiently predict the blood-brain barrier permeability of target drug compounds in early stage drug discovery process.

## Dependencies ##

- Python ≥ 3.9
- scikit-learn ≥ 1.26.4
- numpy == 11.5.0
- hpsklearn == 1.0.3
- hyperopt == 0.2.7
- xgboost == 2.0.3
- rdkit
- pandas

## Execution ##
**To run the prediction:**

```
$ python model.py --prediction --file_name [filename] --model_path BBB.pkl
```
Note: For the prediction step, prepare a .csv file containing SMILES without bioclass (e.g., test_set.csv)

**To run the validation:**

```
$ python model.py --validation --file_name [filename] --model_path BBB.pkl
```
Note: For the validation step, prepare a .csv file containing SMILES with bioclass (0 or 1) (e.g., valid_set.csv)

 
**Please ensure that all the necessary files (BBB.pkl, data_preprocessing.py, scaler, features.txt, inputfile.csv) are kept in the working directory.**
