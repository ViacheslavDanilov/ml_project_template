# Project structure

------------
```bash
.
├── .dvc                      
│   └── config                      # DVC project-level config file
│
├── .github                         # GitHub actions configuration directory
│   └── workflows                   
│       └── ci.yaml                 # Configuration file for continuous integration
│
├── configs                         # Hydra configuration
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
│
├── models                          # Trained and serialized models, model predictions, or model summaries
│
├── notebooks                       # Jupyter Notebooks
│
├── requirements                    # Directory containing various requirements files for replicating the analysis environment
│   ├── dev.txt                     # Requirements file for the development
│   └── tests.txt                   # Requirements file for testing and continuous integration
│
├── src                             # Source code for use in the project
│   ├── __init__.py                 # Make src a Python module
│   ├── data                        # Scripts for loading, generating, and processing data
│   │   └── __init__.py             # Make data a Python module
│   ├── models                      # Scripts for training models and their subsequent use for making predictions                 
│   │   └── __init__.py             # Make models a Python module
│   └── vis                         # Scripts for creating exploratory and results-oriented visualizations
│       └── __init__.py             # Make vis a Python module
│
├── tests                           # Source code for code testing
│    ├── __init__.py                # Make tests a Python module
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
└── README.md                       # The top-level readme file for developers using this project

```
