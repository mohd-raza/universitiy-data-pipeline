## End to End Data Engineering project using Apache Airflow and AWS Crawler, AWS Glue, and Amazon Athena

In this project, I built an ETL pipeline using Apache Airflow. The result was stored in a Sqlite database. After that, I uploaded the data to AWS S3 and used Amazon Athena to run queries on the CSV file by adding a Crawler. There were two DAGs in this project. The first one fetched data from an API and sent it to Sqlite. Once the data was sent to Sqlite, a trigger mechanism activated DAG 2. DAG 2 then retrieved data from Sqlite and uploaded it to an S3 bucket as a CSV file.

#### DAG 1: get_university_api_send_sqlite
![image](https://github.com/mohd-raza/universitiy-data-pipeline/assets/91888013/c0004682-a10e-43af-9718-43d422c44f61)


#### DAG 2: get_sqlite_data_send_s3
![image](https://github.com/mohd-raza/universitiy-data-pipeline/assets/91888013/f0ef8632-4cbf-4b77-b0db-b0111bb6c07b)

