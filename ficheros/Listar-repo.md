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
Como nuestra lista está vacía, habrá que añadirle alguno.
Vamos a añadir en este caso los de [Bitnami](https://bitnami.com/)
Para añadir utilizaremos el siguiente comando:
```
helm repo add bitnami https://charts.bitnami.com/bitnami
```

## Quitar repositorios 

## Buscar charts: nginx, wordpress, etc
