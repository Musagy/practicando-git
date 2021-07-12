# hola

- en git comenzamos editando al usuario con
git config

- y despues iniciamos un repositorio con
    git init

- y despues usamos
    git status
- para ver como estaban los estados de los archivos del repositorio

- agregabamos los archivos con
    git add
- para que pasen al area de preparacion

- esto nos envia a un editor vim en el cual tendremos que poner nuestro mensaje del commit
- para eso presionaremos i para escribir el primer comentario en la primera linea y despues salir con ESC
- despues terminamos poniendo un :wq

- despues puedes ver tus comiciones con
    git log

- ahora si quieres agregar todos los archivos de una carpeta al area de trabajo pon
    git add .

- ahora un atajo para la pasada de commits sin pasar por vim es usar
    git commit -m "mensaje"

- ahora si quieres evitarte el trabajo de enviar SOLO LOS ARCHIVOS MODIFICADOS como commit sin pasar a la area de preparación pon
    git commit -am "mensaje"

- si estamos arrepentidos de los actos que hicimos podemos poner
    git checkout
- esto es para un archivo, pero si quieres hacer lo con todos es
    git checkout -f
- f por f tu trabajo del dia xD
- broma pero es f por forza a que se reinicien todos tus archivos

- la cosa con esto es que no se puede restablecer un archivo ya estando en la area de trabajo o sea los que estan staged
- para hacerlo volver tienes que usar
    git restore "archivo" / git restore .

- ahora si queremos ver las diferencias entre archivos entre su version en modificacion y el del checkpoint se tiene que pore
    git diff "archivo"

- este comando tambien tiene otros tipos como

    git diff --stat "archivo"
    - este es para mostrar cuantas lineas han sido agregadas y cuantas han sido eliminadas

    git diff --numstat "archivo"
    - este solo te pone los numeros, el primer digito los agregados y el segundo los eliminados

- ahora si queremos volve a un estado del proyecto del pasado tenemos que buscar primero en git log cual es al que nosotros queremos ir con su hash, despues tenemos que usar checkout seguido de algunos digitos del principio o todo el hash
    git checkout "hash"

- despues si queremos volver a nuestro punto actual tenemos que poner
    git checkout master

- ahora la presentacion de git log en algo rancia puedes hacerla mas rancia pero con mas informacion con
    git log --raw
    - que es para dar los datos en forma raw o sea din editar

- o tambien puedes hacerlo mas bonito y que todos esten organizados con una linea con
    git log --oneline
    - donde solo veremos la el hash y el comentario aparte de destacar al master de los demas

- ya! pero que aburrido solo tener una rama, como me gustaria tener ot...
- no hay problema papu, puedes crear otras ramas externas a la mitica rama master para no cagarla en ella con esto
    git checkout -b "nombre de rama"

- vez lo sencillo que es =)
- y ahora para volver movernos entre ramas tenemos que poner
    git checkout "rama"
    - y listo papu peto tambien puedes usar
    git switch "rama"
    - y ya tambien

- ahora que tenemos una buena cantidad de commit nos pasara que cuando pongamos git log no nos salgan todos nuestros commits, asi que para ello hay una extencion la cual es
    git log --oneline --all
    - a esta tambien le podemos agregar el --oneline

- que tal si nos cambiamos a master
- ok, ahora veamos el git log pero con la extencion de --graph --decorate
    git log --oneline --all --graph --decorate

- ahora si queremos combinar 2 ramas se tiene que hacer con
    git merge "rama con la que quieres combinar"
    - esto puede causar problemas si has editado el mismo archivo en ambas ramas

- ahora si no podimos hacer el merge, en nuestro editor de codigo, en el archivo con conflito habra salido una zona comparativa de los codigos y tendremos que editarlo para unificarlo. despues tenemos que hacer un commit con esos cambios y ya tendremos la unificacion
- pero si por si a caso quieres evitar el merge porque tiene conflictos,puedes poner
    git merge --abort
    - y listo

- ahora que ya terminamos con ramita2 para que la necesitamos
- hay que eliminarla =)
- para ello esta
    git branch -d "nombre de la rama"
    - para eliminarla

    - y para ver las ramas es
    git branch

- que piola, pero ahora si quiero un archivo que no quiero que git lo reconozca como lo hago

- pues primero tienes que crear un archivo creado .gitignore y en el tendras que poner todos los archivos que no quiere que reconozca

- ahora comenzaremos a hacer un repositorio en git que supongo que mi yo del futuro debe saber muy bien y despues clonar el repositori con
    git clone "http del repositorio"
    
- ahora sera cuestion que tu pongas tus archivo o los crees en esa carpeta y despues de eso hacer le un commit local
- pero ahora, esto no esta en la nube, para ello tenemos que usar
    git push
    
- y ya estara subido

- despues de la gran pelea que tuve en git bush porque no me reconocia los nuevos elementos de la nube, y tardarme mucho para que solo con poner
    git pull
    - ya estuvieran listos los archivo esto de vuelta :)
    - esto sirve para pullear o sea traer los elementos nuevos

- pero antes que puedas pullearlos tienes que descargarlos con
    git fetch origin
    - fetch de FETiCHe por los pies = |
 