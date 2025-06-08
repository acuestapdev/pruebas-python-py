# Game Project

Para correr el juego debes seguir las siguientes instrucciones en la terminal:

```sh
cd game
python3 main.py
```


# App Project

```sh
git clone 
cd app
python3 -m venv env
source env/bin/activate
pip3 install -r requirements.txt
python3 main.py
```

# About Python

Para el manejo de varias versiones de python
Tomado de: https://www.youtube.com/watch?v=9xn1F6JzHUk

#Se debe instalar: 
```sh
brew install pyenv
```
#Instalar la versión de python deseada
```sh
pyenv install “version python” 
```
#Configurar la version general de python
```sh
pyenv global “version python” 
```
#Esto considera a pyenv como el gestor de las versiones de python
PATH=$(pyenv root)/shims:$PATH

#Esto garantiza que cada que abra la terminal se garantice la versión global cuando la terminal esta configurada con zshrc

```sh
echo ‘PATH=$(pyenv root)/shims:$PATH’ >> ~/.zshrc  
```

#Esto garantiza que cada que abra la terminal se garantice la versión global cuando la terminal esta configurada con bash

echo ‘PATH=$(pyenv root)/shims:$PATH’ >> ~/.bash

#Para configurar una versión en una carpeta de proyecto puntual
```sh
cd /“Carpeta proyecto”
pyenv local “version python”
```
# Crear ambientes virtuales para cada modulo o proyecto e instalar dependencias necesarias

#Crear ambiente virtual
```sh
python3 -m venv env
```

#Instalar dependencias y modulos necesarios para el proyecto
```sh
source env/bin/activate
pip3 install -r requirements.txt
```

#Para guardar info de dependencias instalads en ambiente virtual
```sh
pip3 freeze > requirements.txt
```