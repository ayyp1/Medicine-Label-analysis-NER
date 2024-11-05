# 💻 Minor-Project

1. A desktop application.
2. Upload image of backside of medicine blister packet (with label information printed).
3. Detailed information about medicine and it's consumption from reliable source.
4. Medicine collection from Nepalese Authority.
---

# 📋 Table of Contents

- [Minor Project](#-minor-project)
- [Requirements](#️-requirements)
- [How to Use](#-how-to-use)
---

# 🛠️ Requirements

- Tkinter
- PaddleOCR
- SpaCy
- MySQL
- OpenCV
- Pillow
- Matplotlib
- JSON
- TQDM

```bash
pip install -r requirements.txt
```

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
   conda create -n <your_environment_name>
   ```

   ```bash
   pip install -r requirements.txt
   ```

   ***or create conda environment `medsys` using [environment.yml](environment.yml) file***

   ```bash
   conda env create -f environment.yml
   ```
3. **Setup MySQL database**:

   1. Install MySQL Server on your local machine.

   2. Create Database:

      ```bash
      mysql --local-infile=1 -u <your-username> -p
      ```

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

   3. Load csv files:

      ```bash
      LOAD DATA LOCAL INFILE '/path/to/file.csv'
      INTO TABLE med_info
      FIELDS TERMINATED BY ','
      ENCLOSED BY '"'
      LINES TERMINATED BY '\n'
      IGNORE 1 ROWS;
      ```