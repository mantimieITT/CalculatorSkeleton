TBD
# This file will have every command needed to get everything running.

# Required Extensions installed on local windows VSC
# CMake Tools
# C/C++ Extension Pack
# C++ Intellisense
# C++ TestMate
# Remote - WSL

# Install required packages on WSL to compile C++ code
```
sudo apt-get -y update
sudo apt-get install -y build-essential gdb cmake
```

#--- If you get an error on version of CMake use the following to update the CMake version. Reference https://apt.kitware.com/

Version 18.04 Ubuntu WSL run the following commands...
```
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates gnupg software-properties-common wget
wget -O - https://apt.kitware.com/keys/kitware-archive-latest.asc 2>/dev/null | gpg --dearmor - | sudo tee /etc/apt/trusted.gpg.d/kitware.gpg >/dev/null
sudo apt remove --purge --auto-remove cmake
sudo apt-add-repository 'deb https://apt.kitware.com/ubuntu/ bionic main'
sudo apt-get update
sudo apt-get install kitware-archive-keyring
sudo rm /etc/apt/trusted.gpg.d/kitware.gpg
sudo apt-get install -y cmake
```
----#

# Command Line build
# at root directory run...
```
cmake .
make
```

# navigate to bin and the binary should be there.
```
cd bin
./Calculator
```

# Run Unit tests.
```
cd test
./calculator_test
```

