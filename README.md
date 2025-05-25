# Configuración del entorno para el proyecto Notebook-MachineLearning

Este README explica cómo preparar el entorno de desarrollo utilizando **pyenv-win** para manejar versiones de Python, instalar Python 3.11.9 y crear un entorno virtual.

---

## Requisitos previos

- Git instalado en tu sistema.
- Acceso a la terminal (PowerShell, CMD o Git Bash en Windows).

---

# Paso 1: Instalar pyenv-win

Para gestionar versiones de Python en Windows usaremos [pyenv-win](https://github.com/pyenv-win/pyenv-win).

Clona el repositorio e instala pyenv-win con los siguientes comandos:

En PowerShell: 

```bash
git clone https://github.com/pyenv-win/pyenv-win.git "$HOME\.pyenv"
```

En CMD:
```bash
git clone https://github.com/pyenv-win/pyenv-win.git %USERPROFILE%\.pyenv
```

Luego, agrega las variables de entorno en tu perfil para que pyenv esté disponible en la terminal

Para una instalacion de este proyecto es recomendable seguir el [tutorial_de_pynev-win](https://github.com/pyenv-win/pyenv-win/blob/master/docs/installation.md#git-commands)


Ahora terminado de agregar las variables de entorno es recomendable reiniciar la terminal y ejecutar:

```bash
pyenv --version
```

Para ver la version de nuestro pyenv

# Paso 2: Instalar Python 3.11.9
Con pyenv instalado, instala la versión de Python requerida para el proyecto:

```bash
    pyenv install 3.11.9
```

Configura la versión local de Python para este proyecto:
```bash
pyenv local 3.11.9
```

Verifica que la versión está activa:
```bash
pyenv versions
```
Deberías ver 3.11.9 marcada con un asterisco (*) indicando que está activa.

# Paso 3: Crear y activar entorno virtual

Desde la carpeta raíz del proyecto ejecuta:
```bash
python -m venv tf-env
```
En caso de no servir puede usar la python.exe del root (cambiar "tu-usuario" por el nombre de tu usuario) ejecuta este comando :
```bash
 C:\Users\tu-usuario\.pyenv\pyenv-win\versions\3.11.9\python.exe -m venv tf-env
```


Activa el entorno virtual:

En PowerShell:
```bash
.\tf-env\Scripts\Activate.ps1
```

En CMD:
```bash
.\tf-env\Scripts\activate.bat
```

Verifica la versión de Python dentro del entorno:
```bash
python --version
```
# Paso 4: Instalar dependencias

Hacemos:
```bash
 pip install numpy pandas matplotlib seaborn pillow opencv-python scikit-learn tensorflow
```

# Paso 5: Cambiar Kernel de Jupyter

Simplemente vamos a Visual Studio Code y en la parte superior izquierda donde aparece una version de python como 3.11.9, dar click y seleccionar entornos de python, escoger la version de pyenv