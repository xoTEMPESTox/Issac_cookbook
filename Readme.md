# Isaac Sim Cookbook

A personal, Python-based cookbook for working with Isaac Sim and the LeRobot ecosystem.

This repository acts as a hands-on reference for experimenting with:
- Simulation teleoperation
- Real-to-sim data collection
- Synthetic data generation (Gr00t style workflows)
- Policy fine-tuning and evaluation

The focus is not on building a single polished product, but on documenting repeatable workflows, gotchas, and minimal working setups while learning and experimenting with Physical AI pipelines.

---

## What This Repo Is (and Is Not)

**This is:**
- A practical sandbox for Isaac Sim + LeRobot
- A place to test teleoperation, data recording, and training loops
- A living cookbook with working commands and notes

**This is not:**
- A production-ready framework
- A fully abstracted library
- A replacement for official documentation

---

## Repository Structure (High Level)

```

.
├── phase_1_teleoperation/   # Real-to-sim control and data collection
├── phase_2_synthetic/       # Synthetic trajectory generation and augmentation
├── phase_3_training/        # Training and evaluation experiments
├── phase_4_deployment/      # Sim-to-real and inference tests
└── README.md

````

Each phase is intentionally kept simple and self-contained.

---

## Installation and Environment Setup

This setup closely follows the LeRobot + Isaac Sim workflow.

### References
- Installation guide: https://huggingface.co/docs/lerobot/en/installation
- Environment test: https://huggingface.co/docs/lerobot/en/envhub_leisaac

### Create Conda Environment

```bash
conda create -y -n lerobot python=3.10
conda activate lerobot
````

### System Dependencies

```bash
conda install ffmpeg -c conda-forge
```

```bash
sudo apt-get install cmake build-essential python3-dev pkg-config \
libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev \
libswscale-dev libswresample-dev libavfilter-dev
```

### Python Dependencies

```bash
pip install lerobot
```

#### Temporary evdev Build Fix

Some systems hit an evdev build error. Temporary workaround:

Source: [https://stackoverflow.com/questions/79727078/pip-failied-to-build-evdev](https://stackoverflow.com/questions/79727078/pip-failied-to-build-evdev)

```bash
export CC=/usr/bin/gcc
export CXX=/usr/bin/g++
pip install evdev
```

Then install full LeRobot extras:

```bash
pip install 'lerobot[all]'
```

---

## Notes

* Isaac Sim versions can be fragile. Expect occasional breakage.
* Treat this repo as a notebook with code, not a stable API.
* Each phase README documents assumptions and limitations explicitly.