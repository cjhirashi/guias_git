# GIT

## Generales

Visualizar ayuda de git

```bash
git help
```

Visualizar el estatus del repositorio

```bash
git status
```

Este comando mostrará qué archivos no tienen seguimiento y cuales si para realizar commite

Para visualizar el registro de los commits realizados en el proyecto

```bash
git log
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

## COMANDOS MANEJO DE REPOSITORIO

Para subir un archivo al ***stage*** al que se le ha hecho un cambio y se le de seguimiento

```bash
git add <nombre de archivo>
```

Para subir todos los archivos con cambios al ***stage*** para que se les de seguimiento

```bash
git add .
```

Si queremos remover un archivo que ya se haya cargado al ***stage*** para que no se considere en el commite

```bash
git reset <nombre de archivo>
```
    
Para tomar imagen de los cambios en los archivos cargados en el ***stage***

```bash
git commit -m "Nombre del commit"
```

Para regresar el proyecto a como estaba a como quedó en el último commit

```bash
git checkout -- .
```

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