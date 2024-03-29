<p align="center"><img src="https://raw.githubusercontent.com/carjavi/github-guide/master/img/GitHub_Git_logo.png" height="300" alt=" " /></p>
<h1 align="center">Git & Github Guide</h1> 
<h4 align="right">Aug 22</h4>

<img src="https://img.shields.io/badge/OS-Linux%20GNU-yellowgreen">
<img src="https://img.shields.io/badge/OS-Windows%2011-blue">


# git commands
## Comandos Importantes


config # GIT Setting
```
git config --global user.name "Miguel Díaz Rubio" // configuracion global 
git config --global user.email info@migueldiazrubio.com

git config --list #q para salir
git config     #configurar datos del autor

git config user.name #consultar datos del autor
git config user.email #consultar datos del autor

```

Git basic commands
```
git --version

----------------------------------

git init     #le informa al sistema operativo que se va a usar git. Se crea una carpeta oculta .git donde se guardan las versiones.

------------------------------------

git status   #ver si ha cambiado algo en los archivos / ver quien esta en el área de working o staging. 
Si dice working tree clean // no hay nada que actualizar. Los archivos rojos son los archivos que han sido modificados. Los verdes ya se han actualizado

------------------------------------

git add <nombre-archivo> #agraga archivo al staging area
git rm --cached <file-name> #saca al archivo del staging area
git add .    #añadir todo los archivos del directorio al staging area – o área de listado 

git add remote origin

--------------------------------

git push  #lo sube al repositorio remoto

git push origin master
# push: Transfiere commits del repositorio local al remoto
# origin master: Rama maestra (master) al servidor origen (origin)

--------------------------------

git pull  #trae los cambios que hacen los otros desarrolladores

git pull origin master   #Para poder descargar los cambios de remote. De nuevo estás utilizando los parámetros origin para indicar que quieres hacer del pull de tu repositorio remoto definido con el comando anterior

--------------------------------

git diff <file>   #muestra los cambios que ha sufrido ese archivo. Verde lo que se ha agregado y rojo lo que se ha quitado

------------------------------

git log    #para ver todos los commit que se han hecho. El comando git log es enormemente potente y cuenta con muchos parámetros. https://git-scm.com/docs/git-log. con "q" podemos salir. 

--------------------------------

git checkout   #Cargando versiones antiguas
git checkout NOMBRE_DEL_ARCHIVO   # deshacer los cambios realizados. Antes de haber hecho un git add
git checkout -- .    #pero para todos los archivos.

**Nota** 
Este comando únicamente deshace los cambios en el área de
trabajo, ya que todos los cambios que hayan sido incluidos
en el área de preparación no serán descartados.

```


clone
```
git clone https://github.com/xxxxxx.git   #clonas o descarga los archivos del repositorio.

git clone https://TU_USUARIO@github.com/xxxxxxx.git    #Si se trata de un servidor que requiere credenciales, Esto hará que Git te solicite la contraseña de dicho usuario.

git clone --depth=1 https://github.com/marcorodas/ApuntesAndroid.git ApuntesAndroid  

-clone: Crea una copia local del repositorio central al cual llamará "origin"
-Crea una carpeta .git donde se almacenan todos los commit
- --depth=1: Sólo el último commit
```


commit 
```
git commit -m "xxx"  #empaqueta los archivos y se puede dejar un comentario / se crea el snapshop / evita e editor de código

git commit   #con solo este comando solo, me preguntara quien soy y mi clave cuando se hace por primera vez. Luego aparece un editor, si es VIM con tecla “i” puedo  insertar comentario, esc .. wq y me salgo del editor

git commit    # https://git-scm.com/docs/git-commit/2.21.0
git commit -n  # Esta opción pasa por alto los ganchos de pre-commit y commit-msg (interactivo)

git commit -q  #Suprimir el mensaje de resumen de confirmación. (interactivo)

git commit --amend   #Corregir un commit recién hecho. Esto hará que los cambios se incluyan en el último commit realizado. se debe hacer un "git add" primero
```








# Commandos Avanzados
```
git reset --hard        # deshacer los cambios en el área de trabajo & área de preparación. viene acompañado de git clean -df. permite bajar los nuevos cambios sin importar que se hayan cambiado los archivos locales

git reset --p
git reset .
git reset HEAD .

-------------------------------------

git rm    #elimina su copia de trabajo local del archivo

git rm --cached .   #cached Use esta opción para separar y eliminar rutas solo del índice

-------------------------------------

git checkout

--------------------------------------

git fetch origin 
git fetch
# fetch: Importa commits del repositorio remoto al local. 
#        (http://git-scm.com/docs/git-fetch)
#        Si no se especifica ningún repositorio se usará el repositorio remoto "origin"
#        Los guarda como branches remotos. No afecta la copia local.

----------------------------------------

git reset --hard origin/master
# reset: Establece el HEAD (top commit) de la rama actual al commit espeficicado. 
#        (https://git-scm.com/docs/git-reset)
#        En este caso la rama "master" del repositorio remoto "origin"
# --hard: Reinicia el índice y el directorio de trabajo
#         Los cambios fuera del commit especificado son eliminados.

```


<p align="center"><img src="https://raw.githubusercontent.com/carjavi/github-guide/master/img/flow.png"  alt=" " /></p>


# Install Git on Linux ( desde el instalador algunos instaladores de paquetes)
```
apt-get install git-all
dnf install git-all
yum install git
```

# Samples repositorios remotos
```
echo "# Nombre Proyecto" >> README.md
git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/carjavi/nombre_proyecto.git
git push -u origin master

```


# Github

## Cómo borrar un repositorio en github:
1.	ir al repositorio elegido:
2.	ir a la pestaña settings:
3.	bajar hasta el final de la página:
4.	clickar botón de suprimir:
5.	Confirmar escribiendo el nombre del repositorio a eliminar:


## pull request & forks     
son para hacer contribuciones a otros proyectos de github donde nno se es colaborador directo.

Cuando dice esto:
```
On branch master nothing to commit, working tree clean
```
Esto quiere decir que tu repositorio, área de preparación y área de trabajo
tienen exactamente la misma versión de los ficheros que componen el
repositorio.


## Buenas prácticas 
 * con ```q``` podemos salir de los comandos GIT
 * En GIT únicamente deberían guardarse archivos planos  y  archivos pequeños (como logos) que no sufran casi modificaciones durante la vida del proyecto. Los binarios deben guardarse en un CDN.



---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/github-guide/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>
