# 💻 Medicine-Label-OCR-NER

- A desktop application.
- Upload image of backside of medicine blister packet (with label information printed).
- Detailed information about medicine and it's consumption from reliable source.
- Medicine collection from Nepalese Authority.
---

## 📋 Table of Contents

- [Minor Project](#-minor-project)
- [Requirements](#️-requirements)
- [Screenshots](#-snapshots)
- [How to Use](#-how-to-use)

---

## 🛠️ Requirements

- Tkinter
- PaddleOCR
- SpaCy
- MySQL
- OpenCV
- Pillow
- Matplotlib

```bash
pip install -r requirements.txt
```

---

## 📷 Snapshots

| ![Image 1](./GUI/screenshots/home.png) | ![Image 2](./GUI/screenshots/result.png) |
|:--------------------------------:|:--------------------------------:|

---

## 👉 How to Use

To run the notebooks locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/xaxm007/Minor-Project.git
   cd Minor-Project
   ```

2. **Install the required dependencies**:

   ***Create a conda env***: 

   ```bash
   conda create -n <your-environment-name>
   ```

   ```bash
   pip install -r requirements.txt
   ```

   ***or create conda environment `medsys` using [environment.yml](environment.yml) file.***

   ```bash
   conda env create -f environment.yml
   ```
3. **Setup MySQL database**:

   1. Install MySQL Server on your local machine and start the server.

   2. Open MySQL with `--local-infile` enabled:

      ```bash
      mysql --local-infile=1 -u <your-username> -p
      ```

   3. Create Database and Load CSV file:

      ```bash
      CREATE DATABASE  <your-database-name>;
      ```

      ```bash
      USE <your-database-name>;
      ```

      ```bash
      CREATE TABLE <your-table-name> (
         ID INT PRIMARY KEY,
         DRUG_NAME TEXT,
         DOSAGE_FORM_AND_STRENGTH LONGTEXT,
         INDICATIONS LONGTEXT,
         CONTRAINDICATIONS_OR_PRECAUTIONS LONGTEXT,
         DOSAGE_SCHEDULE LONGTEXT,
         ADVERSE_EFFECTS LONGTEXT,
         DRUG_AND_FOOD_INTERACTIONS LONGTEXT
      );
      ```

      ```bash
      SHOW tables;
      ```

      ```bash
      DESCRIBE <your-table-name>;
      ```

      ```bash
      LOAD DATA LOCAL INFILE '/path/to/data.csv'
      INTO TABLE med_info
      FIELDS TERMINATED BY ','
      ENCLOSED BY '"'
      LINES TERMINATED BY '\n'
      IGNORE 1 ROWS;
      ```
   
      ***or create database `medicine` and table `med-info` using [setup.sql](./Database/sql/setup.sql) file.***

      ***Note: adjust the CSV file path if necessary***

      ```bash
      cd Database/sql
      source setup_db.sql;
      ```

      ***or create same database as the actual implementation using [database_copy.sql](./Database/sql/database_copy.sql) file.***

      ```bash
      cd Database/sql
      source database_copy.sql
      ```
   

4. **Run Python Script**:

   ```bash
   cd GUI/tkinter-app
   ```

   ***Note: Fill your `username` and `password` in line `181` in app.py to run the app.***

   ```bash
   conda activate <your-environment-name>
   python app.py
   ```
---
## 📎 Citation:

If you use our code or our dataset please cite us.

```bash
@software{Medicine Label Extraction and Analysis,
author = {Pokharel, A.K and  Maharjan, Saksham},
month = {10},
title = {{Medicine Label NER}},
url = {https://github.com/ayyp1/Medicine-Label-analysis-NER},
version = {1.0.5},
year = {2023}
```
---
