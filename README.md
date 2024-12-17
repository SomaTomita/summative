# summative


# Table of Contents
1. [Environment Setup](#environment-setup)
2. [Database Configuration](#database-configuration)
3. [Saving Data to MongoDB](#saving-data-to-mongodb)
4. [Generating Outputs](#generating-outputs)

---

## 0. Environment Setup <a name="environment-setup"></a>
This project assumes you have **Anaconda** installed and are using **Jupyter Notebook**. Follow the steps below to set up the environment:

### Clone the Repository
Open your terminal and run the following commands:

```bash
git clone <repository_url>
cd <repository_name>
```

### Set Up the Python Environment
Run the notebook to set up the required packages and Python version:

```bash
jupyter notebook summative_exam/version-and-package_install.ipynb
```

### Start Jupyter Notebook
Launch the Jupyter Notebook environment from the root directory:

```bash
jupyter notebook
```

---

## 1. Database Configuration <a name="database-configuration"></a>
This project uses MongoDB to store and manage data. Follow the steps below to configure the database:

### Set Up MongoDB with Docker
Ensure Docker is installed and run the following command to start MongoDB:

```bash
docker-compose up -d
```

###  MongoDB Connection URL
Use the following URL to connect MongoDB in MongoDB Compass or verify in your code:
ex)
```bash
mongodb://root:mongo_password@localhost:27017/
```

### Test the Database Connection
Verify the connection to MongoDB using the test connection notebook:

```bash
jupyter notebook summative_exam/database/test_connection.ipynb
```

- Open **MongoDB Compass** and ensure the MongoDB URL matches the connection string in the notebook.

---

## 2. Saving Data to MongoDB <a name="saving-data-to-mongodb"></a>
This section involves saving the raw data and processed data into MongoDB:

### Save Raw Data
Run the following notebook to save the raw CSV data to MongoDB:

```bash
jupyter notebook summative_exam/src/data_save/save_to_mongodb.ipynb
```

### Process and Save Pivoted Data
Use the following notebook to preprocess the raw data and save pivoted datasets:

```bash
jupyter notebook summative_exam/src/data_save/merge_pivot_count.ipynb
```

---

## 3. Generating Outputs <a name="generating-outputs"></a>
Run the analytics notebook to generate statistics, graphs, and correlation outputs:

### Execute the Analytics Notebook
```bash
jupyter notebook summative_exam/src/output/main_analytics.ipynb
```

---
