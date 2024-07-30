# Bioactivity Prediction App
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
Run the Jupyter notebooks in root directory (steps 4a - 4c) to create a machine-learning model that predicts molecules' bioactivity against a specific gene.

Upon successfully running all code cells, a pickled model named after your gene will be generated. For example, running the notebook with the ADAMTS4 gene will produce a model file named ADAMTS4_model.pkl. You can find this file in the directory.

### Step 5: Launch the app
Launch the app with the PKL file in the root directory. Ensure you update the PKL file path at line 27 in app.py:

```
streamlit run app.py
```

### Step 6: Upload molecules list
Upload a list of molecules in a .txt file to test their bioactivity against your chosen gene. An example file, molecules_example.txt, can be found in the root directory.
