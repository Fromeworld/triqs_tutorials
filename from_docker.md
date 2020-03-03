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