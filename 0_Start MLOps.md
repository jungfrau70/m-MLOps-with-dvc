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