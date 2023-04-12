# Cookiecutter template for an ML, DS or AI project 

## What is this?
This repository represents a logical, reasonably standardized, but flexible project structure for doing and sharing data science work.

#### [Cookiecutter homepage](http://drivendata.github.io/cookiecutter-data-science/)

## Tools used in this project

-----------
* [hydra](https://hydra.cc/): Manage configuration files([article on Medium](https://towardsdatascience.com/introduction-to-hydra-cc-a-powerful-framework-to-configure-your-data-science-projects-ed65713a53c6))
* [pre-commit](https://pre-commit.com/): Automate code reviewing formatting ([article on Medium](https://towardsdatascience.com/4-pre-commit-plugins-to-automate-code-reviewing-and-formatting-in-python-c80c6d2e9f5?sk=2388804fb174d667ee5b680be22b8b1f))
* [DVC](https://dvc.org/): Data version control ([article on Medium](https://towardsdatascience.com/introduction-to-dvc-data-version-control-tool-for-machine-learning-projects-7cb49c229fe0))


## Requirements to use the cookiecutter template:

-----------
 - Python 2.7 or 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
pip install cookiecutter
```

or

``` bash
conda config --add channels conda-forge
conda install cookiecutter
```


## To start a new project, run:

------------
``` bash
cookiecutter https://github.com/ViacheslavDanilov/ml-project-template
```


## The resulting directory structure

------------
```bash
.
├── .dvc                      
│   └── config                      # DVC project-level config file
│   
├── config                          # Hydra configuration
│   ├── main.yaml                   # Main configuration file
│   ├── data.yaml                   # Data processing configurations
│   └── model.yaml                  # Model training and testing configurations
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
├── media                           # Media files used for README.md

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
│    ├── __init__.py                # Makes tests a Python module
│    ├── test_process.py            # Test functions for process.py
│    ├── test_train.py              # Test functions for train.py
│    └── test_visualize.py          # Test functions for visualize.py
│
├── .dvcignore                      # Files or directories that should be excluded when traversing a DVC project
├── .gitignore                      # List of ignored files that cannot commit to Git
├── .pre-commit-config.yaml         # Configuration file for pre-commit package
├── create_env.sh                   # Shell script to create conda environment
├── LICENSE                         # License file of the repository
├── pyproject.toml                  # Unified Python project settings file that replaces setup.py
├── README.md                       # The top-level readme file for developers using this project
└── requirements.txt                # The requirements file for reproducing the analysis environment

```
