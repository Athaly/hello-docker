# Hello Docker

## Descripción

Proyecto introductorio para aprender a crear una imagen básica con Docker. Esta imagen imprime un mensaje en consola al ser ejecutada.

## Objetivos

- Crear un archivo `Dockerfile` válido.
- Construir una imagen Docker basada en `alpine:latest`.
- Ejecutar un contenedor que imprima “Hello, Captain!”.
- (Opcional) Permitir personalizar el mensaje con argumentos de compilación.

## Requisitos

- Docker instalado en el sistema.
- Acceso a la terminal y permisos para usar `sudo`.

## Cómo usar

### Construcción básica

```bash
sudo docker build -t hello-captain .
```

### Ejecución

```bash
sudo docker run hello-captain
```

Debería mostrar:

```
Hello, Captain!
```

### Versión avanzada (opcional)

Permite personalizar el nombre usando argumentos:

#### Dockerfile

```Dockerfile
FROM alpine:latest

ARG NAME=Captain
ENV NAME=$NAME

CMD echo "Hello, $NAME!"
```

#### Construcción con nombre personalizado

```bash
sudo docker build -t hello-custom --build-arg NAME=Valentino .
```

#### Ejecución

```bash
sudo docker run hello-custom
```

Salida esperada:

```
Hello, Valentino!
```

## Estructura del proyecto

```
hello-docker/
└── Dockerfile
```
