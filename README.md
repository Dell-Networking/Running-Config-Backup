# Template repo for SONiC PoC Repos


[![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)](#-how-to-contribute)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/Dell-Networking/PoC-SONiC-template/blob/main/LICENSE.md)
[![GitHub issues](https://img.shields.io/github/issues/Dell-Networking/PoC-SONiC-template)](https://github.com/Dell-Networking/PoC-SONiC-template/issues)

Built and maintained by [Ben Goldstone](https://github.com/benjamingoldstone/) and [Contributors](https://github.com/Dell-Networking/PoC-SONiC-template/graphs/contributors)

------------------

## Contents

- [Description and Objective](#-description-and-objective)
- [Requirements](#-requirements)
- [How to Contribute](#-how-to-contribute)


## 🚀 Description and Objective

For smaller networks, some customers require the ability to create a history of configurations over time for their network devices.  They do not require the ability to automatically restore these configurations.  They simply would like to manually inspect configurations of devices over time.  This means that the configuration should be readable in a syntax familiar to them.  This Python script collects the output of ```show running-configuration | no-more``` and can be scheduled using crontab in linux.  As of this writing it has been tested on Ubuntu 20 and Python3.


## 📋 Requirements

Dependency:  Paramiko

1. Download this script and copy it to an appropriate directory.  By default this script will simply save the configurations in the same directory that the script is located in.
2. In the directory where you have copied the file, execute this command: ```chmod +x sonic_config_backup.py```
3. Open crontab for editing with ```crontab -e```
   1. Add an entry to crontab in this manner: ```0 6 * * * /path/to/python3 /path/to/sonic_config_backup.py```
   2. The "0" in this line specifies the minute.  The "6" specifies the hour.  The "* * *" represents the day of the month, the month of the year, and the day of the week respectively.
   3. You can find the path for python3 with the command ```which python3```

## 👏 How to Contribute

We welcome contributions to the project. Please reference the [CONTRIBUTING](https://github.com/Dell-Networking/PoC-Index/blob/main/CONTRIBUTING.md) guide in the PoC-Index repo for more details (this guide is common across Dell Networking PoC projects).


