# Tutorial repository

===================

This repository contains a set of tutorials both for c++ and ipython
applications.

## My notes

### Install

Debian packages for the Ubuntu LTS Versions 16.04 (xenial) and 18.04 (bionic).:

```bash
sudo apt-get update && sudo apt-get install -y software-properties-common apt-transport-https curl
source /etc/lsb-release
curl -L https://users.flatironinstitute.org/~ccq/triqs/master/$DISTRIB_CODENAME/public.gpg | sudo apt-key add -
sudo add-apt-repository "deb https://users.flatironinstitute.org/~ccq/triqs/master/$DISTRIB_CODENAME/ /"
sudo apt-get update && sudo apt-get install -y triqs
```

### Python2 for jupyter

Since triqs need to be run in python2 kernel, see <https://ipython.readthedocs.io/en/stable/install/kernel_install.html>,

```bash
python2 -m pip --version
```

make sure pip version > 9.0. Install pip for Python2 by `sudo apt install python-pip`

```bash
python2 -m pip install ipykernel
python2 -m ipykernel install --user
```

### ImportError: No module named triqs_cthyb

See for instance the example 13 "Exercise solutions for the Valence-Bond DMFT"

Install continuous-time quantum Monte Carlo (CTQMC) algorithm by 'sudo apt-get install -y cthyb'.
<https://triqs.github.io/cthyb/master/>
