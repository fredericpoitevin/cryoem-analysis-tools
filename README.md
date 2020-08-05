# cryoem-analysis-tools

## How to contribute

### Add fred as a remote
Do this once if you do not see fred in the list when you do `git remote -v`:
```
git remote add fred https://github.com/fredericpoitevin/cryoem-analysis-tools
```

### Good practice
Every time you are about to do some work, first make sure you update your version with mine:
```
git pull fred master
```

## Prepare the environment 
There are two ways to prepare the environment on your system before using this package:

### First Approach
```
conda create -n cryotools python=3.8      #This line creates a new environment called "cryotools" and install Python 3.8
conda activate cryotools
conda install jupyter scikit-learn numpy matplotlib     #This line installs necessary packages
```
### Second Approach
First create the following `environment.yml` file:
```
name: cryotools
channels:
  - defaults
dependencies:
  - python=3.8
  - jupyter
  - scikit-learn
  - numpy
  - matplotlib
```
then create the environment from the text file with:
`conda env create -f environment.yml`.
