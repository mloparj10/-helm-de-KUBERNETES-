
# CASO PRÁCTICO: DESPLIEGUE DE WORDPRESS

En el apartado anterior aprendimos a manejar los reposirotios de Helm. Ahora toca porfín aprender un despliegue de una aplicación, en este caso Wordpress.

## Busqueda del paquete

Vamos a buscar en nuestro repositorio de Bitnami wordpress:

```
helm search repo wordpress
```

![4-a](4-a.png)

Vamos a instalar el priemro que sale, bitnami/wordpress, que trae la version de la app 5.9.0.

Pero antes de instalarla tenemos que hacer un paso previo.

## Parametización

Vamos a parametrizar el wordpress, indicando dos parámetros: el tipo de servicio y el nombre del blog. Para mirar que parametros tenemos que cambiar, buscaremos el chart que hemos elegido antes en [Artifact Hub](https://artifacthub.io/). Esta página sirve para buscar charts. (Como en la terminal, pero de forma gráfica y por una interfaz web). 

Si buscamos "wordpress" Nos aparecerán varios resultados. Nosotros vamos a coger [el segundo](https://artifacthub.io/packages/helm/bitnami/wordpress), que está desarrollado por Bitnami:

![4-b](4-b.png)

Al pinchar en él y bajar por su página, enmcontraremos lso parámetros.

Para el tipo de servicio:

![4-c](4-c.png)

Yo quiero cambiarlo a NodePort.

Para el nombre del blog:

![4-d](4-d.png)

Yo le pondre de nombre "Blog de Mario sobre Helm"

Ya tenemos localizados los parametros. Ya es ora de instar Wordpress:

```
helm install wordpress-mario bitnami/wordpress --set service.type=NodePort --set wordpressBlogName="Blog de Mario sobre Helm"
```

![4-e](4-e.png)

La instalacion ha sido un éxito.

## Comprobación de los objetos creados.

```
kubectl get all
```

![4-f](4-f.png)

Como observamos se ha desplegado todo lo necesario.

## Acceso a la aplicación

Vamos a obtener la IP y el puerto para acceder al wordpress:

![4-g](4-g.png)
![4-h](4-h.png)

Accedemos desde nuestro navegador favorito:
Y como observamos, funciona, y el nombre de arriba a la izquierda es el que definimos en los parametros:

![4-i](4-i.png)


