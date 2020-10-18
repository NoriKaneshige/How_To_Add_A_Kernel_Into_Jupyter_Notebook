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
