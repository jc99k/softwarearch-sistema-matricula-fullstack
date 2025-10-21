# Sistema de Matrícula Fullstack

Este proyecto es una aplicación full-stack para un sistema de matrícula universitaria. Está compuesto por un servicio de backend y un servicio de frontend, cada uno gestionado como un submódulo separado.

## Submódulos

Este repositorio utiliza submódulos de Git para gestionar sus componentes. Los submódulos son:

-   `softwarearch-sistema-matricula-backend`: La API de backend construida con Python/Flask.
-   `softwarearch-sistema-matricula-frontend`: La aplicación de frontend construida con React/TypeScript.

### Clonar el Repositorio

Para clonar este repositorio y sus submódulos, usa el siguiente comando:

```bash
git clone --recurse-submodules <url-del-repositorio>
```

Si ya has clonado el repositorio sin los submódulos, puedes inicializarlos con:

```bash
git submodule update --init --recursive
```

## Ejecutar la Aplicación con Docker Compose

La pila completa de la aplicación se puede ejecutar usando Docker Compose.

### Prerrequisitos

-   Docker
-   Docker Compose

### Configuración

1.  **Variables de Entorno**: Este proyecto utiliza un archivo `.env` para la configuración. Asegúrate de tener un archivo `.env` en el directorio raíz con las variables necesarias definidas. Un `.env.example` podría proporcionarse en los submódulos, pero para el `docker-compose.yml` raíz, deberás crearlo.

2.  **Construir y Ejecutar**: Para construir e iniciar los servicios, ejecuta el siguiente comando desde el directorio raíz del proyecto:

    ```bash
    docker-compose up --build
    ```

    Este comando:
    -   Construirá las imágenes de Docker para los servicios de backend y frontend.
    -   Iniciará los contenedores para todos los servicios definidos en el archivo `docker-compose.yml`.

    Para ejecutar los contenedores en segundo plano, usa la bandera `-d`:

    ```bash
    docker-compose up --build -d
    ```

### Acceder a la Aplicación

-   **Frontend**: El frontend estará disponible en `http://localhost:5173`.
-   **Backend API**: La API de backend estará disponible en `http://localhost:5000`.

### Detener la Aplicación

Para detener los contenedores en ejecución, usa:

```bash
docker-compose down
```
