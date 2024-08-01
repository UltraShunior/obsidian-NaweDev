Para resolver tu ejercicio sobre la clase `Lapicera`, la clase `Cartucho` y la clase `Hoja`, implementaremos las tres clases necesarias. A continuación, se presenta una posible solución en Java:

```java
// Clase Cartucho
class Cartucho {
    private int cantidadTinta; // Cantidad de tinta representada por la cantidad de letras que se pueden escribir

    // Constructor
    public Cartucho(int cantidadTinta) {
        this.cantidadTinta = cantidadTinta;
    }

    // Método para obtener la cantidad de tinta restante
    public int getCantidadTinta() {
        return cantidadTinta;
    }

    // Método para reducir la cantidad de tinta
    public void gastarTinta(int cantidad) {
        this.cantidadTinta -= cantidad;
    }
}

// Clase Lapicera
class Lapicera {
    private Cartucho cartucho; // Cartucho de tinta

    // Constructor
    public Lapicera(Cartucho cartucho) {
        this.cartucho = cartucho;
    }

    // Método para imprimir el nivel de tinta restante
    public void nivelTinta() {
        System.out.println("Nivel de tinta: " + cartucho.getCantidadTinta() + " letras.");
    }

    // Método para escribir una frase
    public void escribir(String frase) {
        int longitudFrase = frase.length(); // Calcula la longitud de la frase

        // Comprobar si hay suficiente tinta
        if (longitudFrase <= cartucho.getCantidadTinta()) {
            System.out.println(frase); // Imprime la frase
            cartucho.gastarTinta(longitudFrase); // Reduce la cantidad de tinta
        } else {
            System.out.println("Tinta insuficiente, por favor cambie el cartucho.");
        }
    }
}

// Clase Hoja (ejecutable)
public class Hoja {
    public static void main(String[] args) {
        // Crear un cartucho con una cantidad de tinta
        Cartucho cartucho = new Cartucho(50); // Cartucho con capacidad para escribir 50 letras

        // Crear una lapicera y ponerle el cartucho
        Lapicera lapicera = new Lapicera(cartucho);

        // Imprimir el nivel de tinta actual
        lapicera.nivelTinta();

        // Intentar escribir una frase
        String frase = "Hola, este es un ejemplo de escritura.";
        lapicera.escribir(frase); // Escribir una frase

        // Imprimir el nivel de tinta después de escribir
        lapicera.nivelTinta();
    }
}
```

### Explicación del código:

1. **Clase `Cartucho`:**
   - Tiene un atributo `cantidadTinta` que representa la capacidad del cartucho (número de letras que puede escribir).
   - Un constructor que inicializa la cantidad de tinta.
   - Un método `getCantidadTinta()` para acceder a la cantidad de tinta restante.
   - Un método `gastarTinta(int cantidad)` que reduce la cantidad de tinta disponible.

2. **Clase `Lapicera`:**
   - Tiene un atributo `cartucho` que representa el cartucho de tinta asociado a la lapicera.
   - Un constructor que inicializa la lapicera con el cartucho dado.
   - Un método `nivelTinta()` que imprime el nivel de tinta restante.
   - Un método `escribir(String frase)` que imprime la frase si hay suficiente tinta; de lo contrario, informa que la tinta es insuficiente.

3. **Clase `Hoja` (ejecutable):**
   - En el método `main`, se crea un cartucho y se establece una cantidad de tinta.
   - Luego se crea una `Lapicera` y se le asigna el cartucho.
   - Se imprime el nivel de tinta antes de escribir, se intenta escribir una frase y luego se imprime el nivel de tinta restante.

Cuando ejecutes este código, debería mostrar el nivel de tinta, imprimir la frase si hay tinta suficiente y luego mostrar el nivel de tinta después de escribir.