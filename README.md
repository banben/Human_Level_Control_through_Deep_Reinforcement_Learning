# 环境

原版的安装方式有些问题，修改了下，修改后的版本是`install_dependencies_mod.sh`，主要参考了下[Getting started with Torch](http://torch.ch/docs/getting-started.html)这篇文章。

但是要先安装torch

```
export PREFIX=$PWD/torch
echo "Installing Torch into: $PREFIX"

sudo apt-get update
sudo apt-get install -qqy build-essential
sudo apt-get install -qqy gcc g++
sudo apt-get install -qqy cmake
sudo apt-get install -qqy curl
sudo apt-get install -qqy libreadline-dev
sudo apt-get install -qqy git-core
sudo apt-get install -qqy libjpeg-dev
sudo apt-get install -qqy libpng-dev
sudo apt-get install -qqy ncurses-dev
sudo apt-get install -qqy imagemagick
sudo apt-get install -qqy unzip
sudo apt-get update

git clone https://github.com/torch/distro.git ~/torch --recursive
cd ~/torch; bash install-deps;
sudo chown -R ffq:ffq $PREFIX
./install.sh
source ~/.bashrc
```

然后再运行修改后的脚本

```
./install_dependencies_mod.sh
```

接着就是游戏的roms，这些roms在[Alfredvc/paac](https://github.com/Alfredvc/paac.git)上面可以找到

最后就是运行了

```
./run_cpu alien
```