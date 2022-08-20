<p align="center"><img src="https://raw.githubusercontent.com/carjavi/github-guide/master/img/GitHub_Git_logo.png" height="300" alt=" " /></p>
<h1 align="center">Git & Github Guide</h1> 
<h4 align="right">Aug 22</h4>

<img src="https://img.shields.io/badge/OS-Linux%20GNU-yellowgreen">
<img src="https://img.shields.io/badge/OS-Windows%2011-blue">


# git commands
```
git --version
git init
git clone https://github.com/xxxxxx.git

git clone https://TU_USUARIO@github.com/xxxxxxx.git    #Si se trata de un servidor que requiere credenciales, Esto hará que Git te solicite la contraseña de dicho usuario.

git status
git add .    #añadir todo los archivos del directorio al staging area
git commit -m "xxx"

git config     #configurar datos del autor
git config --global user.name "Miguel Díaz Rubio"
git config --global user.email info@migueldiazrubio.com
git config user.name #consultar datos del autor
git config user.email 

git commit --amend   #Corregir un commit recién hecho. Esto hará que los cambios se incluyan en el último commit realizado. se debe hacer un "git add" primero

git log #para ver todos los commit que se han hecho. El comando git log es enormemente potente y cuenta con muchos parámetros. https://git-scm.com/docs/git-log

git checkout   #Cargando versiones antiguas
git checkout NOMBRE_DEL_ARCHIVO   # deshacer los cambios realizados. Antes de haber hecho un git add
git checkout -- .    #pero para todos los archivos.
**Nota** 
Este comando únicamente deshace los cambios en el área de
trabajo, ya que todos los cambios que hayan sido incluidos
en el área de preparación no serán descartados.

git reset --hard        # deshacer los cambios en el área de trabajo & área de preparación. viene acompañado de git clean -df

git checkout

```

<p align="center"><img src="https://raw.githubusercontent.com/carjavi/github-guide/master/img/flow.png"  alt=" " /></p>


# Install Git on Linux ( desde el instalador algunos instaladores de paquetes)
```
apt-get install git-all
dnf install git-all
yum install git
```

# Github

pull request & fork #es para hacer contribuciones a otros proyectos de github donde nno se es colaborador directo





---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/github-guide/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>
