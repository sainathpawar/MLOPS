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

Add all files into git
```bash
git add .
```