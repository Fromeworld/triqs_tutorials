# run triqs in docker (the most convinient way maybe)

<https://hub.docker.com/r/flatironinstitute/triqs>

Install
```bash
docker pull flatironinstitute/triqs
```

TRIQS Docker Image
This builds the flatironinstitute/triqs docker hub image which includes triqs and the applications cthyb, dft_tools, maxent and tprf

It can be used to run a Jupyter notebook environment yourself or on Binder, or to run a shell for development:
```bash
docker run --rm -p 8888:8888 flatironinstitute/triqs
docker run --rm -ti flatironinstitute/triqs bash
```
The Jupyter notebook will be accessible at http://localhost:8888, where you should pass the token provided on the command line. If you want the state of the virtual machine to be stored, drop --rm from the commands above. A summary of useful docker commands can be found her

## run with this folder!

First enable sharing in docker setting
<https://token2shell.com/howto/docker/sharing-windows-folders-with-containers/>

Then
```cmd
docker run --rm -p 8888:8888 --name triqs_run -v %USERPROFILE%\Documents\triqs_tutorials:/home/triqs/tutorials/TRIQSTutorialsPython/triqs_tutorials_github_q flatironinstitute/triqs
```


## docker flags

An example is
```bash
docker run -it -p 8022:22 --ipc host --name docker_example --gpus all -v ~/work:/work tensorflow/tensorflow:latest-gpu-py3-jupyter /bin/bash
```
- -i is 'Allocatea pseudo-tty'
- -t Keep STDIN open even if not attached
- -p port
- -ipc host increasing shared ram
- --name docker_example: name the container
- -gpus all: use all gpus
- -v ~/work:/work: map folder
- tensorflow:latest-gpu-py3-jupyter: mirror version name
