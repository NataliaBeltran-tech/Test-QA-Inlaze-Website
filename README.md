<h1>Instrucciones para Ejecutar Scripts de Automatización con Cypress</h1>

Este repositorio contiene scripts de automatización para pruebas end-to-end (E2E) utilizando Cypress. 

Los archivos incluidos son:

1. login_de_usuarios.cy.js: Pruebas de inicio de sesión.
2. registro_de_usuarios.cy.js: Pruebas de registro de usuarios.

A continuación, se detallan las instrucciones para configurar el entorno y ejecutar los scripts de automatización desde Visual Studio Code.

<h2>Requisitos Previos</h2>

Asegúrate de tener lo siguiente instalado: 

1. Node.js (versión 14 o superior).
2. Visual Studio Code.
3. Extensión de Cypress instalada en Visual Studio Code (opcional pero recomendada).

<h2>Instalación de Cypress</h2>

1. Abre Visual Studio Code.

2. Abre el terminal integrado (Ctrl + ñ).

3. Navega al directorio del proyecto con el comando: cd ruta/del/proyecto

4. Inicializa el proyecto (si no se ha hecho previamente) con el comando: npm init -y

5. Instala Cypress ejecutando el siguiente comando: npm install cypress --save-dev

<h2>Estructura del Proyecto</h2>

1. Asegúrate de que los scripts estén colocados en la siguiente ruta dentro del proyecto:

cypress/​specs/
  |-- login_de_usuarios.cy.js
  |-- registro_de_usuarios.cy.js

2. Configuración del Archivo package.json

3. Verifica que el archivo package.json incluya un script para abrir Cypress:

"scripts": {
  "cypress:open": "cypress open",
  "cypress:run": "cypress run"
}

<h2>Instrucciones para Ejecutar los Scripts</h2>

1. Abrir Cypress en Modo Interactivo

   a. Ejecuta el siguiente comando en el terminal para abrir la interfaz de Cypress: npm run cypress:open

   b. Una vez que se abra la ventana de Cypress, selecciona login_de_usuarios.cy.js o registro_de_usuarios.cy.js según la prueba que quieras ejecutar.

2. Ejecutar Cypress en Modo de Ejecución Automática (Headless)

   Para ejecutar las pruebas directamente desde el terminal sin interfaz: npx cypress run --spec "cypress/specs/login_de_usuarios.cy.js" o 

   npx cypress run --spec "cypress/specs/registro_de_usuarios.cy.js", esto ejecutará los scripts y mostrará el resultado en el terminal.

3. Configuración Opcional

   Si deseas que Cypress se ejecute en un navegador diferente al predeterminado (Chrome, Firefox, etc.), puedes especificarlo así:

   npx cypress run --spec "cypress/specs/login_de_usuarios.cy.js" --browser chrome

4. Solución de Problemas

   a. Error: Cypress no se instala correctamente: Verifica que Node.js esté instalado correctamente y que tu versión sea compatible.

   b. El terminal no reconoce el comando cypress: Asegúrate de haber ejecutado npm install cypress --save-dev.

