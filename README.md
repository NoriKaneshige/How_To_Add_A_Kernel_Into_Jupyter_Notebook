# How_To_Add_A_Kernel_Into_Jupyter_Notebook

## 1) activate a virtual environment

## 2) install ipykernel onto the virtual environment
```
(projectname)$ pip install ipykernel
```
## 3) add a kernel into jupyter notebook
```
(projectname)$ ipython kernel install --user --name=projectname
```
## 4) open a jupyter notebook and choose your kernel
Jupyter Notebook > Kernel > Change kernel > choose your kernel

## 5) trouble shooting
### Error may occur, saying something like "jupyter notebook cannot connect to kernel".
### To use new notebook in other directory, need to delete all previous kernels including python3, then create new kernel
[Useful_Link_1](https://github.com/jupyter/notebook/issues/3481)


[Useful_Link_2](https://github.com/jupyter/notebook/issues/1558)


[Useful_Link_3](https://github.com/udacity/aind2-dl/issues/9)


[Useful_Link_3](https://stackoverflow.com/questions/42635310/remove-kernel-on-jupyter-notebook)


```
(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % pip uninstall ipykernel
WARNING: Skipping ipykernel as it is not installed.

(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % pip install ipykernel
Collecting ipykernel

(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % jupyter kernelspec list
Available kernels:
  deepchem_venv    /Users/Koitaro/Library/Jupyter/kernels/deepchem_venv
  python3          /Users/Koitaro/opt/anaconda3/envs/biophysics_435/share/jupyter/kernels/python3

(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % jupyter kernelspec remove deepchem_venv
Kernel specs to remove:
  deepchem_venv       	/Users/Koitaro/Library/Jupyter/kernels/deepchem_venv
Remove 1 kernel specs [y/N]: y
[RemoveKernelSpec] Removed /Users/Koitaro/Library/Jupyter/kernels/deepchem_venv
(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % jupyter kernelspec remove python3     
Kernel specs to remove:
  python3             	/Users/Koitaro/opt/anaconda3/envs/biophysics_435/share/jupyter/kernels/python3
Remove 1 kernel specs [y/N]: y
[RemoveKernelSpec] Removed /Users/Koitaro/opt/anaconda3/envs/biophysics_435/share/jupyter/kernels/python3

(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % conda install ipykernel
Collecting package metadata (current_repodata.json): done
Solving environment: done
==> WARNING: A newer version of conda exists. <==
  current version: 4.8.3
  latest version: 4.8.5
Please update conda by running
    $ conda update -n base -c defaults conda
# All requested packages already installed.

(biophysics_435) Koitaro@MacBook-Pro-3 biophysics_435 % ipython kernel install --user --name=deepchem_venv
Installed kernelspec deepchem_venv in /Users/Koitaro/Library/Jupyter/kernels/deepchem_venv

```
[volumes_and_bind_mounts](https://github.com/NoriKaneshige/How_To_Add_A_Kernel_Into_Jupyter_Notebook/blob/master/kernel_was_connected.png)
# Now you can open a jupyter notebook in any folder and use a kernel with which you can use all installed modules in the virtual environment that the kernel was created upon.

## 6) How to activate and deactivate a virtual environment through conda
```
(base) Koitaro@MacBook-Pro-3 envs % pwd              
/Users/Koitaro/opt/anaconda3/envs
(base) Koitaro@MacBook-Pro-3 envs % ls
biophysics_435	mypymol
(base) Koitaro@MacBook-Pro-3 envs % conda activate biophysics_435 
(biophysics_435) Koitaro@MacBook-Pro-3 envs % conda deactivate biophysics_435 
deactivate does not accept arguments
remainder_args: ['biophysics_435']

(biophysics_435) Koitaro@MacBook-Pro-3 envs % conda deactivate
(base) Koitaro@MacBook-Pro-3 envs % 
```
