
# Instalación de Helm

En este apartado mostraremos como se instala Helm

## Requisitos previos:
 - Tener instalado minikube.
 -  Tener instalado kubectl.
## Paso 1:
Nos descargaremos la version de Helm que más nos convenga desde [aquí](https://github.com/helm/helm/releases).
En nuestro caso hemos descargado la version de ***linux-amd64***.

## Paso 2
Pasaremos a descomprimir nuestro archivo descargado:

```
tar -zxvf helm-v3.0.0-linux-amd64.tar.gz
```

## Paso 3
Helm es un binario, es decir, ***no hay necesidad de instalarlo***. Para ello nos basta con mover el binario que se encuentra dentro de la carpeta descomprimida a  nuestro directorio deseado:

```
mv linux-amd64/helm /usr/local/bin/helm
```

## Paso 4

Ya estaría listo, con irnos a la terminal y escribir "helm version"  nos mostrará que version tenemos

![2-a](https://github.com/mloparj10/helm-de-KUBERNETES/blob/main/images/2-a.png)
