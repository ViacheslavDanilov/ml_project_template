# Data Science Cookie Cutter

## What is this?
This repository is a template for a data science or machine learning project. This is the project structure I frequently use for my data science project. 

## Tools used in this project
* [hydra](https://hydra.cc/): Manage configuration files - [article](https://towardsdatascience.com/introduction-to-hydra-cc-a-powerful-framework-to-configure-your-data-science-projects-ed65713a53c6)
* [pre-commit plugins](https://pre-commit.com/): Automate code reviewing formatting  - [article](https://towardsdatascience.com/4-pre-commit-plugins-to-automate-code-reviewing-and-formatting-in-python-c80c6d2e9f5?sk=2388804fb174d667ee5b680be22b8b1f)
* [DVC](https://dvc.org/): Data version control - [article](https://towardsdatascience.com/introduction-to-dvc-data-version-control-tool-for-machine-learning-projects-7cb49c229fe0)

## Project Structure
```bash
.
├── .dvc                      
│   └── config                      # DVC project-level config file
│
├── calculations                    # Computation files obtained in the project
│   
├── config                          # Hydra configuration
│   ├── main.yaml                   # Main configuration file
│   ├── model                       # Configurations for model training 
│   │   ├── model_1.yaml            # First set of parameters for training the model
│   │   └── model_2.yaml            # Second set of parameters for training the model
│   └── process                     # Configurations for processing data
│       ├── process_1.yaml          # First set of parameters for data processing
│       └── process_2.yaml          # Second set of parameters for data processing
│
├── data                            # Data of the project          
│   ├── final                       # The final, canonical data for modeling
│   ├── interim                     # Intermediate data that has been transformed
│   └── raw                         # The original, immutable data dump
│
├── dvc                             # Storage of DVC files  
│   ├── data                        # DVC files tracking data-related files and directories 
│   └── models                      # DVC files tracking model-related files and directories
│
├── models                          # Trained and serialized models, model predictions, or model summaries
│
├── notebooks                       # Jupyter Notebooks
│
├── src                             # Source code for use in the project
│   ├── __init__.py                 # Makes src a Python module
│   ├── data                        # Scripts for loading, generating, and processing data
│   │   └── process.py
│   ├── models                      # Scripts for training models and their subsequent use for making predictions                 
│   │   └── train_model.py
│   └── visualization               # Scripts for creating exploratory and results-oriented visualizations
│       └── visualize.py
│
├── tests                           # Source code for code testing
│    ├── __init__.py                 # Makes tests a Python module
│    ├── test_process.py             # Test functions for process.py
│    ├── test_train.py               # Test functions for train.py
│    └── test_visualize.py           # Test functions for visualize.py
│
├── .dvcignore                      # Files or directories that should be excluded when traversing a DVC project
├── .flake8                         # Configuration of flake8
├── .gitignore                      # List of ignored files that cannot commit to Git
├── .pre-commit-config.yaml         # Configuration file for pre-commit package
├── LICENSE                         # License file of the repository
├── pyproject.toml                  # Unified Python project settings file that replaces setup.py
├── README.md                       # The top-level readme file for developers using this project
└── requirements.txt                # The requirements file for reproducing the analysis environment

```

## How to use this project

Install Cookiecutter:
```bash
pip install cookiecutter
```

Create a project based on the template:
```bash
cookiecutter https://github.com/ViacheslavDanilov/ml-project-template.git
```
