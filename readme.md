## MLFlow Tracking Demo

Demos Covered:

1. Manual Logging for ML Model
2. Automated logging with DL Model
3. Storing logs to MDB file instead of file directory

[MLFlow Tutorials](https://mlflow.org/docs/latest/tutorials-and-examples/index.html)

step 1:
```commandline
conda create --prefix ./env python=3.7 -y
```
step 2:
```
conda activate ./env
```
or
```commandline
source activate ./env
```
step 3:
```commandline
 pip install -r requirements.txt
```
step 4:

Run LinearRegressionModel.py multiple time with different choice of alpha and l1ratio

step 5:

Observe that there is new folder created with name mlruns which has details of each run recorded in sub directory named 0.

step 6:

visualize the runs info in mlflow dashboard
```commandline
mlflow ui
```
same happens when we run the LogisticRegressionModel.py file

step 7:

NeuralNetworkModel.py has auto log feature enabled, hence it will log the params, metrics and models with out specifying to log manually in code.

step 8:

change the log storage from file system to mdb file
```commandline
mlflow server \
--backend-store-uri sqlite:///mlflow.db \
--default-artifact-root ./artifacts \
--host 127.0.0.1 -p 5000
```
