# GA-ACE
Codes of GA-ACE accompanying the paper "Bidirectional Action-Dependent Q-learning with Global Average Credit Assignment". The GA-ACE algorithm facilitates a more timely and rational distribution of reward among the agents, enabling them to adjust their strategies promptly in the appropriate direction.

## Installation

### All scripts

The scripts from installation to execution are all here.

```
# install starcraft
conda create -n ace python=3.8
wget https://blzdistsc2-a.akamaihd.net/Linux/SC2.4.10.zip
unzip SC2.4.10.zip
export SC2PATH="StarCraftII"
pip install pysc2 protobuf==3.19.5

# install grf
apt-get update && apt-get install git cmake build-essential libgl1-mesa-dev libsdl2-dev \
    libsdl2-image-dev libsdl2-ttf-dev libsdl2-gfx-dev libboost-all-dev \
    libdirectfb-dev libst-dev mesa-utils xvfb x11vnc -y \
    && apt clean \
    && rm -rf /var/cache/apt/*
python3 -m pip install --upgrade pip setuptools psutil wheel
git clone https://github.com/google-research/football.git
```

### Install environment

#### Installing StarCraft II

##### Linux

Please download the Linux version of [StarCraft II](https://blzdistsc2-a.akamaihd.net/Linux/SC2.4.10.zip) from the Blizzard's repository and make sure the downloaded version of SC2 is 4.10.

##### Windows

Please install StarCraft II from [Battle.net](https://battle.net/).  You may need to set the `SC2PATH` environment variable.

#### Installing Google Research Football

Following the settings in CDS, we also make a reasonable change to the two half-court offensive scenarios: we will lose if our players or the ball returns to our half-court. For users who installed grf using the pip install method, maps can be modified using the following command,

```bash
pip install gfootball
```

For users who wants to install GRF from sources using GitHub repository, please refer to [GRF](https://github.com/google-research/football). Then users can modify the maps directly in the GRF repository.
