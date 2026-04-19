from datetime import datetime
from airflow import DAG
from airflow.operators.python import PythonOperator

def hello():
    print("Hello Airflow 🚀")

with DAG(
    dag_id="simple_hello_dag",
    start_date=datetime(2024, 1, 1),
    schedule="@daily",
    catchup=False,
) as dag:

    task1 = PythonOperator(
        task_id="say_hello",
        python_callable=hello
    )
