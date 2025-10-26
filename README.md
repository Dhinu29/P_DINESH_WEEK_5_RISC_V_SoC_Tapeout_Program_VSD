# P_DINESH_WEEK_5_RISC_V_SoC_Tapeout_Program_VSD

# 🧾 OpenROAD Installation Report

# 📘 1. Introduction

OpenROAD (Open Routing, Optimization, and Analysis for Designs) is an open-source physical design toolchain that automates the digital ASIC design flow.
This week’s objective was to install and configure OpenROAD on a Linux system (Ubuntu 22.04 / WSL2).

# 🎯 2. Objective

- To install OpenROAD successfully on Ubuntu.

- To verify the installation through sample design runs.

- To document issues, dependencies, and resolutions.

 # 🧩 4. Installation Steps
```
#steps followed:

sudo apt install -y libgtest-dev cmake build-essential
sudo apt install libspdlog-dev
sudo apt install -y liblemon-dev

git clone https://github.com/google/or-tools.git
cd or-tools
mkdir build && cd build
cmake -DBUILD_DEPS=ON -DCMAKE_BUILD_TYPE=Release ..
make -j$(nproc)
sudo make install

git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD.git
cd OpenROAD/
sudo ./etc/DependencyInstaller.sh -base
mkdir build
cd build
cmake ..

```
