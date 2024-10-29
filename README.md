# 💻 Minor-Project

1. A desktop application
2. Upload image of backside of medicine blister packet (with label information printed)
3. Detailed information about medicine and it's consumption from reliable source
4. Medicine collection from Nepalese Authority 
---

# Table of Contents

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
   git clone https://github.com/yourusername/MLchemy.git
   cd MLchemy
   ```

   `Recommended`, Follow steps to use conda env:

   1. **Create a conda env**: 

      ```bash
      conda create -n <your_environment_name>
      ```

   2. **Install Ipykernel for using Jupyter Notebook**:

      ```bash
      conda install ipykernel
      ```

   3. **Connect new ipykernel to the conda env**:

      ```bash
      python -m ipykernel install --user --name <your_env_name> --display-name "<new_name_for_your_kernel"
      ```

2. **Install the required dependencies** (see [Requirements](#requirements)):

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Jupyter Notebooks**:

   Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```