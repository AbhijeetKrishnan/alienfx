
AlienFX is a Linux utility to control the lighting effects of your Alienware computer.
============

At present there is a CLI version (``alienfx``) and a gtk GUI version (``alienfx-gtk``). And 
has been tested on Debian/Ubuntu/Kali, Fedora and Arch Linux.

[![Version](https://img.shields.io/badge/version-2.1.1-red.svg)]() [![GitHub license](https://img.shields.io/github/license/trackmastersteve/alienfx.svg)](https://github.com/trackmastersteve/alienfx/blob/master/LICENSE) [![Python3](https://img.shields.io/badge/python-3.6-green.svg)]() [![GitHub issues](https://img.shields.io/github/issues/trackmastersteve/alienfx.svg)](https://github.com/trackmastersteve/alienfx/issues) [![GitHub stars](https://img.shields.io/github/stars/trackmastersteve/alienfx.svg)](https://github.com/trackmastersteve/alienfx/stargazers)  [![GitHub forks](https://img.shields.io/github/forks/trackmastersteve/alienfx.svg)](https://github.com/trackmastersteve/alienfx/network) 

## Table of Contents

- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Dependencies

AlienFX is written in python and has been tested on ``python 2.7`` and ``python 3.6``. It requires
the following python packages to run:

1. pyusb >= 1.0.0b1.
   Note that your distribution may only provide ``the pre-1.0`` version of ``pyusb``. If
   this is the case, you can install ``pyusb 1.0`` using the 
   following command:
      ```sh
      $ pip install --pre pyusb
      ```

2. pkg_resources.
   You can install ``pkg_resources`` using the following command:
      ```sh
      $ pip install setuptools
      ```

3. cairo.
   You can install ``cairo`` using the following command:
   
   On Debian/Ubuntu/Kali:
      ```sh
      $ sudo apt install libcairo2-dev
      ```

   or Fedora:
      ```sh
      $ sudo dnf install cairo-devel
      ```
      
   or Arch:
      ```sh
      $ sudo pacman -S cairo
      ```

4. gi.
   You can install gi using the following command:
   
   On Debian/Ubuntu/Kali:
      ```sh
      $ sudo apt install python-gi python-gi-cairo
      ```
   
   or Fedora:
      ```sh
      $ sudo dnf install pygobject3 cairo-gobject
      ```
      
   or Arch:
   
      (For Python 2.7)
      ```sh
      $ sudo pacman -S python2-gobject python2-cairo
      ```
      (For Python 3.6)
      ```sh
      $ sudo pacman -S python-gobject python-cairo
      ```

## Installation

Install AlienFX using these commands:
  
  ```sh
  $ sudo python setup.py install
  ```
  ```sh
  $ sudo python setup.py install_data
  ```

Note that the second invocation is required to ensure that icon files etc. are
properly installed.

The installation includes a udev rules file that allows AlienFX to access the 
AlienFX USB controller on your computer without needing root permissions. If 
you run the install commands without sudo, then the udev rules file will not 
be installed. 

## Usage

Lighting configurations are stored in "theme files", which are simple json
files stored in ``$XDG_CONFIG_HOME/alienfx``. If ``XDG_CONFIG_HOME`` is not set, then
``~/.config/alienfx`` is used. Both the CLI and GUI programs use these theme
files, and the GUI program allows you to create new themes as well.

See the man page of alienfx for the cli options supported.

Supported models and adding support for new models:
--------------------------------------------------

At present, AlienFX supports and has been tested on the following Alienware models:

1.  M11xR1   Laptop  -  (Needs the correct Zone Codes)
2.  M11xR2   Laptop  -  (Needs the correct Zone Codes)
3.  M11xR3   Laptop  -  (Needs the correct Zone Codes)
4.  M13xR2   Laptop  -  support by [Simon Wood](https://github.com/mungewell)
5.  M13xR3   Laptop  -  (Needs the correct Zone Codes)
6.  M14xR1   Laptop  -  support by [Ashwin Menon](https://github.com/ashwinm76)
7.  M14xR2   Laptop  -  (Needs the correct Zone Codes)
8.  M14xR3   Laptop  -  (Needs the correct Zone Codes)
9.  M15x     Laptop  -  (Needs the correct Zone Codes)
10. M17x     Laptop  -  support by [trackmastersteve](https://github.com/trackmastersteve)
11. M17xR3   Laptop  -  (Needs the correct Zone Codes)
12. M17xR4   Laptop  -  (Needs the correct Zone Codes)
13. M18xR2   Laptop  -  (Needs the correct Zone Codes)
14. Aurora   Desktop -  support by [Bill Ochetski](https://github.com/ochetski)

## Contributing

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) Please read [CONTRIBUTING.md](https://github.com/trackmastersteve/alienfx/blob/master/CONTRIBUTING.md) for further details. 

## Disclaimer

I DO NOT accept responsibility for frying your AlienFX controller chip with my code.
Haven't fried any yet, but this is just so I can sleep at night. ;)
