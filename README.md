## Bioactivity Prediction App
This project is an adaptation of Data Professor's bioinformatics tutorial. This tutorial predicts the bioactivity of any molecule to any gene. This tutorial focuses on the ADAMTS4 gene which is responsible for aggrecan degradation in a human model of OA [link](https://pubmed.ncbi.nlm.nih.gov/21815191/). 

## Reproducing this Web App
To recreate this web app on your own computer, follow these steps:

### Step 1: Create a Conda Environment
First, create a Conda environment called bioactivity:
```
conda create -n bioactivity python=3.7.9
```
### Step 2: Next, activate the bioactivity environment:
```
conda activate bioactivity
```
### Step 3: Install prerequisite libraries
```
pip install -r requirements.txt
```

### Step 4: Generating the PKL file for specific gene
Run jupyter notebooks (4a - 4c)  to create a machine learning model that predicts molecules' bioactivity against a certain gene of choice. 

Upon successfully running all code cells, a pickled model named after your gene will be generated. For example, running the notebook with the ADAMTS4 gene will produce a model file named ADAMTS4_model.pkl. You can find this file in directory. 

###  Launch the app
Launch the app with pkl file in the root directory. Change pkl file at line 27 on app.py. 

```
streamlit run app.py
```

### Upload a list of molecules to check their bioactivity towards your picked gene
