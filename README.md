conda create --name dsdv0.5 python=3.8.5 -y
conda activate dsdv0.5

python setup.py


python run.py --enable_animation_mode --settings "./settings/animation_settings.json"
