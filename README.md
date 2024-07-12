# Blood-Brain-Barrier-Permeablity-Prediction-Model
Machine learning-based prediction model for blood-brain barrier permeability prediction of early stage drug screening

## Introduction: ## 

Welcome to our repository, here we provide machine learning model to efficiently predict the blood-brain barrier (BBB) permeability of target drug compounds in early stage drug discovery process. BBB is a critical physiological barrier that protects the central nervous system (CNS) from potentially harmful substances while allowing essential nutrients to pass through. Accurate prediction of a compound's ability to cross the BBB is essential in the development of CNS-targeting drugs. 

## Classification criteria
The model uses a logBB threshold:

</strong>If <em>logBB</em> ≥ -1, the compound is <strong>BBB Permeable</strong> and belongs to class 1. If <em>logBB</em> < -1, it is <strong>Not BBB Permeable</strong> and belongs to class 0.</strong>



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
<strong>Note:</strong> For the prediction step, prepare a .csv file containing SMILES without bioclass (e.g., test_set.csv)

**To run the validation:**

```
$ python model.py --validation --file_name [filename] --model_path BBB.pkl
```
<strong>Note:</strong> For the validation step, prepare a .csv file containing SMILES with bioclass (0 or 1) (e.g., valid_set.csv)

**OutPut:**

Our model generates output in binary value (1 or 0), where 1 indicates compound to be permeable, while 0 indicates non-permeable
 
**Please ensure that all the necessary files (BBB.pkl, data_preprocessing.py, scaler, features.txt, input_file.csv, model.py) are kept in the working directory**
