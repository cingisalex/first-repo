This repo introduces some first simple steps in the *version control system git*. However, before I start, I would like to recommend the following [link](https://medium.com/@QuantumBlack/data-scientists-the-only-useful-code-is-production-code-8b4806f2fe75):
```
https://medium.com/@QuantumBlack/data-scientists-the-only-useful-code-is-production-code-8b4806f2fe75
```
and its corresponding template [repository](https://github.com/thuijskens/production-tools):
```
https://github.com/thuijskens/production-tools
```
The repository and article were created by *QuantumBlack*.

### -----to short user manual-----
**1st Scenario**:
We clone this repo to our local machine and create a dev branch. Afterwards, we swicht to the dev branch and initiate a new branch.
```
$git clone https://github.com/cingisalex/first-repo.git 
$git checkout -b dev
$git checkout dev 
$git checkout -b dev_newfeature #initiate new branch from dev branch
```

**2nd Scenario**:
Important: we can not switch immediatelly from a *master* branch to *dev_newfeature* branch, we firstly have to switch to *dev* and then to *dev_newfeature*. So, we work on the *dev_newfeature* branch and created or made changes in a script file1.py. After successful changes, we want to commit those changes and push it from our local machine to the remote repository.
```
[MAKE YOUR OWN CHANGES IN THE SCRIPTS]
$git checkout dev 
$git checkout dev_newfeature
$git add file1.py *.ipynb file3.pdf (PLEASE DON'T USE "add *")
$git commit -m "PLEASE INSERT MEANINGFUL COMMIT MESSAGE"
$git push
```
**3rd Scenario**: *merge*
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
$git branch -D dev_newfeature [OPTIONAL, this deletes the branch]
```
