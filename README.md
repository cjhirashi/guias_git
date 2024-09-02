# GIT

## Generales

Visualizar ayuda de git

```bash
git help
```

## Creación de proyecto

Crear una copia de algún repositorio existente

```bash
git clone <URL de repositorio en la nuebe (GitHub)>
```

Crear un reposirotio para nuevo proyecto y lo inicializa

```bash
git init
```

## Configuraciones globales

Configruación global de los datos de programador

Nombre de usuario

```bash
git config --global user.name "Nombre del usuario"
```

Email de usuario

```bash
git config --global user.email "E-mail del usuario"
```

Para cambiar el nombre de rama principal para nuevos proyectos

```bash
git config --global init.defaultBranch <nombre>
```

Enlistar los datos configurados en la configuración global de git

```bash
git config --global -e
```

 1. Esto nos despliega información como la siguiente

```bash
[user]
        name = Nombre de usuuario
        email = Mail de usuario
~            
~              
~                                                               
~/.gitconfig[+] [unix] (17:49 18/07/2024)                               2,26-33 All
-- INSERT --
```
2. Si queremos modificar alguna parte de la configuración, persionamos la tecla `a` y esto nos habilitará para cambiar cualquier parte de la información desplegada.

3. Si queremos salir y guardad la información despues de haber realizado algún cambio, entonces presionamos una vez la tecla `esc` y escribimos los siguientes caracteres en la terminal y presionamos intro

```bash
:wq!
```

4. Si queremos salir sin guardar los cambios, escribir los siguientes caracteres

```bash
:q!
```

### CREAR ALIAS PARA COMANDOS

Para crear un alias de los comandos de git

```bash
git config --global alias.<Nombre corto> <"Comando al que se le aplica el alias">
```

Ejemplo

```bash
git config --global alias.s "status --short"
```
Así se vería como se ejecuta el comando normalmente y el segundo cómo ahora se puede ejecutar con el alias

```bash
git status --short

git s
```

## COMANDOS MANEJO DE REPOSITORIO

### SUBIR Y BAJAR ARCHIVOS AL STAGE

Visualizar el estado de los arvchivos a los que ya le estamos dando seguimiento, cuales están ya en el ***stage*** y qué archivos tienen cambios y no se an subido al ***stage***

```bash
git status
```

Una visualización corta del estado

```bash
git status --short
```

Para subir un archivo al ***stage*** al que se le ha hecho un cambio y se le de seguimiento

```bash
git add <nombre de archivo>
```

Para subir todos los archivos con cambios al ***stage*** para que se les de seguimiento

```bash
git add .
```

Para subir todos los arvchivos con una misma extensión al ***stage*** para que se les de seguimiento

```bash
git add *.<extensión>
```

Esto solo agregará los archivos dentro de la raíz del proyecto, si los archivos se encuentran dentro de una carpeta, hay que indicar la ruta donde se encuentran

```bash
git add carpeta/*.<extensión>
```

Si queremos añadir todos los archivos dentro de un mismo directorio (carpeta), junto con sus dierectorios

```bash
git add carpeta/
```

Cuando se agrega una carpeta vacía al proyecto, git no la gestiona, solo hasta que tiene contenido, por ejemplo la carpeta ***uploads***, en este caso, esa carpeta se ocupa para archivos que carga el usuario, por lo que en desarrollo puede estar vacía, en este caso para que Git la considere y la administre en el repositorio, hay que agregarle un archivo ***.gitkeep***, de esta forma la carpeta puede ser gestionada en el repositorio

Si queremos remover un archivo que ya se haya cargado al ***stage*** para que no se considere en el commite

```bash
git reset <nombre de archivo>
```

### COMMITS DE PROYECTO

Para tomar imagen de los cambios en los archivos cargados en el ***stage***

```bash
git commit -m "Nombre del commit"
```

Para regresar el proyecto a como estaba a como quedó en el último commit

```bash
git checkout -- .
```

Este comando mostrará qué archivos no tienen seguimiento y cuales si para realizar commite

Para visualizar el registro de los commits realizados en el proyecto

```bash
git log
```

Para salir del Log

```bash
:q
```

### RAMAS DEL PROYECTO
Para saber en qué rama estamos trabajando

```bash
git branch
```

Para cambiar el nombre de una rama

```bash
git branch -m <Nombre actual> <Nuevo nombre>
```

Para enlazar el proyecto de git al repositorio en github, hay que crear un repositorio primero, al crear este repositorio, nos
entregará los siguientes comandos para enlazar el proyecto al repositorio.

```bash
git remote add origin https://github.com/"Cuenta github"/"Nombre del repositorio" #genera la conexión con el repositorio
    
git branch -M main  #Cambia la rama master del repositorio
    
git push -u origin main #Sube el proyecto al repositorio
```

Para singronizar el proyecto de git con github ejecutar el siguiente comando

```bash
git push
```