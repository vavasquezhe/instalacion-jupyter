# Configuración de Ubuntu

Esta guía describe el proceso de instalación de Python, IPython, R, Jupyter y
los kernels para Jupyter de R (IRkernel) y Bash (IBash) en Ubuntu.


### Paso 1
Para abrir Terminal, haga click en el ícono de búsqueda. Escriba **`Terminal`**,
y haga click en el ícono de la aplicación.


### Paso 2
Descargue Anaconda con el siguiente comando en Bash.
```
wget  https://repo.anaconda.com/archive/anaconda3-5.2.0-Linux-x86_64.sh
```

### Paso 3
Instale Anaconda.
```
bash Anaconda3-5.2.0-Linux-x86_64.sh
```

### Paso 4
Cuando el instalador le pregunte si agrega Anaconda al path del sistema,
responda **`yes`**.

### Paso 5
Cuando finalice la instalación, cierre **`Terminal`** y vuelva a abrirlo.


### Paso 6
Instale **`pip`** con el siguiente comando en **`Terminal`**:
```
sudo apt install python3-pip
```

### Paso 7
Instale los paquetes requeridos por Python con los siguientes comandos:
```
pip install --upgrade pip
```

```
pip install msgpack
```

```
pip install jupyter_contrib_nbextensions
```

```
jupyter contrib nbextension install --user
```

```
pip install jupyter_dashboards
```

```
jupyter dashboards quick-setup --sys-prefix
```

```
pip install pixiedust_node
```

```
pip install PyQt5
```

```
pip install markdown2
```

```
pip install Flask
```

```
pip install Flask-WTF
```

```
pip install pymysql
```

```
pip install ipython-sql
```

### Paso 8
Instale **`IPython`** con:
```
sudo apt install ipython3
```

### Paso 9
Instale `Jupyter`:
```
pip install jupyter
```

### Paso 10
Verifique que jupyter se encuentra funcionando correctamente. Abra Jupyter:
```
jupyter notebook
```


### Paso 11 (Lenguaje R)
Para instalar el lenguaje R, ejecute el siguiente comando en Bash. El sistema
pedirá su contraseña para poder continuar.

```
sudo apt install r-base
```

### Paso 12
Instale las librerías requeridas por el IRkernel ejecutando los siguientes
comandos en Bash.

```
sudo apt-get install libcurl4-openssl-dev
```

```
sudo apt-get install build-essential
```

```
sudo apt-get install libcurl4-gnutls-dev
```

```
sudo apt-get install libxml2-dev
```

```
sudo apt-get install libssl-dev
```

### Paso 13
Abra el interprete de R con el siguiente comando:

```
sudo -i R
```

### Paso 14
En el prompt de R, ejecute los siguientes comandos para instalar el IRkernel.

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

```
devtools::install_github('IRkernel/IRkernel')
```

### Paso 15
Salga de R con el comando **`quit()`**

### Paso 16
Abra R en la consola de comando:

```
R
```

### Paso 17
Finalice la instalación del IRkernel ejecutando en R el siguiente comando:

```
IRkernel::installspec(user = FALSE)
```

### Paso 18
Verifique que el kernel fue correctamente instalado. Abra jupyter desde Bash con
el siguiente comando:
```
jupyter notebook
```



### Paso 19
En el menú **`New`** de Jupyter debe aparece la opción de crear notebooks que
usen el lenguaje R.


### Paso 20 (IBash)
Abra Bash y ejecute el siguiente comando:
```
sudo chmod u=rwx,g=rwx,o=rwx /usr/local/share
```

### Paso 21
Instale **`IBash`**.

```
pip install bash_kernel
```

```
python -m bash_kernel.install
```

### Paso 22
En el menú **`New`** de Jupyter debe aparece la opción de crear notebooks en
Bash.

![alt](images/macOS-jupyter-IBash.png)
