##### PDF: 
- https://drive.google.com/file/d/1mhD-N4OhmRq8mEoQXCvCPRs60V7yK7rL/view?usp=sharing


##### Complemento:
La composición es un concepto fundamental en la programación orientada a objetos que permite crear relaciones entre clases de una manera más modular y flexible. En Java, la composición se refiere a la práctica de incluir objetos de una clase dentro de otra clase, creando así una relación "tiene un" entre ellas.

En el ejemplo proporcionado, vemos cómo la clase Persona "tiene un" DNI. Esto se logra declarando un atributo de tipo DNI dentro de la clase Persona. Esta técnica ofrece varias ventajas:

1. Modularidad: Permite dividir una clase grande y compleja en clases más pequeñas y manejables.

2. Reutilización de código: La clase DNI puede ser utilizada en otros contextos donde se necesite información de identificación.

3. Encapsulación: Los detalles internos de la clase DNI están ocultos para la clase Persona, lo que mejora la seguridad y reduce la complejidad.

4. Flexibilidad: Es más fácil modificar o reemplazar la clase DNI sin afectar directamente a la clase Persona.

Para implementar la composición en Java:

1. Crea las clases separadas (por ejemplo, Persona y DNI).
2. Declara un atributo en la clase contenedora (Persona) del tipo de la clase contenida (DNI).
3. Proporciona métodos getter y setter para acceder y modificar el objeto contenido.
4. Al crear instancias, crea primero el objeto contenido y luego asígnalo al objeto contenedor.

La composición es especialmente útil cuando se quiere representar relaciones complejas entre objetos sin recurrir a la herencia, lo que puede llevar a jerarquías de clases demasiado rígidas o complicadas.

Es importante notar que la composición crea una fuerte dependencia entre las clases, por lo que es crucial considerar cuidadosamente qué relaciones deben modelarse mediante composición y cuáles podrían beneficiarse de otros patrones de diseño o relaciones más flexibles.