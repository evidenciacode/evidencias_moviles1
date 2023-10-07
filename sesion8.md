<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->
## Actividad 8 

package com.mycompany.actividad8;

import java.util.ArrayList;

public class Actividad8 {

    public static void main(String[] args) {
       Cancion C1 = new Cancion("julian", "Diciembre", "El Pesebre Julian");
       BandaSonora B1 = new BandaSonora("Titanio", "La Quemona");
       Album A1 = new Album("Mega", "San Jose");
    
       ArrayList<String> Canciones = new ArrayList<>();
       
       Canciones.add("El Pesebre");
       Canciones.add("Don Quijote");
       Canciones.add("El chupin");
       Canciones.add("El Despecho");

       System.out.println(Canciones.get(0));
       System.out.println(Canciones.get(1));
       System.out.println(Canciones.get(2));
       System.out.println(Canciones.get(3));

    }
    
}

## Album

package com.mycompany.actividad8;


public class Album extends Musica {
    private String Canciones;

    public Album(String Canciones, String TituloCancion) {
        super(TituloCancion);
        this.Canciones = Canciones;
    }
    
    @Override
    public void Play() {

    }

    @Override
    public void Stop() {

    }

    @Override
    public void Pause() {

    }

    @Override
    public void Next() {

    }

    @Override
    public void Previous() {

    }
}

## BandaSonora


package com.mycompany.actividad8;


public class BandaSonora extends Musica {
    private String Pelicula;

    public BandaSonora(String Pelicula, String TituloCancion) {
        super(TituloCancion);
        this.Pelicula = Pelicula;
    }
    
    
    @Override
    public void Play() {

    }

    @Override
    public void Stop() {

    }

    @Override
    public void Pause() {

    }

    @Override
    public void Next() {

    }

    @Override
    public void Previous() {

    }
    
    
}

## Cancion


package com.mycompany.actividad8;


public class Cancion extends Musica {
    private String Artista;
    private String Album;

    public Cancion(String Artista, String Album, String TituloCancion) {
        super(TituloCancion);
        this.Artista = Artista;
        this.Album = Album;
    }

    
    @Override
    public void Play() {

    }

    @Override
    public void Stop() {
        
    }

    @Override
    public void Pause() {

    }

    @Override
    public void Next() {

    }

    @Override
    public void Previous() {

    }

     
}
 ## Musica 

 
package com.mycompany.actividad8;


public abstract class Musica {
    String TituloCancion;

    public Musica(String TituloCancion) {
        this.TituloCancion = TituloCancion;
    }
    
    public String getTituloCancion() {
        return TituloCancion;
    }

    public void setTituloCancion(String TituloCancion) {
        this.TituloCancion = TituloCancion;
    }
    
    public abstract void Play();
    
    public abstract void Stop();
    
    public abstract void Pause();
    
    public abstract void Next();
    
    public abstract void Previous();
    
    
  
}










