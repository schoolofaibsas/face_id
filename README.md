# Face Recognition

En este primer encuentro, trabajamos en comenzar a entender el funcionamiento de keras y tensorflow, utilizando Python.

El proyecto consiste en capturar y reconocer caras en imágenes obtenidas de una webcam. 

> NOTA: este ejercicio fue creado a partir del trabajo de habrman. Pueden acceder al repo original:
> https://github.com/habrman/FaceRecognition.git

## Requerimientos

### IMPORTANTE!

Necesitamos correr la version de Python 3.6.x (no la 3.7 porque tensorflow-gpu no estaría disponible).

Si necesitan hacer un downgrade, desde el Anaconda navigator pueden hacerlo:

![Alt text](python-version-change.png?raw=true "Change Python Version")

Si están utilizando Visual Studio Code pueden hacerlo en la barra inferior, cambiando el compilador:

![Alt text](python-version.png?raw=true "Change Python Version")

### IMPORTANTE 2!

Verificar que el path a la instalación de Python3.6 está en la variable PATH del sistema. (En general es C:\Program files\Python36).

Luego debemos verificar que estamos utilizando una versión actualizada de pip, ejecutando el siguiente comando:

```
python -m pip install --upgrade pip
```

Hemos dejado un archivo "requirements.txt", donde figuran todos los requerimientos necesarios para ejecutar el programa en "main.py".

Para instalar automáticamente los requerimientos, ejecuten en la consola el siguiente código:

```
pip install --ignore-installed --user -r requirements.txt
```

> NOTA: Para los que no tengan el modelo ResNet, pueden descargarlo del siguiente link:
> https://drive.google.com/file/d/0B5MzpY9kBtDVZ2RpVDYwWmxoSUk/edit

Luego extraerlo en la carpeta "models".

## Ejecución

Para ejecutar el modelo deberán ejecutar el siguiente comando:

```
python main.py './models/model.py' './ids/'
```

Para los que me preguntaron acerca de integrarlo con visual studio, dentro de anaconda navigation se puede instalar Visual Studio Code.

> NOTA: Inicien Visual Studio Code como administrador.

Luego, para incluir los parámetros de inicialización en el debug, tienen que acceder al archivo "launch.json" (Debug --> Add configuration), y agregar los args al primer objeto:

```
{
    "name": "Python: Current File",
    "type": "python",
    "request": "launch",
    "program": "${file}",
    "args": [
        "./models/model.pb",
        "./ids/"
    ]
},
```

## Resultado

![Alt text](working.png?raw=true "Working")


        
