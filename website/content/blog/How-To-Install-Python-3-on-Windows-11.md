---
title: "How To Install Python 3 on Windows 11"
date: 2022-07-18T22:41:04-05:00
draft: false
author: "Abe"
tags:
    - Python
    - Pip
    - Windows 11
description: "How To Install Python 3 on Windows 11"
images:
    - "/images/install-tube-cast.png"

---
This article will walk through the steps to install python3 on Windows 11
in order to use the python package [tube-cast](https://github.com/abe-101/tube-cast).

## Use the Executable Installer

Head over to [python.org](https://python.org/download/windows/)
and download the latest version of python.

- ![python.org](/images/python-website.png)
    


## Launch the Executable Installer

When the download is finished, open up the Installer.  
Before installing Select the check box `Add Python 3.10 to PATH`.

- ![python Installer](/images/python-installer.png)

## Confirm Installation
To confirm the installation was successful open command prompt
and type 
```
python --version
```
you should see the version of python installed.  

- ![python Installer](/images/python-version.png)

## Pip
[Pip](https://pypi.org/project/pip/) is the package installer for Python. You can use pip to install packages from the Python Package Index and other indexes.  
We will use pip to install tube-cast.  
First check the version of pip 
```
pip --version
```
Upgrade to the latest version
```
python -m pip install --upgrade pip
```

- ![python Installer](/images/upgrade-pip.png)


## Install tube-cast
To install tube-cast run the command:
```
pip install tube-cast
```

- ![python Installer](/images/install-tube-cast.png)


## Start tube-casting 😉

Now tube-cast is ready to be used. For instructions type
```
tube-cast --help
```
when you use the tool you should see output like

- ![python Installer](/images/tube-cast-output.png)
