# Game Project

Para correr el juego debes seguir las siguientes instrucciones en la terminal:

Tomado de: https://github.com/platzi/curso-python-pip

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
```sh
PATH=$(pyenv root)/shims:$PATH
```

#Esto garantiza que cada que abra la terminal se garantice la versión global cuando la terminal esta configurada con zshrc

```sh
echo ‘PATH=$(pyenv root)/shims:$PATH’ >> ~/.zshrc  
```

#Esto garantiza que cada que abra la terminal se garantice la versión global cuando la terminal esta configurada con bash
```sh
echo ‘PATH=$(pyenv root)/shims:$PATH’ >> ~/.bash
```

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

# FAST API
#Tomado de: https://fastapi.tiangolo.com/#installation

#Para levantar el servidor
```sh
uvicorn main:app --reload --port 8080
```

# DOCKER
#Como instalar docker en Mac

Instalador: https://docs.docker.com/desktop/setup/install/mac-install/

Tomado de: https://platzi.com/cursos/python-pip/instalacion-de-docker/

En Mac tienes dos opciones. Todo dependerá si tienes los nuevos chips M1 o Intel, ya que hay un instalable apropiado para ambas arquitecturas de chip. Puedes escoger el instalable desde Install Docker Desktop on Mac.

Adicionalmente, si cuentas con los nuevos chips M1, debes ejecutar la siguiente instrucción en tu terminal softwareupdate --install-rosetta

Una vez descargues el instalador adecuado, solo debes seguir los pasos y pasar Docker Desktop a tus aplicaciones.

#Para instalar Docker desktop en MAC 10.15 - Versiones viejas.

Tomado de: https://www.youtube.com/watch?v=9ALVtKjfmHA

#La que me funciono en MAC 10.15.:

Tomado de: https://stackoverflow.com/questions/68373008/install-docker-on-macos-catalina

It seems that Docker Desktop 4.16 does not support macOS Catalina (10.15) any more.

If you don't want to update to a newer macOS version, you can install an older version of Docker Desktop which still works on macOS Catalina. Docker Desktop 4.15 works on Catalina.

```sh
# Download Cask code for Docker Desktop 4.15.0,93002
curl https://raw.githubusercontent.com/Homebrew/homebrew-cask/1a83f3469ab57b01c0312aa70503058f7a27bd1d/Casks/docker.rb -O

# Install Docker Desktop from Cask Code
brew install --cask docker.rb

# OR

# if Docker Desktop is already installed then reinstall from Cask Code
brew reinstall --cask docker.rb 
```

#Para crear el contenedor
```sh
docker-compose build
```

#Para Subir o inicializar contenedor
```sh
docker-compose up -d
```

#Para validar el contenedor(es) creado(s)
```sh
docker-compose ps
```

#Para ingresar a un contenedor creado, con  una interfaz de ejecución bash
```sh
docker-compose exec "Nombre Contenedor" bash
docker-compose exec app-csv bash
```

#Para bajar un contenedor creado
```sh
docker-compose down
```

#Para jugar con Docker

Tomado de: https://labs.play-with-docker.com/





