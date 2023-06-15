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

mlflow server --backend-store-uri=sqlite:///mlflow-data/mlrunsdb.db --default-artifact-root=file:mlflow-data/mlruns
mlflow server --backend-store-uri=sqlite:///mlflow_data/mlrunsdb.db --default-artifact-root=file:/Users/jaganlalthoppe/workspace/mlops/model-management/mlflow_data/mlruns
aimlflow sync --mlflow-tracking-uri=sqlite:///mlflow_data/mlrunsdb.db --aim-repo=./mlflow_data
aim up --repo=../mlflow_data/


"mssql+pyodbc://<UserName>:<Password>@<ServerName>.database.windows.net:1433/<DatabaseName>?driver=ODBC+Driver+17+for+SQL+Server"
“mssql+pyodbc://<iacoe_dlops>:<S33PgtPD40@123>@<pepiacoe1d.database.windows.net>.database.windows.net:1433/<duaas>?driver=ODBC+Driver+17+for+SQL+Server”

mlflow server --backend-store-uri "mssql+pyodbc://iacoe_dlops:S33PgtPD40@123@pepiacoe1d.database.windows.net.database.windows.net:1433/duaas?driver=ODBC+Driver+17+for+SQL+Server" --default-artifact-root "wasbs:/<container>@<StorageAccount>.blob.core.windows.net" --host 0.0.0.0

ENV MLFLOW_SERVER_DEFAULT_ARTIFACT_ROOT "wasbs:/<container>@<StorageAccount>.blob.core.windows.net"


mlflow server --backend-store-uri "mssql+pyodbc://iacoe_dlops:S33PgtPD40@123@pepiacoe1d.database.windows.net/duaas?driver=ODBC+Driver+17+for+SQL+Server" --default-artifact-root "wasbs://mlflowserver@labelrightarabicuat.blob.core.windows.net/" --host 0.0.0.0


server = 'pepiacoe1d.database.windows.net'
database = 'duaas'
username = 'iacoe_dlops'
password = 'S33PgtPD40@123'
sql_driver="{ODBC Driver 17 for SQL Server}"

C:\>sqlcmd -S pepiacoe1d.database.windows.net -d duaas -U iacoe_dlops -P S33PgtPD40@123 -I