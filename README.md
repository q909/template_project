# Cookiecutter Data Science

_A logical, reasonably standardized but flexible project structure for doing and sharing data science work._

**Cookiecutter Data Science (CCDS)** is a tool for setting up a data science project template that incorporates best practices. To learn more about CCDS's philosophy, visit the [project homepage](https://cookiecutter-data-science.drivendata.org/).

> ℹ️ Cookiecutter Data Science v2 has changed from v1. It now requires installing the new cookiecutter-data-science Python package, which extends the functionality of the [cookiecutter](https://cookiecutter.readthedocs.io/en/stable/README.html) templating utility. Use the provided `ccds` command-line program instead of `cookiecutter`.


To start a new project, create CONDA enviroment, cd to your folder and run in miniconda:

```bash
ccds https://github.com/q909/template_project
```



## Installation

Cookiecutter Data Science v2 requires Python 3.8+. Since this is a cross-project utility application, we recommend installing it with [pipx](https://pypa.github.io/pipx/). Installation command options:

```bash
# With pipx from PyPI (recommended)
pipx install cookiecutter-data-science

# With pip from PyPI
pip install cookiecutter-data-science

# With conda from conda-forge (coming soon)
# conda install cookiecutter-data-science -c conda-forge
```

## Starting a new project

1. Create ONENOTE notebook from template
2. Create MS Planner board
3. Create CONDA enviroment (CONDA)
4. Init PROJECTDIR from template (CCDS: ccds https://github.com/q909/template_project)
5. Init POETRY (poetry install in PROJECTDIR)
6. Init GIT (git init)
7. Connect GIT remote (git remote add origin)
8. Code, commit, enjoy!





### OneNote
    1. Open C:\Users\ValgaevO\OneDrive - AIT\Documents\OneNote Notebooks
    2. Double click on "template_notebook"
    3. Create new OneNote notebook from a template

### Microsoft Planner
    1. Create new ToDo plan
    
### Code
	1. Open CONDA prompt (miniconda)
	2. Create conda enviroments with any python versions required for the project 
		a. conda env list
		b. conda create  --name MYPROJECT-ENVIROMENT_py3-XX python==3.XX
		c. conda activate MYPROJECT-ENVIROMENT_py3-XX
	
	3. Run: cd C:\Users\ValgaevO\Lokal documents\01_code\01_ait-projects
	4. Initiate project with CCDS template: ccds https://github.com/q909/template_project
	5. Run: cd MY_PROJECT_DIR
	6. Create POETRY enviroment 
		a. Init poetry enviroment (MINICONDA in cd MY_PROJECT_DIR):  poetry install
		b. Add new required package to poetry toml: poetry add XXX
	7. Open VSCode
	8. Select MYPROJECT-ENVIROMENT_py3-XX CONDA enviroment in VSCode
	9. Open and run notebook
Copy .env file to the MY_PROJECT_DIR


### GIT
	1. Init GIT repo: 
		a. VSCode 
		b. git init (in PROJECTDIR)
	2. Create a remote repo online (GitHub or GitLab)
	3. Check .gitignore file
	4. Add GIT remote: git remote add origin https://github.com/q909/XXXXXXX or https://gitlab-intern.ait.ac.at/ValgaevO/XXXXXXXX
	5. Publish branch and sync with remote
	6. Get the changes from the remote: git pull origin master
	7. Commit: git commit -m "this is my first commit"
Push the commits to the GitLab project: git push origin master (or git push --force origin master)







### The resulting directory structure

The directory structure of your new project will look something like this (depending on the settings that you choose):

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         {{ cookiecutter.module_name }} and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── {{ cookiecutter.module_name }}   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes {{ cookiecutter.module_name }} a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations   
```

## Using v1

If you want to use the old v1 project template, you need to have either the cookiecutter-data-science package or cookiecutter package installed. Then, use either command-line program with the `-c v1` option:

```bash
ccds https://github.com/drivendataorg/cookiecutter-data-science -c v1
# or equivalently
cookiecutter https://github.com/drivendataorg/cookiecutter-data-science -c v1
```

## Contributing

We welcome contributions! [See the docs for guidelines](https://cookiecutter-data-science.drivendata.org/contributing/).

### Installing development requirements

```bash
pip install -r dev-requirements.txt
```

### Running the tests

```bash
pytest tests
```
