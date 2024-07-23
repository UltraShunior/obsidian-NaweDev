El **Modelo de Datos Orientado a Documentos** es un enfoque de almacenamiento y administración de datos en [[Bases de datos NoSQL]], donde la unidad principal de almacenamiento es un "documento". Este modelo es muy diferente del modelo relacional tradicional ([[Bases de datos relacionales]]), que utiliza tablas, filas y columnas.

### Características del Modelo de Datos Orientado a Documentos

1. **Documentos**: Los documentos son las unidades fundamentales de datos. En MongoDB, estos documentos se representan en formato BSON (Binary JSON), una extensión binaria de JSON (JavaScript Object Notation). Los documentos pueden contener datos en estructuras jerárquicas y anidadas, lo que permite una representación rica de datos.
2. **Colecciones**: Los documentos se agrupan en colecciones. Una colección es un conjunto de documentos que están relacionados entre sí, similar a una tabla en una base de datos relacional, pero sin un esquema fijo.
3. **Esquemas Flexibles**: No es necesario definir un esquema antes de insertar datos en una colección. Esto permite almacenar documentos con diferentes estructuras en la misma colección.
4. **Tipos de Datos Diversos**: Los documentos pueden contener varios tipos de datos, como cadenas, números, fechas, matrices y otros documentos anidados.

### Cómo Funciona

1. **Creación de Documentos**: Un documento en una base de datos orientada a documentos es una estructura JSON/BSON que contiene pares de campo-valor. Los valores pueden ser datos primitivos (como cadenas o números), matrices, u otros documentos.
   ```json
   {
       "nombre": "Juan Pérez",
       "edad": 30,
       "direccion": {
           "calle": "Calle 123",
           "ciudad": "Ciudad ABC"
       },
       "hobbies": ["lectura", "fútbol"]
   }
   ```

2. **Almacenamiento en Colecciones**: Los documentos se almacenan en colecciones. Aunque no se requiere un esquema fijo, es común que los documentos en una colección compartan algunas características y estructuras similares.
   ```json
   [
       {
           "nombre": "Juan Pérez",
           "edad": 30,
           "direccion": {
               "calle": "Calle 123",
               "ciudad": "Ciudad ABC"
           },
           "hobbies": ["lectura", "fútbol"]
       },
       {
           "nombre": "María Gómez",
           "edad": 25,
           "direccion": {
               "calle": "Avenida 456",
               "ciudad": "Ciudad XYZ"
           },
           "hobbies": ["cocina", "natación"]
       }
   ]
   ```

3. **Consultas**: Las consultas en bases de datos orientadas a documentos son flexibles y permiten buscar documentos basados en cualquier campo. Además, MongoDB ofrece operaciones avanzadas como agregaciones, búsquedas de texto completo y operaciones geoespaciales.
   ```javascript
   db.coleccion.find({ "edad": { "$gt": 25 } })
   ```
   Esta consulta busca todos los documentos en la colección "coleccion" donde el campo "edad" es mayor que 25.

4. **Actualizaciones**: Los documentos pueden ser actualizados fácilmente, y es posible modificar solo partes del documento sin necesidad de actualizar todo el documento.
   ```javascript
   db.coleccion.updateOne(
       { "nombre": "Juan Pérez" },
       { "$set": { "direccion.ciudad": "Nueva Ciudad" } }
   )
   ```

5. **Escalabilidad**: MongoDB y otras bases de datos orientadas a documentos están diseñadas para escalar horizontalmente mediante sharding, lo que permite distribuir documentos en múltiples nodos de una manera eficiente.

### Ventajas del Modelo de Datos Orientado a Documentos

- **Flexibilidad**: La capacidad de almacenar datos sin un esquema fijo permite una rápida adaptación a los cambios en los requisitos de la aplicación.
- **Simplicidad**: El modelo de documentos es intuitivo y se alinea bien con las estructuras de datos utilizadas en la programación moderna, especialmente en aplicaciones web.
- **Escalabilidad**: Las bases de datos orientadas a documentos están diseñadas para manejar grandes volúmenes de datos y pueden escalar horizontalmente.
- **Eficiencia en Lectura y Escritura**: Optimizado para operaciones rápidas de lectura y escritura, adecuado para aplicaciones en tiempo real.

En resumen, el modelo de datos orientado a documentos es una forma poderosa y flexible de manejar datos, especialmente en aplicaciones modernas donde la estructura de los datos puede cambiar rápidamente.