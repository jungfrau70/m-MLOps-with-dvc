export WORKDIR='/root/PySpark/workspace/9_MLOps'
cd $WORKDIR


conda env create -f environment.yml
conda activate mlops
pip install -r requirements.txt

git init
dvc init

create step_01.py
create step_02.py
create dvc.yaml

dvc repro

git add . && git commit -m "My first commit"
git remote add origin https://github.com/jungfrau70/mlops.git
git push origin master
