# model-management
Model management using MLFlow

# Prerequisite
1. Install mlflow on your local machine
2. Create an environment to install required python libraries for model development

    ```
    a. python -m venv env
    b. source env/bin/activate
    c. pip install -r requirements.txt
    ```

# Steps

Once the dependencies are installed and the environment is activated

**Run the MLFlow server**

```
mlflow server --backend-store-uri=sqlite:///mlflow_data/mlrunsdb.db --default-artifact-root=file:/Users/jaganlalthoppe/workspace/mlops/model-management/mlflow_data/mlruns
```

**Run the training code**
```
cd MLFlow_client\
python train.py
```

Open `http://127.0.0.1:5000/` on your browser, you should be able to see IRIS-V1 experiment from the list of Experiments