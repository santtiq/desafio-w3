# Desafio Técnico - w3 IT Solutions

Bienvenido a un desafío tecnico sobre una aplicación simple que proporciona información sobre los países y su población.


## Estructura del Proyecto

El proyecto se organiza en dos partes: la api y el frontend.

- **api/**: Contiene el código del servidor Express que gestiona las solicitudes relacionadas con la información de los países.

  - **Configuración del Puerto:**
    El servidor se ejecuta en el puerto 8080 de forma predeterminada. Para personalizar el puerto, se recomienda crear un archivo `.env` en la carpeta `backend` y definir la variable `PORT`. Si no se proporciona un archivo `.env`, el servidor se ejecutará en el puerto 8080.

    ```bash
    # backend/.env
    PORT=tupuerto
    ```
    Tené en cuenta que si decidís cambiar el puerto en el backend, tenes que asegurarte de actualizar la solicitud de la API en el front ubicada en el archivo `front-countries/app/components/Search.jsx`. Busca la línea donde se hace la solicitud y ajusta el puerto en la URL en consecuencia.

    ```jsx
    // frontend/app/components/Search.jsx
    const res = await axios.get(`http://localhost:8080/buscar?valor=${valor}`)
    ```


- **frontend/**: Alberga la interfaz de usuario construida con React y Next.js 13. Consta de una pagina con un input encargado de buscar, según que país se coloque, su nombre (si es que hay mas de una coincidencia), población y porcentaje.


## Requisitos Previos

- Node.js y npm deben estar instalados en tu sistema. Puedes descargarlos desde [el sitio oficial de Node.js](https://nodejs.org/).


## Configuración Inicial

1. Clonar el repositorio:
    ```bash
    git clone https://github.com/santtiq/desafio-w3.git
    cd desafio-w3
    ```

2. Instala las dependencias del backend y frontend:
    ```bash
    cd api-countries
    npm install

    cd front-countries
    npm install
    ```


## Ejecución del Proyecto

1. **Inicia el Backend:**
    ```bash
    cd api-countries
    nodemon app
    ```

    El servidor estará disponible en `http://localhost:8080` si no se proporciona un archivo `.env`. En caso de que se configure un archivo `.env`, el servidor se ejecutará en el puerto especificado en la variable `PORT`.

2. **Inicia el Frontend:**
    ```bash
    cd front-countries
    npm run dev
    ```

   La aplicación estará disponible en `http://localhost:3000`.