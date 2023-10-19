<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->

## Clase vehiculo

class Vehiculo {
        protected String marca;
        protected String modelo;
        private int año;

        public Vehiculo(String marca, String modelo, int año) {
    this.marca = marca;
    this.modelo = modelo;
    this.año = año;
}

public void mostrarInformacion() {
    System.out.println("Marca: " + marca);
    System.out.println("Modelo: " + modelo);
    System.out.println("Año: " + año);
} }

## Subclase automovil

class Automovil extends Vehiculo {
private int numPuertas;
private String tipoTransmision;

public Automovil(String marca, String modelo, int año, int numPuertas, String tipoTransmision) {
    super(marca, modelo, año);
    this.numPuertas = numPuertas;
    this.tipoTransmision = tipoTransmision;
}

public void mostrarInformacionAutomovil() {
    System.out.println("Marca: " + marca);
    System.out.println("Modelo: " + modelo);
    System.out.println("Año: " + año);
    System.out.println("Número de Puertas: " + numPuertas);
    System.out.println("Tipo de Transmisión: " + tipoTransmision);
} }

## subclase Motocicleta

class Motocicleta extends Vehiculo {
private String tipo;
private int cilindraje;

public Motocicleta(String marca, String modelo, int año, String tipo, int cilindraje) {
    super(marca, modelo, año);
    this.tipo = tipo;
    this.cilindraje = cilindraje;
}

public void mostrarInformacionMotocicleta() {
    System.out.println("Marca: " + marca);
    System.out.println("Modelo: " + modelo);
    System.out.println("Año: " + año);
    System.out.println("Tipo: " + tipo);
    System.out.println("Cilindraje: " + cilindraje + " cc");
}

}

## Main

public class Main {
public static void main(String[] args) {
    Automovil automovil = new Automovil("Toyota", "Camry", 2022, 4, "Automática");
    
    automovil.mostrarInformacionAutomovil();
    
    Motocicleta motocicleta = new Motocicleta("Honda", "CBR500R", 2021, "Deportiva", 500);
    
    motocicleta.mostrarInformacionMotocicleta();
} 
}



