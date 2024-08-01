##### Consigna:
Crear las clases necesarias para cumplir con los siguientes comportamientos:
● Diario: Cada diario tiene un nombre, un titular y la fecha en que se publicó. Dichos datos se establecen en el momento en que se crea el mismo.
● Imprenta: La imprenta tan sólo imprime los diarios que recibe. Para eso, tiene un método “imprimir” que recibe una lista de diarios e imprime fecha, nombre y titular de cada diario.

##### Respuesta:
Necesitamos 2 clases, `Diario` e `Imprenta`:


```java
import java.util.ArrayList;
import java.util.List;

// Clase Diario
class Diario {
    private String nombre;
    private String titular;
    private String fecha;

    // Constructor
    public Diario(String nombre, String titular, String fecha) {
        this.nombre = nombre;
        this.titular = titular;
        this.fecha = fecha;
    }

    // Métodos getter para acceder a los atributos
    public String getNombre() {
        return nombre;
    }

    public String getTitular() {
        return titular;
    }

    public String getFecha() {
        return fecha;
    }
}

// Clase Imprenta
class Imprenta {
    public void imprimir(List<Diario> diarios) {
        for (Diario diario : diarios) {
            System.out.println("Fecha: " + diario.getFecha());
            System.out.println("Nombre: " + diario.getNombre());
            System.out.println("Titular: " + diario.getTitular());
            System.out.println("--------------------------------");
        }
    }
}

// Clase principal para ejecutar el código
public class Main {
    public static void main(String[] args) {
        // Crear algunos diarios
        Diario diario1 = new Diario("El Mundo", "Titular del Mundo", "2023-10-01");
        Diario diario2 = new Diario("La Nación", "Titular de la Nación", "2023-10-02");
        Diario diario3 = new Diario("El País", "Titular del País", "2023-10-03");

        // Agregar diarios a una lista
        List<Diario> listaDiarios = new ArrayList<>();
        listaDiarios.add(diario1);
        listaDiarios.add(diario2);
        listaDiarios.add(diario3);

        // Crear la imprenta y imprimir los diarios
        Imprenta imprenta = new Imprenta();
        imprenta.imprimir(listaDiarios);
    }
}
```

### Explicación del código:

1. **Clase `Diario`:** 
    - Contiene tres atributos: `nombre`, `titular` y `fecha`.
    - Un constructor que inicializa estos atributos al momento de la creación del objeto.
    - Métodos getter para acceder a los valores de los atributos.

2. **Clase `Imprenta`:**
    - Contiene un método `imprimir` que recibe una lista de objetos `Diario`.
    - El método itera sobre la lista y utiliza los métodos getter para imprimir la fecha, nombre y titular de cada diario en la consola.

3. **Clase `Main`:**
    - Es la clase principal donde se crean algunas instancias de `Diario`, se agregan a una lista y se llama al método `imprimir` de la clase `Imprenta`.

Cuando ejecutes este código, deberías ver la información de los diarios impresa en la consola.