# How do I copy specific subject folders, sub-folders, or specific files to my scratch directory? 

### 1. Create a list of subjects of interest
Create a text file with one subject ID per line, for example:


Create a file to store subjects:
```bash
nano subjects.txt
```

Fill in your subjects (e.g.):
```bash
sub-BRS0001
sub-BRS0002
sub-BRS0003
```
Then save and close (Ctrl+x, y, Enter).

---
### 2. Create and run rsync scripts

Below are examples you can copy and modify depending on what you need.

#### **Option A – Copy entire subject folders**
```bash
while read subj; do
mkdir -p ~/scratch/BRS
rsync -axH --no-g --no-p --chmod=u=rw /project/ctb-rmcintos/data-sets/BRS/${subj} ~/scratch/BRS/
done < subjects.txt
```
This reads in subjects of interest from your subject list and copies each subject folder (including all sessions, sub-directories, and files) to `~/scratch/BRS`.


#### **Option B – Copy only a specific sub-folder for each subject (e.g., ses-1/eeg/)**
```bash
while read subj; do
mkdir -p ~/scratch/BRS/${subj}/ses-1
rsync -axH --no-g --no-p --chmod=u=rw /project/ctb-rmcintos/data-sets/BRS/${subj}/ses-1/eeg ~/scratch/BRS/${subj}/ses-1/
done < subjects.txt
```
This copies only the `/eeg` sub-folder for each subject.

