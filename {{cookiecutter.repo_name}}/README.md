# Project structure

------------
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
├── media                           # Media files used for README.md
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
