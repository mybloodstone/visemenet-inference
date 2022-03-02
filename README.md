# visemenet-inference
- Inference Demo Code of ["VisemeNet-tensorflow"](https://github.com/yzhou359/VisemeNet_tensorflow)
    * The repo is outdated and difficult to setup the environment for testing of the pretrained model

## How to freeze graph
- The code does not need bazel-build for "freeze-graph" function
- Refers to https://github.com/lighttransport/VisemeNet-infer

### Requirements
* Python 3.6.x using ["pyenv"](https://github.com/pyenv/pyenv)
* Tensorflow 1.1.0

1. Setup the envs and packages
```shell
# Install Virtualenv using pyenv
pyenv install 3.6.5
pyenv virtualenv 3.6.5 visemenet-freeze
pyenv activate visemenet-freeze
```
```shell
# Install packages
pip install tensorflow==1.1.0
```

2. Clone the repo
```shell
# Clone Visemenet repo and the pretrained model
git clone https://github.com/yzhou359/VisemeNet_tensorflow.git
curl -L https://www.dropbox.com/sh/7nbqgwv0zz8pbk9/AAAghy76GVYDLqPKdANcyDuba?dl=0 > pretrained_model.zip
unzip prtrained_model.zip -d VisemeNet_tensorflow/data/ckpt/pretrain_biwi/
```

3. Freeze Graph and Save as pb
```shell
# Freeze Graph
python freeze_graph.py
```

