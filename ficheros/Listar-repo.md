# Trabajando con los repositorios

Un repositorio es el lugar donde se pueden recopilar y compartir Charts. 

## Listar repositorios

Para ver los repositorios que tenemos añadidos (que será de donde descargará nuestros proximos charts para los despliegues) utilizaremos el siguiente comando:

```
helm repo list 
```

![3-a]()

Si acabas de instalar Helm, es probable que tu lista de repositorios esté vacía.


## Añadir repositorios: bitnami

Como nuestra lista está vacía, habrá que añadirle alguno. Podemos añadir la cantidad que queramos de repositorios distintos.
Vamos a añadir en este caso los de [Bitnami](https://bitnami.com/). Es una de las principales bibliotecas con las que trabaja Helm.
Para añadir utilizaremos el siguiente comando:

```
helm repo add bitnami https://charts.bitnami.com/bitnami
```

![3-b]()

Donde pone "Bitnami" es el nombre que queremos ponerle al repositorio. (No importa como lo llamemos, pero es aconsejable poner un nombre relacionado con el repositorio)

La dirección https seria la del repositorio deseado

## Quitar repositorios 

Si el repositorio no nos gusta, vemos que trae pocos paquetes, o que no encontramos el que queremos (En el caso de Bitnami no creo que ocurra ya que este cuenta con un amplio repertorio) podemos quitar el repositorio para que Helm no vueva a buscar en él.
Se utiliza el siguiente comando:

```
helm repo  remove bitnami
```

![3-c]()

## Buscar charts: nginx, wordpress, etc

Es hora de buscar aplicaciones que queramos desplegar. Es un comando muy simple, que si sabes inglés y te has visto los comandos anteriores no es muy dificil de acertar:

```
helm search repo nombre_app
```

Donde he puesto "nombre_app" obviamente lo sustituimos por la aplicacion que queramos buscar. En este caso yo quiero buscar un Nginx:

![3-d]()
