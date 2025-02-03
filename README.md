# Urban.Grocers-Functional-Test-With-API
En este proyecto se realizaron pruebas funcionales y de integración sobre la API **Urban.grocers**. Se verificó que los endpoints respondieran correctamente a las solicitudes usando **Postman** y cubriendo los métodos HTTP: **GET**, **POST**, **PUT** y **DELETE**.

## Objetivo de las Pruebas

El objetivo de las pruebas es asegurar que los endpoints de la API respondan correctamente a las solicitudes y manejen adecuadamente los parámetros proporcionados. Se realizaron pruebas funcionales para verificar que las solicitudes **GET**, **POST**, **PUT** y **DELETE** funcionen correctamente, así como pruebas de comportamiento para asegurar que la lógica del servidor sea coherente con las expectativas.

### Tipos de Pruebas Realizadas:

1. **Pruebas Funcionales**: Se realizaron pruebas para asegurar que los endpoints respondieran correctamente a las solicitudes, incluyendo la creación, lectura, actualización y eliminación de recursos. Los tipos de pruebas realizadas fueron:
   - **Pruebas de Solicitudes GET**: Verificación de que el endpoint GET devuelve la lista de recursos solicitada.
   - **Pruebas de Solicitudes POST**: Verificación de que el endpoint POST crea correctamente un nuevo recurso.
   - **Pruebas de Solicitudes PUT**: Verificación de que el endpoint PUT actualiza correctamente los recursos existentes, aunque se identificó un problema donde algunos cambios no se reflejaban como se esperaba.
   - **Pruebas de Solicitudes DELETE**: Verificación de que el endpoint DELETE elimina correctamente un recurso.

2. **Pruebas de Integración**: Se validó que los endpoints de la API interactuaran correctamente con la base de datos o los servicios backend, asegurando que las solicitudes de creación, obtención, actualización y eliminación de recursos se procesaran correctamente.

3. **Pruebas de Comportamiento**: Se evaluó que las respuestas de la API fueran correctas, validando los códigos de estado HTTP (200, 201, 204) y el contenido de las respuestas. También se verificó que los errores fueran gestionados adecuadamente, especialmente en las solicitudes PUT.

4. **Pruebas de Validación de Errores**: Se detectó que algunas solicitudes PUT no reflejaron los cambios en los recursos, lo que indica un problema con la lógica del servidor que maneja la actualización de los recursos. Este problema requiere revisión y corrección.

## Herramientas Utilizadas

- **Postman**: Utilizado para realizar las pruebas de los endpoints de la API.

## Endpoints Probados

- `GET /api/v1/resource`: Recupera una lista de recursos.
- `POST /api/v1/resource`: Crea un nuevo recurso.
- `PUT /api/v1/resource/{id}`: Actualiza un recurso existente.
- `DELETE /api/v1/resource/{id}`: Elimina un recurso.

## Resultados de las Pruebas

### 1. **GET /api/v1/resource**
   - **Resultado**: Éxito
   - **Descripción**: La solicitud GET retorna correctamente la lista de recursos con un código de estado 200. Los datos fueron consistentes con las expectativas.

### 2. **POST /api/v1/resource**
   - **Resultado**: Éxito
   - **Descripción**: La solicitud POST crea un nuevo recurso correctamente, con un código de estado 201. La respuesta incluye el nuevo recurso con todos los campos requeridos.

### 3. **PUT /api/v1/resource/{id}**
   - **Resultado**: Parcialmente exitoso
   - **Descripción**: La solicitud PUT actualiza el recurso especificado. Sin embargo, algunos cambios no se reflejan correctamente en la respuesta. Se necesita una revisión más profunda.

### 4. **DELETE /api/v1/resource/{id}**
   - **Resultado**: Éxito
   - **Descripción**: La solicitud DELETE elimina el recurso correctamente, con un código de estado 204. No se encontraron problemas.

## Problemas Identificados

### **Actualización de Recursos (PUT)**
   - **Descripción**: Algunas solicitudes PUT no reflejan los cambios esperados en la respuesta.
   - **Impacto**: Medio
   - **Acción Recomendada**: Se recomienda revisar la lógica del servidor que maneja las solicitudes PUT para garantizar que los cambios se guarden y se reflejen correctamente.

## Conclusión

En general, las pruebas realizadas a la API han demostrado que la mayoría de los endpoints funcionan correctamente y cumplen con los requisitos esperados. Sin embargo, se identificaron algunos problemas en la operación de actualización de recursos mediante el método PUT, lo que requiere una investigación adicional. Se recomienda tomar las acciones indicadas para corregir estos problemas y asegurar que la API continúe funcionando de manera óptima en las siguientes fases de desarrollo.
