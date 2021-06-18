Open Anaconda Prompt & create enviornment
create env
```bash
conda create -n winequality python=3.7 -y
```

Activate the env
```bash
conda activate winequality
```

Create requirements.txt & install it
```bash
pip install -r requirements.txt
```

Create template.py & mentioned the directory structure to create, run it
```bash
python template.py
```

Create .gitignore file

put winequality.csv file in the data_given folder. 

let initialise the git, files went untracked mode (U)
```bash
git init
```
Initialize the dvc & .dvcingnore file is created
```bash
git dvc
```
Add the winequality dataset into dvc, .dvc file is created
```bash
dvc add data_given\winequality.csv
```

Add all files into git , After that all files turned into Added mode (A)
```bash
git add .
```

Commit all the changes & then A mode clear , 
```bash
git commit -m "first commit"
```
.gitignore file is created automatically for winequality.csv files

let update REAME.md as it is modified
```bash
git add . && git commit -m "Update the README.md files"
```

Call Remote git remote directory & push the code

```bash
git remote add origin https://github.com/sainathpawar/MLOPS.git
git branch -M main
git push -u origin main
```

1. Create get_data.py file under src directory to get the data
2. Create load_data.py file to load the data with required preprocessing & save it under data\raw\winequality.csv
3. add staged into dvc.yaml file


Once program is done do the testing uisng pytest & tox
tox is providing virtual enviornmet for temporary testing

skipsdist = True is mentioned in tox.ini files becasue setup.py file is not there


To run the tox 
```bash
tox
```

To reload the virutal enviornment 
```bash
tox -r
```

To create python dsitribution to run on differnt machine
you can share the tar file with anyone
```bash
python setup.py sdist bdist
```

setup commands - This will use to create package for your program for ex. Numpy or Pandas
```bash
pip install -e .
```

Packages install in your prgram

```bash
pip freeze
```