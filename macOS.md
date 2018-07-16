# Configuración de Mac OS

Esta guía describe el proceso de instalación y configuración de Anaconda (que
incluye Python, IPython y Jupyter), el lenguaje R, RStudio y los kernels para
Jupyter de R (IRkernel) y Bash (IBash) en el sistema operativo macOS.



### Paso 1 (Anaconda Python)
Descargue del sitio [https://www.continuum.io/downloads](https://www.continuum.io/downloads) el
instalador de Python 3.7 – Anaconda para OS X.


### Paso 2
Ejecute el instalador y acepte todas las opciones por defecto.


### Paso 3
Instale los paquetes requeridos por Python. El listado se encuentra
en el archivo [lista-python.md](lista-python.md)

### Paso 4 (Lenguaje R)
Descargue el instalador del lenguje R del sitio
[https://www.icesi.edu.co/CRAN/](https://www.icesi.edu.co/CRAN/)
haciendo click en **`Download R for (Mac) OS X`**.

### Paso 5
Descargue y ejecute el instalador.


### Paso 6
Una vez finalice la instalación, abra ``Terminal`` en
**``Finder > Aplicaciones > Utilidades > Terminal.``**.

### Paso 7
En Terminal ejecute **`R`** para abrir el interprete del lenguaje R en la
consola de comandos.


### Paso 8
En **`R`** ejecute el siguiente comando para actualizar la configuración
internacional en el interprete del lenguaje.

```
> system('defaults write org.R-project.R force.LANG en_US.UTF-8')
```

### Paso 9
Luego ejecute los siguientes comandos en el prompt de **`R`** para instalar
el ``IRkernel``.

```
install.packages('repr')
```

```
install.packages('IRdisplay')
```

```
install.packages('evaluate')
```


```
install.packages('crayon')
```

```
install.packages('pbdZMQ')
```

```
install.packages('devtools')
```

```
    install.packages('uuid')
```

```
    install.packages('digest')
```

````
devtools::install_github('IRkernel/IRkernel')
```

```
IRkernel::installspec(user = FALSE)
```


### Paso 10
Salga de **`R`** con:
```
> quit()
```

### Paso 11
Verifique que el kernel de ``R`` fue instalado correctamente. Abra jupyter desde
``Terminal`` con el siguiente comando:
```
$ jupyter notebook
```
En el menú **`New`** de Jupyter debe aparece la opción de crear notebooks que
usen el lenguaje R.

![alt](images/macOS-jupyter-R.png)


### Paso 12
Instale los paquetes de R que aparecen en el archivo [lista-R.md](lista-R.md)


### Paso 13 (RStudio)
Vaya a la pagina [https://www.rstudio.com/products/RStudio/](https://www.rstudio.com/products/RStudio/)
y descargue RStudio Desktop.

### Paso 14
Ejecute el instalador.


### Paso 15 (IBash)
Abra ``Terminal`` y ejecute los siguientes comandos para Instalar IBash.
```
$ pip install bash_kernel
$ python -m bash_kernel.install
```

### Paso 16
Verifique que en el menú **`New`** de Jupyter debe aparece la opción de crear notebooks en Bash.

![alt](images/macOS-jupyter-IBash.png)
