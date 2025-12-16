# Cookbook

This is a Python based cookbook for Le Issac , undertaking task like sim teloperation , Groot , Finetuning 


## Installation

guide : https://huggingface.co/docs/lerobot/en/installation

```
conda create -y -n lerobot python=3.10

conda activate lerobot

conda install ffmpeg -c conda-forge
```

```
sudo apt-get install cmake build-essential python3-dev pkg-config libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev libswscale-dev libswresample-dev libavfilter-dev
```

```
pip install lerobot
```

evdev bug requies temp fix [source](https://stackoverflow.com/questions/79727078/pip-failied-to-build-evdev)


```
export CC=/usr/bin/gcc
export CXX=/usr/bin/g++
pip install evdev
```

```
pip install 'lerobot[all]' 
```