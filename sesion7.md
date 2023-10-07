<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->
## Actividad 7


public class Actividad7 {

    public static void main(String[] args) {
        Producto P1 = new Producto();
        P1.mostrarInformacion();
       
        Producto P2 = new Producto("Laptop", 200000);
        P2.mostrarInformacion();
       
        Producto P3 = new Producto("Iphone", 5000, 5);
        P3.mostrarInformacion();
    }
}


## Producto

public class Producto {
    private String nombre;
    private double precio;
    private int cantidadDisponible;
    
    public Producto(){
        this.nombre = "desconocido";
        this.precio = 0.0;
        this.cantidadDisponible = 0;
    }

    public Producto(String nombre, double precio) {
        this.nombre = nombre;
        this.precio = precio;
        this.cantidadDisponible = 0;
    }

    public Producto(String nombre, double precio, int cantidadDisponible) {
        this.nombre = nombre;
        this.precio = precio;
        this.cantidadDisponible = cantidadDisponible;
    }
    
    public double CalcularValorTotal(){
        return this.precio * this.cantidadDisponible;
        
    }
    
    public void mostrarInformacion(){
        System.out.println("Nombre: " + this.nombre);
        System.out.println("Precio: " + this.precio);
        System.out.println("Cantidad: " + this.cantidadDisponible);
    }
    
    public void incrementarCantidad(){
        this.cantidadDisponible = this.cantidadDisponible + 1;
    }
    
    public void incrementarCantidad(int CantidadIncrementar){
        this.cantidadDisponible = this.cantidadDisponible + CantidadIncrementar;
    }
    
    public void actualizarPrecio(double nuevoPrecio) {
        precio = nuevoPrecio;
    }
    
     public void actualizarPrecio(double nuevoPrecio, String moneda) {
        double tasaCambio = 1.0;
        switch (moneda) {
            case "EUR":
                tasaCambio = 1.2; 
                break;
            case "COP":
                tasaCambio = 0.00027; 
                break;
            
        }
        precio = nuevoPrecio * tasaCambio;
    }

    public void actualizarPrecio(double nuevoPrecio, String moneda, double tasaCambio) {
        precio = nuevoPrecio * tasaCambio;
    }

    public static void main(String[] args) {
 
        Producto producto1 = new Producto();
        Producto producto2 = new Producto("Laptop", 800.0);
        Producto producto3 = new Producto("Teléfono", 500.0, 10);

        System.out.println("Producto 1:");
        producto1.mostrarInformacion();

        System.out.println("\nProducto 2:");
        producto2.mostrarInformacion();

        System.out.println("\nProducto 3:");
        producto3.mostrarInformacion();

        producto1.incrementarCantidad();
        producto2.incrementarCantidad(5);

        producto1.actualizarPrecio(25.0);
        producto2.actualizarPrecio(1000.0, "EUR");
        producto3.actualizarPrecio(800000.0, "COP");
        producto3.actualizarPrecio(750.0, "USD", 0.00027);

        System.out.println("\nProducto 1 (Después de actualizar):");
        producto1.mostrarInformacion();

        System.out.println("\nProducto 2 (Después de actualizar):");
        producto2.mostrarInformacion();

        System.out.println("\nProducto 3 (Después de actualizar):");
        producto3.mostrarInformacion();
    }

}


