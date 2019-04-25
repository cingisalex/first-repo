This repo introduces some first simple steps in the *version control system git*. However, before I start, I would like to recomend the following link:
```
https://medium.com/@QuantumBlack/data-scientists-the-only-useful-code-is-production-code-8b4806f2fe75
```
and the corresponding template repository:
```
https://github.com/thuijskens/production-tools
```
The excelent repository and article were created by *QuantumBlack*.

### -----to short user manual-----
**1st Scenario**:
Clone this repo to your local machine and swich to the dev branch and initiate a new branch.
```
$git clone https://github.com/cingisalex/first-repo.git 
$git checkout dev 
$git checkout -b dev_newfeature #initiate new branch from dev branch
```

**2nd Scenario**:
I assume you work on the *dev* branch and you create or make changes in a script file1.py. After sucessfull changes, you want to commit those changes and push it from your local machine to the remote repository.
```
[MAKE YOUR OWN CHANGES IN THE SCRIPTS]
$git add file1.py *.ipynb file3.pdf (PLEASE DON'T USE "add *")
$git commit -m "PLEASE INSERT MEANINGFUL COMMIT MESSAGE"
$git push
```
**3rd Scenario**: *new PO-request*
Creating from the *dev* a new branch *dev_newfeature*. And merging the new branch back to *dev* 
```
$git checkout dev
$git checkout -b dev_newfeature #initiate new branch from dev branch
[MAKE YOUR OWN CHANGES IN THE SCRIPTS]
$git add file1.py *.ipynb file3.pdf (PLEASE DON'T USE "add *")
$git commit -m "PLEASE INSERT MEANINGFUL COMMIT MESSAGE"
$git push
[...Once we are ready to include the new features to our dev...]
$git checkout dev
$git merge dev_newfeature
$git branch -D dev_newfeature [OPTIONAL]
```
