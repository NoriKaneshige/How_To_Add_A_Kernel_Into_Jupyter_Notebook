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
