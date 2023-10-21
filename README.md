## END to END Machine Learning

### Create virtual Environment
```
conda create -p HouseP_P python==3.8
```

- -p --> Current Directory

### Actiavte virtual environment
    conda activate HouseP_P/

### Now create a README.md file and add all the project information here

- Now create a `requirements.txt` file where all the library can be written 

### Install all necessary libraries

```
pip install -r requirements.txt
```
### Create a `setup.py` file
- If I want to convert this project into packages then at that time this file will be used.
```
Steps:

Step2
setup(
    name='RegressiorProject',
    version='0.0.1',
    author='Narsingh Maurya',
    author_email='narsingh2231@gmail.com',
    install_requires=['numpy','pandas','matplotlib'],
    packages=find_packages()

)

```

#### ====================================

`-e .` ---> Whenever `requirements.txt` file have this notation this trigger the `setup.py`
to get install all the packages.

### to ignore `-e.` in `setup.py`
```
#step1:
HYPHEN_E_DOT = '-e .'

#step2: we add a condition in get_requirements function
if HYPHEN_E_DOT in requirements:
    requirements.remove(HYPHEN_E_DOT)           
```

### My setup is ready and can be installed as package
```
pip install -r requirements.txt
```
- It will install as a package in the same folder 

### If you want to install this separately from `setup.py` file then bellow code can be used.
```
python setup.py install
``` 

## 2.

### Always craete a folder called as `src`
 - Create a file `__init__.py`
 - To stablish a connections beween the folders so that any piece of code can be used by just importing it.

### create a folder called as `Notebooks`
- To perform EDA and research work or feature engineering
- and do not wanted to have this folder in the packages


### Create some file in In `src` folder
- `logger.py` to write a logging logic
- `exceptpion.py` for exception handling etc.
- `utils.py` to write any generic functionality which can be used in this entire project like database connections, reading mysql or anything such kind of functions.


### Create  `components` folder inside `src` folder
- To create a training pipeline and prediction pipeline there will be different components will be developed here.
- after creating this folder create a     ```__init__.py``` file in this folder to connect this folder with the module.

- create a python file ```data_ingestion.py```
- create a python file ```data_transformation.py```
- create a python file ```model_trainer.py```
- If project is bigger then make a model_evaluation file also otherwise write your code in trainer itself.

### Create a `pipeline` folder in `src`
- after creating this folder create a     ```__init__.py``` file in this folder to connect this folder with the module.

- create a python file here as ```training_pipeline.py```

### Create a file `.gitignore` in main folder

- from your git repo, copy any gitignore python format and paste in this file which is just been created and save it.

- add your venv name into thin file in environment section. and save.

### Push your file and folder structure to git repo.
- create a git repo or use exsting one
- in cmd:
    - git init
    - git add .
    - git status
    - git 