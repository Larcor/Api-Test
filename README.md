## 🖥️ Pruebas de API (Postman / Newman)

Este repositorio contiene las pruebas automatizadas de los servicios utilizando postman y newman

### 🛠️ Configuración e Instalación

1.  **Requisito:** Instalar **Node.js y npm** (el gestor de paquetes de Node.js).
2.  **Instalar Newman y el Reportero HTML (Globalmente):**

    ```bash
    npm install -g newman
    npm install -g newman-reporter-htmlextra
    ```

### 🚀 Instrucciones de Ejecución

El comando siguiente asume que el archivo de **colección** (`Prueba.postman_collection.json`) est en la raíz del repositorio.

#### Comando de Ejecución Completo (la evidencia se genera en la carpeta Resultados)

```bash
newman run Prueba.postman_collection.json -e MiEntorno.postman_environment.json -r htmlextra --reporter-htmlextra-export "resultados/Reporte_Prueba_API.html" --reporter-htmlextra-title "Prueba Técnica API"
