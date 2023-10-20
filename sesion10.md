<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->


## Ejercicio 1

## Clase Vehiculo

public abstract class Vehiculo {
    
    public abstract void acelerar();
    public abstract void frenar();
    public abstract void girar();

   
    }

## Coche

public class Coche extends Vehiculo {

    public Coche() {
    }

    @Override
    public void acelerar() {
       
    }

    @Override
    public void frenar() {
       
    }

    @Override
    public void girar() {
        
    }
    
    
}

## Moto

public class Moto extends Vehiculo {

    public Moto() {
    }

    @Override
    public void acelerar() {
        
    }

    @Override
    public void frenar() {
        
    }

    @Override
    public void girar() {
        
    }
    
    
}


## Bicicleta

class Bicicleta extends Vehiculo {

    @Override
    void acelerar() {
        System.out.println("La bicicleta acelera");
    }

    @Override
    void frenar() {
        System.out.println("La bicicleta frena");
    }

    @Override
    void girar() {
        System.out.println("La bicicleta gira");
    }
    
}

## Main

public static void main(String[] args) {
     ArrayList<Vehiculo> vehiculos = new ArrayList<>();
        vehiculos.add(new Coche());
        vehiculos.add(new Bicicleta());
        vehiculos.add(new Moto());

        for (Vehiculo vehiculo : vehiculos) {    
            vehiculo.acelerar();
            vehiculo.frenar();
            vehiculo.girar();
         
        }
    }
  
## --------------------------------------------------------  

