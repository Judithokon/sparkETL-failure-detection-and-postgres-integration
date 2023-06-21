# SparkETL-failure detection and postgres integration

The SparkETL-Failure Detection and Postgres Integration project is a data pipeline built using Apache Spark. Its purpose is to collect data from multiple CSV files, combine relevant columns from each dataset into a single dataset, and add a new column called "failure status" to indicate any failures that occurred during the data processing stages of the pipeline then load the final dataset into postgres database.

### Project Overview
The ETL (Extract, Transform, Load) process implemented in this project allows efficient handling of large volumes of data through the distributed processing capabilities of Apache Spark. It supports various datasets from different sources and ensures that only the necessary columns are selected and merged together.

One key feature of this project is the inclusion of the "pipeline status" column, which dynamically generates values based on predefined conditions. This column automatically determines whether a failure has occurred during the execution of the ETL process. Each row in the resulting dataset is assigned a value of 1 or 0 in the "pipeline status" column, indicating the presence or absence of a pipeline failure, respectively.

Once the data has been successfully integrated and the "failure status" column has been added, the resulting dataset is loaded into a Postgres database. This step ensures secure storage and facilitates further analysis, reporting, and decision-making based on the processed data.

### How to Use
To use this project, follow the steps below:

1. Clone the repository: `git clone https://github.com/Judithokon/sparkETL-failure-detection-and-postgres-integration.git`
2. Ensure you have Apache Spark and a Postgres database installed and properly configured.
3. Place your CSV files in the appropriate directory or update the file paths in the code accordingly.
4. Modify the column merging logic to suit your specific requirements, if necessary.
5. Set the predefined conditions for failure detection in the pipeline status column.
6. Run the project's main script or execute the necessary Spark jobs according to your project structure.
7. Verify that the pipeline successfully completes the ETL process and adds the "failure status" column to the resulting dataset.
8. Connect to your Postgres database and create the required table schema.
9. Load the processed dataset into the Postgres database for secure storage and further analysis.

### Additional Notes
- Ensure that you have sufficient computational resources to handle the size of the datasets being processed.
- It is recommended to test the project on a small subset of data before scaling it up to the full dataset.
- Customize the project as needed, considering specific data requirements, transformations, and failure conditions.

### Contributors
- [Judith](https://github.com/Judithokon) - Project Lead

### License
This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code as per the terms of the license.

### Acknowledgments
- [Apache Spark](https://spark.apache.org/) - Powerful distributed computing framework
- [PostgreSQL](https://www.postgresql.org/) - Open-source relational database management system
